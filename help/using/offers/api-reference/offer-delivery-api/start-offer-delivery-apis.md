---
title: 開始提供交付API
description: 瞭解有關可提供個性化服務的API的更多資訊。
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 7bc1a4ec-113c-4af7-b549-ee17b843b818
source-git-commit: bf738ebac09d5c852872a8ea85f6532ad9d4222d
workflow-type: tm+mt
source-wordcount: '442'
ht-degree: 4%

---

# 開始提供交付API {#about-decisioning-apis}

您可以使用 **決定** 或 **邊判別** API。 此外， **批決策** API允許您在一次調用中向給定段中的所有配置檔案提供優惠。 段中每個配置檔案的提供內容都放在Adobe Experience Platform資料集中，在該資料集中可用於自定義批處理工作流。

在本頁中，您將找到與 **決定** 和 **邊判別** API。 雖然這兩種方法都允許您向客戶提供優惠，但我們建議使用 **邊判別** API（盡可能）用於入站使用情形，並確保在您的平台上實現更好的延遲和吞吐量。

|  | 請求數/秒 | 延遲性 |
|---|---|---|
| 決策 API | 2000 | &lt;500ms |
| 邊緣決策 API | 5000 | &lt;250ms |

有關如何使用API的詳細資訊，請參閱以下各節：
* [決策 API](decisioning-api.md)
* [邊緣決策 API](edge-decisioning-api.md)
* [批次決策 API](batch-decisioning-api.md)

## 邊緣判定API功能 {#edge}

**對體驗事件和決策請求的唯一請求**

使用邊緣決定API，您可以將體驗事件本身與決策請求一起發送到一個請求中，而不是有兩個不同的請求。

例如，如果客戶訪問您的網站，請求將包括體驗事件（客戶訪問該頁面），並返回優惠以填充訪問的頁面。

**將上下文資料儲存到Adobe Experience Platform**

上下文資料是指您在希望返回優惠時才知道的資料。 例如，購買物品的顏色、購買時的天氣等。

當使用邊緣決策API請求傳遞上下文資料時，資料被儲存到Adobe Experience Platform配置檔案中，從而允許將來重新使用。

>[!NOTE]
>
>要儲存上下文資料，需要配置專用的XDM架構。

## 確定API功能 {#decisioning}

下面列出的功能僅適用於決策API。 如果您需要利用其中一個來滿足您的要求，請使用決策API。 否則，我們建議使用邊決策API。

* **體驗事件**:利用體驗事件構建決策規則。
* **提供內容和特性**:您可以選擇不使用專用選項返回優惠的內容和特徵。
* **提供元資料**:啟用選項以返回聘用的元資料。
* **合併策略**:在請求中使用與與沙盒關聯的合併策略不同的合併策略。
* **判斷事件和頻率上限**:塊判斷事件不會被發生的任何頻率上限計數。
* **重複命題**:啟用選項，以不消除重複命題。
