---
product: journey optimizer
title: inSegment
description: 瞭解中的函式
feature: Journeys
role: Developer
level: Experienced
keywords: inSegment，函式，運算式，歷程
exl-id: 8417af75-6e97-4ad4-86b4-3ecd264a5560
version: Journey Orchestration
feature_v2: []
subfeature_v2: []
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 521
ht-degree: 2%

---

# inSegment {#inSegment}

檢查個人是否屬於指定對象。

>[!NOTE]
>
>您最多可以擷取100個對象。

對象名稱必須是字串常數。 它不能是欄位參考或運算式。

對象是在[Adobe Experience Platform](https://platform.adobe.com/audience/overview)中定義。 運算式編輯器提供自動完成的對象清單。

對象可以有兩種狀態：

* 已實現：實體符合區段定義的資格。
* 已退出：實體正在退出區段定義。

只有具有&#x200B;**已實現**&#x200B;對象參與狀態的個人才會被視為對象的成員。 如需如何評估對象的詳細資訊，請參閱[Segmentation Service檔案](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html?lang=zh-Hant#interpret-segment-results)。

`inSegment('segmentName') == true`表示您擁有segmentMembership且狀態為entered/existing。

`inSegment('segmentName') == false`表示您擁有退出狀態的segmentMembership。

## 類別

Adobe Experience Platform

## 函式語法

`inSegment(<parameter>)`

## 參數

| 參數 | 說明 | 類型 |
|--- |--- |--- |
| 區段 | 對象名稱 | `<string>` |

## 簽章與傳回的型別

`inSegment(<string>)`

傳回布林值。

## 範例

`inSegment("men over 50")`

說明：

如果歷程執行個體中的個人是名為「超過50歲的男性」的Adobe Experience Platform對象的一部分，則函式會傳回&#x200B;**[!UICONTROL true]**，否則會傳回&#x200B;**[!UICONTROL false]**。

+++ AI知識參考

本節包含結構化知識，用於支援與本主題相關的解譯、擷取和問答。

如需完整瞭解，此資訊應結合本頁的檔案。 兩者皆非獨立來源；頁面說明功能，本節提供額外內容，以協助去除術語、意圖、適用性和限制條件的歧義。

* **TL；DR：**&#x200B;此頁面會記錄舊版`inSegment`函式，此函式會檢查歷程設定檔是否屬於已命名的Adobe Experience Platform對象，並傳回布林值。

**意圖：**
* 使用`inSegment`檢查設定檔是否為具名對象的作用中成員
* 使用`inSegment('name') == true`確認在歷程條件中實現的（作用中）對象成員資格
* 使用`inSegment('name') == false`確認已退出（非使用中）的對象成員資格

**字彙表：**
* **已實現**：對象參與狀態，表示實體目前符合區段定義&#x200B;*（產品特定）*&#x200B;的資格
* **已退出**：對象參與狀態，表示實體正在離開或已經離開區段定義&#x200B;*（產品特定）*

**護欄：**
* 單一歷程中最多可擷取100個對象
* 對象名稱必須是字串常數；欄位參考和運算式不支援作為引數

**術語：**
* 正式名稱：inSegment — 首字母縮寫：none — 變體：inAudience （目前偏好函式）
* 同義字： &quot;inSegment&quot; = &quot;audience membership check&quot; （舊版）
* 請勿混淆：「inSegment」（舊版/已棄用的函式）≠「inAudience」（目前建議的函式）
* 請勿混淆：「已實現」（作用中成員）≠「已退出」（不再是成員）

**常見問題集：**
* **問：`inSegment`與`inAudience`之間有何差異？** — `inSegment`是舊版函式名稱；`inAudience`是目前建議的函式。 兩者都會檢查對象成員資格，但`inAudience`具有更完整的檔案，包括護欄和傳播時間詳細資料。
* **問：`inSegment('name') == true`是什麼意思？**  — 這表示設定檔具有「已實現」segmentMembership狀態，即個人是對象的作用中成員。
* **問：我可以傳遞動態運算式作為對象名稱嗎？**  — 否，對象名稱必須是字串常數；不支援欄位參考和運算式。
* **問：在一個歷程中可以評估多少個對象？**  — 單一歷程中最多可擷取100個對象。

+++
