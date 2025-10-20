---
title: 程式碼型實施中的決定專案重複資料刪除
description: 本頁說明如何在Journey Optimizer程式碼型實施中，將重複資料刪除套用至您的決策請求。
feature: Code-based Experiences
topic: Content Management
role: Developer
level: Experienced
exl-id: f9477611-b792-4b28-8ec2-6bbea2fa3328
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '371'
ht-degree: 1%

---

# 程式碼型體驗實作中的決策

在程式碼型體驗中使用決策時，請考慮在下列所述的情況下將下列標幟新增到您的使用者端實作。

## 使用決定測試程式碼型體驗 {#code-based-test-decisions}

<!--Currently you cannot simulate content from the user interface in a [code-based experience](create-code-based.md) campaign or journey using decisions.-->

使用決策測試[程式碼型體驗](create-code-based.md)時，`dryRun`旗標可用於抑制報表和上限計數器的意見反應事件。

發佈行銷活動後，將`dryRun`標幟新增至使用者端實作中的XDM事件`data`區塊：

```
{
    "data": {
        "__adobe": {
            "ajo": {
                "dryRun": true
            }
        }
    }
}
```

<!--
>[!CAUTION]
>
>Adding the `dryRun` flag to your request will prevent feedback to be captured for reporting and frequency counters from being added to.-->

## 程式碼型實施中的決定專案重複資料刪除 {#code-based-decisioning-deduplication}

當您在程式碼型體驗中使用[決定原則](../experience-decisioning/create-decision.md)時，您可以在使用者端實作中將重複資料刪除套用至您的決定請求。

決策請求（透過Konductor）接受重複資料刪除旗標，這會處理包含多個決策原則或位置的單一請求中的決策專案唯一性。

### 重複資料刪除邏輯 {#deduplication-logic}

對於任何決策請求，您可以根據設定有一或多個決策原則/位置。

* 對於&#x200B;**單一**&#x200B;決定原則以及請求中的位置，回應中的所有專案都是唯一的（依預設）。 單一請求中的兩個決定專案不能相同。

* 針對請求中的&#x200B;**多個**&#x200B;決定原則/位置：

   * 如果`allowDuplicateDecisionItems`設為`false`：回應中的所有專案都是唯一的（無論專案是用於哪個訊息/決定原則/位置）。

   * 如果`allowDuplicateDecisionItems`設為`true` （預設）：回應中的專案可以重複（如果多個訊息/決定原則/位置符合該請求的相同決定專案的資格）。

### 在請求中套用重複資料刪除 {#deduplication-in-request}

依照預設，重複資料刪除旗標設為`true`。

在Konductor請求中，如果您想在回應中取得唯一元素，可傳遞重複資料刪除旗標。 在此情況下，請將其設為`false`。

```
{
    "data": {
        "__adobe": {
            "ajo": {
                "allowDuplicateDecisionItems": false
            }
        }
    }
}
```

+++決策範例請求

```
curl --location 'https://edge-int.adobedc.net/ee/v1/interact?configId=2f21d344-b69f-4a4f-98e8-000282fc9552' \
--header 'Content-Type: application/json' \
--data-raw '{
    "events": [
        {
            "query": {
                "personalization": {
                    "schemas": [
                        "https://ns.adobe.com/personalization/html-content-item"
                    ],
                    "surfaces": [
                        "https://www.adobe.com/san/placement/header",
                        "https://www.adobe.com/san/placement/footer"
                    ]
                }
            },
            "xdm": {
                "identityMap": {
                    "Email": [
                        {
                            "id": "cmk-exd-user01-deleted@adobe.com",
                            "primary": true
                        }
                    ]
                }
            },
            "data": {
                "__adobe":{
                    "ajo":{
                        "allowDuplicateDecisionItems": false
                    }
                }       
            }
        }
    ]
}'
```

+++

### 重複資料刪除回應 {#deduplication-response}

假設您的決定原則與單一請求中頁首和頁尾的位置相同。

* 決策會傳回兩個主張。

