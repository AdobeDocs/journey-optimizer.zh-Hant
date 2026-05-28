---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: 開始使用傳遞產品建議 API
description: 深入瞭解可用於提供個人化優惠的API。
badge: label="舊版" type="Informative"
feature: Decision Management, API
topic: Integrations
role: Developer
level: Experienced
exl-id: 7bc1a4ec-113c-4af7-b549-ee17b843b818
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/qo18m5-seH1yCaxQPJ7hmXDSkBPex-PgYKMQRsOBhBw
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2id: ad78185d-8f79-40ad-9bad-cbde74af74ee
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
subfeature_v2: id: a7a194a0-75e2-4913-8a83-14714fbf68e6id: eb547372-2a95-4d13-b0fd-f720c9895880id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 488
ht-degree: 7%

---

# 開始使用傳遞產品建議 API {#about-decisioning-apis}

>[!TIP]
>
>[!DNL Adobe Journey Optimizer] 的新決策功能「決策」現在可透過程式碼型體驗和電子郵件管道使用！ [了解更多](../../../experience-decisioning/gs-experience-decisioning.md)

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
