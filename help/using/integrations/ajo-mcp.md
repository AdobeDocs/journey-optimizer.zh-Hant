---
solution: Journey Optimizer
product: journey optimizer
title: 使用MCP使用者端(Beta)
description: 瞭解如何使用MCP伺服器將Adobe Journey Optimizer連線至MCP使用者端
feature: Integrations
topic: Content Management, Artificial Intelligence
badge: label="Beta" type="Informative"
role: User, Developer
level: Beginner, Intermediate
subfeature_v2: []
feature_v2: id: fe96aceb-8194-4a8a-a6b0-75302d02804d
source-git-commit: 7ced44f92f816d83d9a9ad667b4322dcb5930741
workflow-type: tm+mt
source-wordcount: 1369
ht-degree: 1%

---

# 使用MCP使用者端 {#ajo-mcp}

>[!BEGINSHADEBOX]

**在此頁面上：**&#x200B;取得[!DNL Adobe Journey Optimizer] MCP伺服器的逐步總覽 — 從模型內容通訊協定基本概念與支援的使用者端，到可用的工具、範例提示、設定先決條件、連線步驟以及常見問題的解答。

>[!ENDSHADEBOX]

[!DNL Adobe Journey Optimizer] MCP整合可讓您使用純語言提示來查詢行銷活動、歷程和優惠方案，而不需要撰寫API呼叫或導覽產品熒幕。 此頁面說明整合的運作方式、您可以執行哪些操作，以及如何開始使用。

>[!AVAILABILITY]
>
>[!DNL Adobe Journey Optimizer] MCP伺服器目前可在&#x200B;**Claude Web**、**Claude Desktop**&#x200B;和&#x200B;**Cursor**&#x200B;中使用。 未來版本將新增對其他MCP相容應用程式的支援。

## Beta、安全性和法律注意事項 {#mcp-notices}

**Beta檔案通知：**&#x200B;此檔案涵蓋Beta功能，不構成最終檔案。 此處描述的內容與Beta版本有關，且在正式發行前可能會有所變更。 Adobe不對本檔案的完整性或準確性發表任何宣告。

藉由使用Adobe Journey Optimizer MCP Server (Beta) (「Beta」)，您在此確認Beta係依&#x200B;**「原樣」提供，並無任何保固**。 Adobe沒有義務維護、更正、更新、變更、修改或以其他方式支援Beta。 建議您謹慎使用，切勿依賴這類Beta及/或隨附資料的正確運作或效能。 Beta視為Adobe的機密資訊。 任何「意見回饋」（有關Beta的資訊，包括但不限於您在使用Beta時遇到的問題或缺陷、建議、改進和建議）會在此指派給Adobe，包括所有權利、標題，以及對此等意見回饋的興趣。

>[!WARNING]
>
>模型內容通訊協定(MCP)是一種新興的開放原始碼標準，可能會帶來安全性或可靠性風險。 Adobe MCP伺服器整合和相關檔案係依「現況」提供，不提供任何形式的保證。
>
>將MCP使用者端或伺服器連線至Adobe產品是客戶選擇的設定。 客戶應負責評估任何MCP整合的安全性和適用性。 Adobe對於因設定錯誤、誤用MCP、協力廠商實作中的漏洞，或透過啟用MCP的工作流程執行的意外動作所引起的問題，概不負責。
>
>為了降低風險，Adobe鼓勵您在有效使用之前在沙箱環境中測試整合，並在確認或依賴之前，仔細檢閱及驗證所有MCP啟動的動作和回應。

## 什麼是模型內容通訊協定？ {#mcp-overview}

行銷和客戶體驗團隊越來越仰賴聊天式應用程式和開發人員工具（例如Anthropic Claude、OpenAI ChatGPT、Cursor和Microsoft Copilot Studio）來簡化日常工作。 這些應用程式支援&#x200B;**模型內容通訊協定(MCP)**，這是開放標準，可讓應用程式以統一的方式將後端工具公開給大型語言模型(LLM)。