* 如果`itemId-X`是同時符合決定原則與位置組合的單一決定專案：

   * 如果`allowDuplicateDecisionItems`是`true`（預設）：在單一回應中傳回兩個主張的`itemId-X`。

   * 如果`allowDuplicateDecisionItems`是`false`：

      * 第一個主張會傳回`itemId-X`。

      * 系統會為第二個主張傳遞遞補決定專案（也是唯一的）或空白決定專案。

+++決定範例回應(`allowDuplicateDecisionItems` = `true`)

```
{
    "requestId": "b40170e9-7d31-4242-adcc-18063d6b1d9e",
    "handle": [
        {
            "payload": [
                {
                    "id": "d97f102c-bdae-4ed7-aff6-622d73e3db3d",
                    "scope": "https://www.adobe.com/san/placement/header",
                    "scopeDetails": {
                        "decisionProvider": "AJO",
                        "correlationID": "3cc4ee00-bb76-4eaa-94b6-9b9be2c53e3a-0",
                        "characteristics": {
                            "eventToken": "eyJtZXNzYWdlRXhlY3V0aW9uIjp7Im1lc3NhZ2VFeGVjdXRpb25JRCI6IlVFOkluYm91bmQiLCJtZXNzYWdlSUQiOiJmYWM4YzVmZi1mYWNlLTRkOWItYmEzYi0yYzJjZTEyYzBjODYiLCJtZXNzYWdlUHVibGljYXRpb25JRCI6IjNjYzRlZTAwLWJiNzYtNGVhYS05NGI2LTliOWJlMmM1M2UzYSIsIm1lc3NhZ2VUeXBlIjoibWFya2V0aW5nIiwiY2FtcGFpZ25JRCI6ImUzYmJlZmZkLTZjYjItNGEwMy1iMjRhLTk1YzQ5ZjBkZjRlNCIsImNhbXBhaWduVmVyc2lvbklEIjoiZDlmMTMwNjAtZGVhNC00MTE1LTk5YzMtOGZjMTRjMWFiNTFiIiwiY2FtcGFpZ25BY3Rpb25JRCI6ImE1NmE0OTIxLWJjMjQtNGRjMC04Nzk3LTA2NmU4YzE0NTM5YiJ9LCJtZXNzYWdlUHJvZmlsZSI6eyJtZXNzYWdlUHJvZmlsZUlEIjoiYmQxMDEzNGMtNjBkMS00NjZiLWEwYWMtOWQ0MzdmNmY5YTczIiwiY2hhbm5lbCI6eyJfaWQiOiJodHRwczovL25zLmFkb2JlLmNvbS94ZG0vY2hhbm5lbHMvY29kZSIsIl90eXBlIjoiaHR0cHM6Ly9ucy5hZG9iZS5jb20veGRtL2NoYW5uZWwtdHlwZXMvY29kZSJ9fX0=",
                            "subPropositions": "W3siaWQiOiI4ZmMzMDBjYy1iMTg5LTQ2MTUtYmY0OC03NjIwMjZkMjlmMWYiLCJzY29wZSI6Imh0dHBzOi8vd3d3LmFkb2JlLmNvbS9zYW4vcGxhY2VtZW50L2hlYWRlciIsInNjb3BlRGV0YWlscyI6eyJkZWNpc2lvblByb3ZpZGVyIjoiRVhEIiwiY29ycmVsYXRpb25JRCI6IjNjYzRlZTAwLWJiNzYtNGVhYS05NGI2LTliOWJlMmM1M2UzYS0wIiwic3RyYXRlZ2llcyI6W3sic3RyYXRlZ3lJRCI6IjlhOTRjZjhjLTNkZjItNDE2NS1hMzRiLTIxNzBlMjg2YmUzMiIsInN0ZXAiOiJkZWNpc2lvblBvbGljeSJ9LHsic3RyYXRlZ3lJRCI6Imh0dHBzOi8vd3d3LmFkb2JlLmNvbS9zYW4vcGxhY2VtZW50L2hlYWRlciIsInN0ZXAiOiJwbGFjZW1lbnQifV0sInJhbmsiOjEsImFjdGl2aXR5Ijp7ImlkIjoiZTNiYmVmZmQtNmNiMi00YTAzLWIyNGEtOTVjNDlmMGRmNGU0I2E1NmE0OTIxLWJjMjQtNGRjMC04Nzk3LTA2NmU4YzE0NTM5YiIsInByaW9yaXR5IjowLCJtYXRjaGVkU3VyZmFjZXMiOlsiaHR0cHM6Ly93d3cuYWRvYmUuY29tL3Nhbi9wbGFjZW1lbnQvaGVhZGVyIl19fSwiaXRlbXMiOlt7ImlkIjoiZHBzOmM3MjI1YzNmYWMxNGUzMDBjYTNkZTlmY2I2ZDk4NTI0YjM5NTQ4YzFmYzFlYmQ2OToxOThkM2I5NDczZDRjYzQ3IiwiZXRhZyI6IjciLCJuYW1lIjoidGVzdFNhbi1tYW51YWxGYWxsYmFjay1vZmZlcjAxIiwic2NvcmUiOjExLjAsIml0ZW1TZWxlY3Rpb24iOnsic2VsZWN0aW9uRGV0YWlsIjp7InN0cmF0ZWd5SUQiOiJkcHM6c2VsZWN0aW9uLXN0cmF0ZWd5OjFhMGUzOTY4NzJlOWZiMWUiLCJzdHJhdGVneU5hbWUiOiJ0ZXN0U2FuLW1hbnVhbEZhbGxiYWNrLXN0cmF0ZWd5MTAwIiwic2VsZWN0aW9uVHlwZSI6InNlbGVjdGlvblN0cmF0ZWd5IiwidmVyc2lvbiI6Ijc0NUYzN0MzNUU0Qjc3NkUwQTQ5NDIxQkBBZG9iZU9yZzo2MzM5NzRmNC1lNTRlLTQyZjMtYjk3NC1mNGU1NGVjMmYzYmU6NThlNjE0MTItZTExOS00Mjg4LWJiZGEtYmQ1NGQ1MDgxNjVmIn0sInJhbmtpbmdEZXRhaWwiOnsic3RlcCI6InByaW9yaXR5In19LCJ0b2tlbiI6IitsckV1NWtHdnkrRXVYRFZ1K0VMWHcifV19XQ=="
                        },
                        "rank": 1,
                        "activity": {
                            "id": "e3bbeffd-6cb2-4a03-b24a-95c49f0df4e4#a56a4921-bc24-4dc0-8797-066e8c14539b",
                            "priority": 0,
                            "matchedSurfaces": [
                                "https://www.adobe.com/san/placement/header"
                            ]
                        }
                    },
                    "items": [
                        {
                            "id": "f37463f7-d23b-4ef1-b412-de1ac127efb9",
                            "schema": "https://ns.adobe.com/personalization/html-content-item",
                            "data": {
                                "content": "\nitemId: dps:c7225c3fac14e300ca3de9fcb6d98524b39548c1fc1ebd69:198d3b9473d4cc47\nitemName: testSan-manualFallback-offer01\ntrackingToken: +lrEu5kGvy+EuXDVu+ELXw\n"
                            }
                        }
                    ]
                },
                {
                    "id": "e1de0998-44d6-435d-8974-1d5175a845ea",
                    "scope": "https://www.adobe.com/san/placement/footer",
                    "scopeDetails": {
                        "decisionProvider": "AJO",
                        "correlationID": "3cc4ee00-bb76-4eaa-94b6-9b9be2c53e3a-0",
                        "characteristics": {
                            "eventToken": "eyJtZXNzYWdlRXhlY3V0aW9uIjp7Im1lc3NhZ2VFeGVjdXRpb25JRCI6IlVFOkluYm91bmQiLCJtZXNzYWdlSUQiOiJmYWM4YzVmZi1mYWNlLTRkOWItYmEzYi0yYzJjZTEyYzBjODYiLCJtZXNzYWdlUHVibGljYXRpb25JRCI6IjNjYzRlZTAwLWJiNzYtNGVhYS05NGI2LTliOWJlMmM1M2UzYSIsIm1lc3NhZ2VUeXBlIjoibWFya2V0aW5nIiwiY2FtcGFpZ25JRCI6ImUzYmJlZmZkLTZjYjItNGEwMy1iMjRhLTk1YzQ5ZjBkZjRlNCIsImNhbXBhaWduVmVyc2lvbklEIjoiZDlmMTMwNjAtZGVhNC00MTE1LTk5YzMtOGZjMTRjMWFiNTFiIiwiY2FtcGFpZ25BY3Rpb25JRCI6ImE1NmE0OTIxLWJjMjQtNGRjMC04Nzk3LTA2NmU4YzE0NTM5YiJ9LCJtZXNzYWdlUHJvZmlsZSI6eyJtZXNzYWdlUHJvZmlsZUlEIjoiMGI4NTYxMzAtNDZiNy00OTQ1LTgwYTAtZjM2MGUzMjhlMjllIiwiY2hhbm5lbCI6eyJfaWQiOiJodHRwczovL25zLmFkb2JlLmNvbS94ZG0vY2hhbm5lbHMvY29kZSIsIl90eXBlIjoiaHR0cHM6Ly9ucy5hZG9iZS5jb20veGRtL2NoYW5uZWwtdHlwZXMvY29kZSJ9fX0=",
                            "subPropositions": "W3siaWQiOiI1NzViZDY3My0yMTQ1LTQ2MzAtYjQ1Yy1iNDAwMGUxMzI1NmMiLCJzY29wZSI6Imh0dHBzOi8vd3d3LmFkb2JlLmNvbS9zYW4vcGxhY2VtZW50L2Zvb3RlciIsInNjb3BlRGV0YWlscyI6eyJkZWNpc2lvblByb3ZpZGVyIjoiRVhEIiwiY29ycmVsYXRpb25JRCI6IjNjYzRlZTAwLWJiNzYtNGVhYS05NGI2LTliOWJlMmM1M2UzYS0wIiwic3RyYXRlZ2llcyI6W3sic3RyYXRlZ3lJRCI6IjlhOTRjZjhjLTNkZjItNDE2NS1hMzRiLTIxNzBlMjg2YmUzMiIsInN0ZXAiOiJkZWNpc2lvblBvbGljeSJ9LHsic3RyYXRlZ3lJRCI6Imh0dHBzOi8vd3d3LmFkb2JlLmNvbS9zYW4vcGxhY2VtZW50L2Zvb3RlciIsInN0ZXAiOiJwbGFjZW1lbnQifV0sInJhbmsiOjEsImFjdGl2aXR5Ijp7ImlkIjoiZTNiYmVmZmQtNmNiMi00YTAzLWIyNGEtOTVjNDlmMGRmNGU0I2E1NmE0OTIxLWJjMjQtNGRjMC04Nzk3LTA2NmU4YzE0NTM5YiIsInByaW9yaXR5IjowLCJtYXRjaGVkU3VyZmFjZXMiOlsiaHR0cHM6Ly93d3cuYWRvYmUuY29tL3Nhbi9wbGFjZW1lbnQvZm9vdGVyIl19fSwiaXRlbXMiOltdfV0="
                        },
                        "rank": 1,
                        "activity": {
                            "id": "e3bbeffd-6cb2-4a03-b24a-95c49f0df4e4#a56a4921-bc24-4dc0-8797-066e8c14539b",
                            "priority": 0,
                            "matchedSurfaces": [
                                "https://www.adobe.com/san/placement/footer"
                            ]
                        }
                    },
                    "items": [
                        {
                            "id": "f37463f7-d23b-4ef1-b412-de1ac127efb9",
                            "schema": "https://ns.adobe.com/personalization/html-content-item",
                            "data": {
                                "content": "\nitemId: dps:c7225c3fac14e300ca3de9fcb6d98524b39548c1fc1ebd69:198d3b9473d4cc47\nitemName: testSan-manualFallback-offer01\ntrackingToken: +lrEu5kGvy+EuXDVu+ELXw\n"
                            }
                        }
                    ]
                }
            ],
            "type": "personalization:decisions",
            "eventIndex": 0
        }
    ]
}
```

