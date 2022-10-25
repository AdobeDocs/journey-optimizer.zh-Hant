---
title: 開始使用傳遞優惠方案 API
description: 進一步了解可提供個人化優惠方案的API。
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 7bc1a4ec-113c-4af7-b549-ee17b843b818
source-git-commit: bf738ebac09d5c852872a8ea85f6532ad9d4222d
workflow-type: tm+mt
source-wordcount: '442'
ht-degree: 6%

---

# 開始使用傳遞優惠方案 API {#about-decisioning-apis}

您可以使用 **決策** 或 **Edge Decisioning** API。 此外， **批次決策** API可讓您透過一次呼叫，將選件傳送至指定區段中的所有設定檔。 區段中每個設定檔的選件內容會放置於Adobe Experience Platform資料集中，供自訂批次工作流程使用。

在本頁面中，您將會找到 **決策** 和 **Edge Decisioning** API。 雖然兩者皆可讓您傳送優惠方案給客戶，但建議您使用 **Edge Decisioning** 盡可能針對傳入使用案例使用API，並確保平台上的延遲和輸送量更佳。

|  | 請求數/秒 | 延遲性 |
|---|---|---|
| 決策 API | 2000年 | &lt;500ms |
| 邊緣決策 API | 5000 | &lt;250ms |

如需如何使用API的詳細資訊，請參閱以下章節：
* [決策 API](decisioning-api.md)
* [邊緣決策 API](edge-decisioning-api.md)
* [批次決策 API](batch-decisioning-api.md)

## Edge Decisioning API功能 {#edge}

**體驗事件和決策請求的不重複請求**

有了Edge Decisioning API，您可以在單一請求中傳送體驗事件本身與決策請求，不必有兩個不同的請求。

例如，如果客戶造訪您的網站，請求將包含體驗事件（客戶造訪頁面），然後取回優惠方案以填入造訪的頁面。

**內容資料儲存至Adobe Experience Platform**

內容資料是指您只在想要傳回選件時才知道的資料。 例如，購買文章的顏色、購買時的天氣等。

使用Edge Decisioning API請求傳遞內容資料時，資料會儲存至Adobe Experience Platform設定檔中，供日後重複使用。

>[!NOTE]
>
>若要儲存內容資料，您必須設定專用的XDM架構。

## 決策API功能 {#decisioning}

下列功能僅可搭配Decisioning API使用。 如果您需要運用其中一項來符合需求，請使用Decisioning API。 否則，建議您使用Edge Decisioning API。

* **體驗事件**:運用體驗事件來建立決策規則。
* **選件內容與特性**:您可以選擇不使用專用選項傳回選件的內容和特性。
* **選件中繼資料**:啟用選項以傳回選件的中繼資料。
* **合併策略**:與與沙箱相關聯的合併原則，請在請求中使用不同的合併原則。
* **決策事件與頻率限定**:封鎖決策事件，避免被發生的任何頻率限定計算。
* **重複命題**:啟用不刪除重複命題的選項。