[!DNL Adobe Journey Optimizer]現在提供MCP伺服器，直接在任何MCP相容應用程式中呈現行銷活動和沙箱作業。 透過[!DNL Adobe Journey Optimizer] MCP整合，不同的角色可以圍繞相同的協調流程資料共同作業，而不需要針對[!DNL Adobe Journey Optimizer] REST API撰寫查詢，或導覽多個UI熒幕。 客戶可以用對話方式描述他們的意圖，讓LLM叫用適當的MCP工具。

## 主要功能 {#mcp-capabilities}

[!DNL Adobe Journey Optimizer] MCP伺服器可讓您直接從AI助理檢查、摘要和疑難排解行銷活動、歷程和選件。 所有作業都是&#x200B;**唯讀** — MCP伺服器介面會擷取API作為純語言回答，因此您可以：

* **瞭解歷程邏輯** — 取得任何歷程分支、條件和動作的人類可讀摘要。
* **立即取得行銷活動可見度** — 以簡單語言詢問行銷活動狀態和管道設定，並立即取得解答，無需瀏覽功能表或手動提取報告。
* **提早發現問題** — 表面停止行銷活動、孤立草稿，以及您提出要求的頻道設定問題，讓您的團隊可以快速採取行動。
* **圍繞即時資料共同作業** — 行銷人員、行銷活動經理和利害關係人可以透過其AI助理查詢相同的即時[!DNL Adobe Journey Optimizer]資料，更輕鬆地保持一致、決定和移動。
* **稽核您的協調流程產品組合** — 檢閱行銷活動的完整狀態，而不剖析JSON或跨產品畫面跳躍。

## 可用的工具 {#mcp-tools}

[!DNL Adobe Journey Optimizer] MCP伺服器公開下列工具：

**行銷活動工具**

| 工具 | 說明 |
|---|---|
| **列出行銷活動** | 瀏覽您的[!DNL Adobe Journey Optimizer]行銷活動。 支援依狀態篩選（草稿、即時、已停止、已完成）。 |
| **取得行銷活動** | 依ID擷取特定行銷活動的完整詳細資料和設定，包括對象目標定位、排程、頻道和內容設定。 |
| **列出頻道設定** | 檢視電子郵件、簡訊、推播或WhatsApp頻道的表面預設集和品牌設定。 |

**歷程工具**

| 工具 | 說明 |
|---|---|
| **取得所有歷程** | 瀏覽您[!DNL Adobe Journey Optimizer]沙箱中的所有歷程。 |
| **取得歷程** | 依ID擷取特定歷程的完整詳細資料，包括其分支、條件和動作。 |
| **視覺化您的歷程** | 使用互動式工具呈現您的歷程，以便以視覺化方式探索其結構和流程。 |

>[!NOTE]
>
>所有工具均為唯讀。 目前的Beta版本不支援寫入操作（建立、更新或刪除物件）。

## 使用案例 {#mcp-use-cases}

下列範例顯示如何使用自然語言與[!DNL Adobe Journey Optimizer] MCP伺服器互動：

| 目標 | 範例提示 |
|---|---|
| **行銷活動和歷程概觀** | 顯示我所有的Journey Optimizer行銷活動/歷程/在Journey Optimizer中設定了多少行銷活動/歷程？ |
| **狀態稽核** | 哪些行銷活動/歷程目前為上線？ /列出任何暫停或停止的行銷活動/歷程。 |
| **行銷活動和歷程詳細資料** | 取得行銷活動[ID]的完整詳細資料/逐步說明行銷活動[ID]中設定的所有專案。 /取得歷程[ID]的完整詳細資料/逐步說明歷程[ID]中設定的所有專案。 |
| **對象和目標** | 行銷活動/歷程[ID]以哪些對象為目標？ /促銷活動/歷程[ID]上設定了哪些適用性規則？ |
| **排程與時間** | 行銷活動[ID]何時排定執行？ /行銷活動[ID]是單次傳送還是週期性？ |
| **疑難排解** | 為什麼行銷活動[ID]可能不會傳送？ /檢閱行銷活動[ID]的設定是否有任何問題。 |
| **頻道設定** | 我的沙箱中有哪些管道預設集可用？ /顯示我的所有電子郵件通道設定。 |
| **管道稽核** | 哪些管道設定遺漏或不完整？ /我跨所有管道有多少管道設定？ |

