---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: 開始使用傳遞產品建議 API
description: 深入瞭解可用於提供個人化優惠的API。
feature: Decision Management, API
topic: Integrations
role: Developer
level: Experienced
exl-id: 7bc1a4ec-113c-4af7-b549-ee17b843b818
version: Journey Orchestration
source-git-commit: d6a9a8a392f0492aa6e4f059198ce77b6b2cd962
workflow-type: tm+mt
source-wordcount: '469'
ht-degree: 4%

---

# 開始使用傳遞產品建議 API {#about-decisioning-apis}

您可以使用&#x200B;**決策**&#x200B;或&#x200B;**Edge決策** API來傳遞優惠方案。 此外，**批次決策** API可讓您透過一次呼叫，將優惠傳送給指定對象中的所有設定檔。 對象中每個設定檔的選件內容都會放在Adobe Experience Platform資料集中，可用於自訂批次工作流程。

在此頁面中，您會找到&#x200B;**決策**&#x200B;與&#x200B;**Edge決策** API所提供之特定功能的相關資訊。 雖然兩者皆可讓您為客戶提供優惠方案，但我們建議儘可能針對傳入使用案例使用&#x200B;**Edge Decisioning** API，並確保平台上有更好的延遲和輸送量。

如需如何使用API的詳細資訊，請參閱下列章節：

* [決策 API](decisioning-api.md)
* [邊緣決策 API](edge-decisioning-api.md)
* [批次決策 API](batch-decisioning-api.md)

## Edge決策API功能 {#edge}

**體驗事件和決策要求的唯一要求**

使用Edge Decisioning API，您可以連同決策請求一起在單一請求中傳送體驗事件本身，而不是有兩個不同的請求。

例如，如果客戶造訪您的網站，要求會包含體驗事件（客戶造訪的頁面），並取得選件以填入造訪的頁面。

**將內容資料儲存至Adobe Experience Platform**

內容資料是指您只知道想要回某個優惠方案的資料。 例如，所購買文章的顏色、購買時的天氣等。

使用Edge Decisioning API請求傳遞內容資料時，資料會儲存至Adobe Experience Platform設定檔中，以便日後重複使用。

>[!NOTE]
>
>為了儲存內容資料，您需要設定專用的XDM結構描述。

**頻率限定計數器更新**

如果您的部分優惠已啟用頻率上限以定義其上限計數重設的頻率，則計數器會更新，且在3秒內可在Edge Decisioning API決定中使用。 [瞭解如何將限制新增至優惠方案](../../offer-library/add-constraints.md)

## 決策API功能 {#decisioning}

下列功能僅適用於Decisioning API。 如果您需要運用其中一種來滿足需求，請使用決策API。 否則，我們建議您使用Edge Decisioning API。

* **優惠方案內容和特性**：您可以選擇不使用專用選項來傳回優惠方案的內容和特性。
* **優惠方案中繼資料**：啟用選項以傳回優惠方案的中繼資料。
* **合併原則**：在您的要求中使用與沙箱關聯的不同合併原則。
* **決策事件和頻率上限**：封鎖決策事件不會被任何發生的頻率上限計算在內。
* **重複的主張**：啟用不刪除重複主張的選項。