+++

+++決定範例回應(`allowDuplicateDecisionItems` = `false`)

```
{
    "requestId": "b40170e9-7d31-4242-adcc-18063d6b1d9e",
    "handle": [
        {
            "payload": [
                {
                    "id": "d97f102c-bdae-4ed7-aff6-622d73e3db3d",
                    "scope": "https://www.adobe.com/san/placement/header",
                    "scopeDetails": {
                        "decisionProvider": "AJO",
                        "correlationID": "3cc4ee00-bb76-4eaa-94b6-9b9be2c53e3a-0",
                        "characteristics": {
                            "eventToken": "eyJtZXNzYWdlRXhlY3V0aW9uIjp7Im1lc3NhZ2VFeGVjdXRpb25JRCI6IlVFOkluYm91bmQiLCJtZXNzYWdlSUQiOiJmYWM4YzVmZi1mYWNlLTRkOWItYmEzYi0yYzJjZTEyYzBjODYiLCJtZXNzYWdlUHVibGljYXRpb25JRCI6IjNjYzRlZTAwLWJiNzYtNGVhYS05NGI2LTliOWJlMmM1M2UzYSIsIm1lc3NhZ2VUeXBlIjoibWFya2V0aW5nIiwiY2FtcGFpZ25JRCI6ImUzYmJlZmZkLTZjYjItNGEwMy1iMjRhLTk1YzQ5ZjBkZjRlNCIsImNhbXBhaWduVmVyc2lvbklEIjoiZDlmMTMwNjAtZGVhNC00MTE1LTk5YzMtOGZjMTRjMWFiNTFiIiwiY2FtcGFpZ25BY3Rpb25JRCI6ImE1NmE0OTIxLWJjMjQtNGRjMC04Nzk3LTA2NmU4YzE0NTM5YiJ9LCJtZXNzYWdlUHJvZmlsZSI6eyJtZXNzYWdlUHJvZmlsZUlEIjoiYmQxMDEzNGMtNjBkMS00NjZiLWEwYWMtOWQ0MzdmNmY5YTczIiwiY2hhbm5lbCI6eyJfaWQiOiJodHRwczovL25zLmFkb2JlLmNvbS94ZG0vY2hhbm5lbHMvY29kZSIsIl90eXBlIjoiaHR0cHM6Ly9ucy5hZG9iZS5jb20veGRtL2NoYW5uZWwtdHlwZXMvY29kZSJ9fX0=",
                            "subPropositions": "W3siaWQiOiI4ZmMzMDBjYy1iMTg5LTQ2MTUtYmY0OC03NjIwMjZkMjlmMWYiLCJzY29wZSI6Imh0dHBzOi8vd3d3LmFkb2JlLmNvbS9zYW4vcGxhY2VtZW50L2hlYWRlciIsInNjb3BlRGV0YWlscyI6eyJkZWNpc2lvblByb3ZpZGVyIjoiRVhEIiwiY29ycmVsYXRpb25JRCI6IjNjYzRlZTAwLWJiNzYtNGVhYS05NGI2LTliOWJlMmM1M2UzYS0wIiwic3RyYXRlZ2llcyI6W3sic3RyYXRlZ3lJRCI6IjlhOTRjZjhjLTNkZjItNDE2NS1hMzRiLTIxNzBlMjg2YmUzMiIsInN0ZXAiOiJkZWNpc2lvblBvbGljeSJ9LHsic3RyYXRlZ3lJRCI6Imh0dHBzOi8vd3d3LmFkb2JlLmNvbS9zYW4vcGxhY2VtZW50L2hlYWRlciIsInN0ZXAiOiJwbGFjZW1lbnQifV0sInJhbmsiOjEsImFjdGl2aXR5Ijp7ImlkIjoiZTNiYmVmZmQtNmNiMi00YTAzLWIyNGEtOTVjNDlmMGRmNGU0I2E1NmE0OTIxLWJjMjQtNGRjMC04Nzk3LTA2NmU4YzE0NTM5YiIsInByaW9yaXR5IjowLCJtYXRjaGVkU3VyZmFjZXMiOlsiaHR0cHM6Ly93d3cuYWRvYmUuY29tL3Nhbi9wbGFjZW1lbnQvaGVhZGVyIl19fSwiaXRlbXMiOlt7ImlkIjoiZHBzOmM3MjI1YzNmYWMxNGUzMDBjYTNkZTlmY2I2ZDk4NTI0YjM5NTQ4YzFmYzFlYmQ2OToxOThkM2I5NDczZDRjYzQ3IiwiZXRhZyI6IjciLCJuYW1lIjoidGVzdFNhbi1tYW51YWxGYWxsYmFjay1vZmZlcjAxIiwic2NvcmUiOjExLjAsIml0ZW1TZWxlY3Rpb24iOnsic2VsZWN0aW9uRGV0YWlsIjp7InN0cmF0ZWd5SUQiOiJkcHM6c2VsZWN0aW9uLXN0cmF0ZWd5OjFhMGUzOTY4NzJlOWZiMWUiLCJzdHJhdGVneU5hbWUiOiJ0ZXN0U2FuLW1hbnVhbEZhbGxiYWNrLXN0cmF0ZWd5MTAwIiwic2VsZWN0aW9uVHlwZSI6InNlbGVjdGlvblN0cmF0ZWd5IiwidmVyc2lvbiI6Ijc0NUYzN0MzNUU0Qjc3NkUwQTQ5NDIxQkBBZG9iZU9yZzo2MzM5NzRmNC1lNTRlLTQyZjMtYjk3NC1mNGU1NGVjMmYzYmU6NThlNjE0MTItZTExOS00Mjg4LWJiZGEtYmQ1NGQ1MDgxNjVmIn0sInJhbmtpbmdEZXRhaWwiOnsic3RlcCI6InByaW9yaXR5In19LCJ0b2tlbiI6IitsckV1NWtHdnkrRXVYRFZ1K0VMWHcifV19XQ=="
                        },
                        "rank": 1,
                        "activity": {
                            "id": "e3bbeffd-6cb2-4a03-b24a-95c49f0df4e4#a56a4921-bc24-4dc0-8797-066e8c14539b",
                            "priority": 0,
                            "matchedSurfaces": [
                                "https://www.adobe.com/san/placement/header"
                            ]
                        }
                    },
                    "items": [
                        {
                            "id": "f37463f7-d23b-4ef1-b412-de1ac127efb9",
                            "schema": "https://ns.adobe.com/personalization/html-content-item",
                            "data": {
                                "content": "\nitemId: dps:c7225c3fac14e300ca3de9fcb6d98524b39548c1fc1ebd69:198d3b9473d4cc47\nitemName: testSan-manualFallback-offer01\ntrackingToken: +lrEu5kGvy+EuXDVu+ELXw\n"
                            }
                        }
                    ]
                },
                {
                    "id": "e1de0998-44d6-435d-8974-1d5175a845ea",
                    "scope": "https://www.adobe.com/san/placement/footer",
                    "scopeDetails": {
                        "decisionProvider": "AJO",
                        "correlationID": "3cc4ee00-bb76-4eaa-94b6-9b9be2c53e3a-0",
                        "characteristics": {
                            "eventToken": "eyJtZXNzYWdlRXhlY3V0aW9uIjp7Im1lc3NhZ2VFeGVjdXRpb25JRCI6IlVFOkluYm91bmQiLCJtZXNzYWdlSUQiOiJmYWM4YzVmZi1mYWNlLTRkOWItYmEzYi0yYzJjZTEyYzBjODYiLCJtZXNzYWdlUHVibGljYXRpb25JRCI6IjNjYzRlZTAwLWJiNzYtNGVhYS05NGI2LTliOWJlMmM1M2UzYSIsIm1lc3NhZ2VUeXBlIjoibWFya2V0aW5nIiwiY2FtcGFpZ25JRCI6ImUzYmJlZmZkLTZjYjItNGEwMy1iMjRhLTk1YzQ5ZjBkZjRlNCIsImNhbXBhaWduVmVyc2lvbklEIjoiZDlmMTMwNjAtZGVhNC00MTE1LTk5YzMtOGZjMTRjMWFiNTFiIiwiY2FtcGFpZ25BY3Rpb25JRCI6ImE1NmE0OTIxLWJjMjQtNGRjMC04Nzk3LTA2NmU4YzE0NTM5YiJ9LCJtZXNzYWdlUHJvZmlsZSI6eyJtZXNzYWdlUHJvZmlsZUlEIjoiMGI4NTYxMzAtNDZiNy00OTQ1LTgwYTAtZjM2MGUzMjhlMjllIiwiY2hhbm5lbCI6eyJfaWQiOiJodHRwczovL25zLmFkb2JlLmNvbS94ZG0vY2hhbm5lbHMvY29kZSIsIl90eXBlIjoiaHR0cHM6Ly9ucy5hZG9iZS5jb20veGRtL2NoYW5uZWwtdHlwZXMvY29kZSJ9fX0=",
                            "subPropositions": "W3siaWQiOiI1NzViZDY3My0yMTQ1LTQ2MzAtYjQ1Yy1iNDAwMGUxMzI1NmMiLCJzY29wZSI6Imh0dHBzOi8vd3d3LmFkb2JlLmNvbS9zYW4vcGxhY2VtZW50L2Zvb3RlciIsInNjb3BlRGV0YWlscyI6eyJkZWNpc2lvblByb3ZpZGVyIjoiRVhEIiwiY29ycmVsYXRpb25JRCI6IjNjYzRlZTAwLWJiNzYtNGVhYS05NGI2LTliOWJlMmM1M2UzYS0wIiwic3RyYXRlZ2llcyI6W3sic3RyYXRlZ3lJRCI6IjlhOTRjZjhjLTNkZjItNDE2NS1hMzRiLTIxNzBlMjg2YmUzMiIsInN0ZXAiOiJkZWNpc2lvblBvbGljeSJ9LHsic3RyYXRlZ3lJRCI6Imh0dHBzOi8vd3d3LmFkb2JlLmNvbS9zYW4vcGxhY2VtZW50L2Zvb3RlciIsInN0ZXAiOiJwbGFjZW1lbnQifV0sInJhbmsiOjEsImFjdGl2aXR5Ijp7ImlkIjoiZTNiYmVmZmQtNmNiMi00YTAzLWIyNGEtOTVjNDlmMGRmNGU0I2E1NmE0OTIxLWJjMjQtNGRjMC04Nzk3LTA2NmU4YzE0NTM5YiIsInByaW9yaXR5IjowLCJtYXRjaGVkU3VyZmFjZXMiOlsiaHR0cHM6Ly93d3cuYWRvYmUuY29tL3Nhbi9wbGFjZW1lbnQvZm9vdGVyIl19fSwiaXRlbXMiOltdfV0="
                        },
                        "rank": 1,
                        "activity": {
                            "id": "e3bbeffd-6cb2-4a03-b24a-95c49f0df4e4#a56a4921-bc24-4dc0-8797-066e8c14539b",
                            "priority": 0,
                            "matchedSurfaces": [
                                "https://www.adobe.com/san/placement/footer"
                            ]
                        }
                    },
                    "items": [
                        {
                            "id": "3913a28e-d33b-475b-9737-9f6de3940799",
                            "schema": "https://ns.adobe.com/personalization/html-content-item",
                            "data": {
                                "content": ""
                            }
                        }
                    ]
                }
            ],
            "type": "personalization:decisions",
            "eventIndex": 0
        }       
    ]
}
```

+++