## 先決條件 {#mcp-prerequisites}

在將[!DNL Adobe Journey Optimizer] MCP伺服器連線到您的MCP使用者端之前，請確定下列事項：

* 您有使用中的[!DNL Adobe Journey Optimizer]授權。
* 您可以存取支援的MCP相容應用程式（目前為Claude Web、Claude Desktop或Cursor）。
* 您在[!DNL Adobe Journey Optimizer]中擁有檢視行銷活動、歷程和優惠方案的必要許可權。

## 連線[!DNL Adobe Journey Optimizer] MCP伺服器 {#mcp-connect}

>[!NOTE]
>
>這項整合位於Beta中。

您可以透過您偏好的MCP使用者端連線[!DNL Adobe Journey Optimizer] MCP伺服器，包括&#x200B;**Claude Web**、**Claude Desktop**&#x200B;和&#x200B;**Cursor**。

**透過MCP使用者端連線**

在MCP使用者端中設定MCP伺服器時，請使用下列伺服器端點URL：

`https://ajo-mcp.adobe.io/mcp`

**透過Claude Web或Claude Desktop連線**

若要在Claude Web或Claude Desktop中設定MCP伺服器，請移至&#x200B;**聯結器**&#x200B;並選取&#x200B;**Adobe Journey Optimizer**。

## 常見問題 {#mcp-faq}

+++支援哪些MCP使用者端？

[!DNL Adobe Journey Optimizer] MCP伺服器目前可用於&#x200B;**Claude Web**、**Claude Desktop**&#x200B;和&#x200B;**Cursor**。 未來版本可能會新增對其他MCP相容應用程式的支援。
+++

+++我可以透過MCP存取哪些[!DNL Adobe Journey Optimizer]物件？

您可以存取行銷活動、歷程、選件和沙箱資訊。 操作是唯讀的（擷取API）；目前版本不支援寫入操作。
+++

+++我需要開發人員存取權才能使用[!DNL Adobe Journey Optimizer] MCP伺服器嗎？

不會。 MCP伺服器是專為行銷和技術人員所設計。 行銷人員可以在任何支援的MCP使用者端中使用自然語言提示與其互動，而開發人員也可以在支援MCP的開發人員工具中使用它。
+++

+++我的資料是否傳送給MCP使用者端提供者？

當您提交提示時，MCP使用者端可能會傳送相關內容（包括MCP伺服器傳回的[!DNL Adobe Journey Optimizer]資料）到其模型以進行處理。 在連線到生產資料之前，請檢閱MCP使用者端提供者的隱私權和資料處理原則。
+++

+++我在[!DNL Adobe Journey Optimizer]中需要哪些許可權？

您要查詢的物件（行銷活動、歷程或選件）至少需要&#x200B;**檢視**&#x200B;許可權。 不需要寫入許可權，因為MCP伺服器只會執行讀取作業。 如果您不確定目前的存取層級，請連絡您的[!DNL Adobe Journey Optimizer]系統管理員。
+++

+++我可以在沙箱環境中使用MCP伺服器嗎？

可以。 MCP伺服器遵循您的[!DNL Adobe Journey Optimizer]沙箱設定。 您可以在提示中指定沙箱，或使用限定於特定沙箱的憑證連線，以查詢沙箱專屬的資料。
+++

