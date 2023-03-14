---
title: Visual Editing Helper 擴充功能
description: 探索Visual Editing Helper Chrome擴充功能，其可讓您在Journey Optimizer中製作和預覽網頁
feature: Web Channel
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: f4a0ec45-d624-4f80-b888-42e5987cdc4f
badge: label="Beta" type="Informity"
source-git-commit: 160e4ce03d3be975157c30fbe511875a85b00551
workflow-type: tm+mt
source-wordcount: '409'
ht-degree: 18%

---

# Visual Editing Helper 擴充功能 {#visual-editing-helper}

>[!BEGINSHADEBOX]

本檔案提供下列內容：

* [開始使用網路頻道](get-started-web.md)
* [建立網站體驗](create-web.md)
* [製作網頁](author-web.md)
* **[Visual Editing Helper 擴充功能](visual-editing-helper.md)**
* [網站報告](web-report.md)

>[!ENDSHADEBOX]

為了快速撰寫和預覽您的網頁體驗，Google Chrome的Adobe Experience Cloud Visual Editing Helper瀏覽器擴充功能可讓您在Adobe中妥善地載入網站 [!DNL Journey Optimizer] 網頁設計工具。

## 安裝Visual Editing Helper擴充功能 {#install-visual-editing-helper}

要獲取並安裝Visual Editing Helper瀏覽器擴展，請執行以下步驟。

1. 從Google Chrome線上應用程式商店，導覽至 [Adobe Experience Cloud Visual Editing Helper](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target="_blank"} 瀏覽器擴充功能。

1. 按一下「**[!UICONTROL 新增至 Chrome]** > **[!UICONTROL 新增擴充功能]**」。

1. 在中建立網頁頻道行銷活動 [!DNL Journey Optimizer]. [了解作法](author-web.md#create-web-campaign)

1. 開啟 [!DNL Journey Optimizer] 網頁設計工具，開始編寫您的網頁體驗。 [了解更多](author-web.md)

1. 按一下對應的圖示，以確定Chrome瀏覽器工具列中的Visual Editing Helper瀏覽器擴充功能已啟用。

   ![](assets/web-visual-editing-extension.png)

Adobe Experience Cloud Visual Editing Helper現在會在 [!DNL Journey Optimizer] 網頁設計工具來強化製作功能。

擴充功能沒有任何條件式設定，且會自動處理所有設定，包括SameSite Cookie設定。

>[!NOTE]
>
>某些網站可能無法可靠地在 [!DNL Journey Optimizer] Web設計器，原因如下：
>
> * 網站的安全性原則過於嚴格。
> * 網站架設在 iFrame 中。
> * 客戶的 QA 或暫存網站無法供外部世界使用 (網站僅供內部使用)。


## 疑難排解

使用Adobe時 [!DNL Journey Optimizer] 網頁設計工具，如果您嘗試載入無法載入的網站，會顯示訊息建議您安裝 [Visual Editing Helper瀏覽器擴充功能](#install-visual-editing-helper).

如果網站上尚未實作Adobe Experience Platform Web SDK，網頁設計器中會顯示訊息，建議您安裝Visual Editing Helper瀏覽器擴充功能並實作 [Web SDK](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=zh-Hant){target="_blank"}.

如果網站無法載入或意外運作，可能的修正是在瀏覽器中接受網站上的Cookie，再嘗試以Adobe載入 [!DNL Journey Optimizer].

針對驗證下的頁面，如果登入頁面無法載入，或嘗試登入後您仍未登入，請嘗試先登入瀏覽器的其他索引標籤，然後在Adobe中載入網站 [!DNL Journey Optimizer] 網頁設計工具。
