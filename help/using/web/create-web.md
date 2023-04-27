---
title: 建立網站體驗
description: 了解如何在Journey Optimizer中撰寫網頁及編輯其內容
feature: Web Channel
topic: Content Management
role: User
level: Beginner
exl-id: e28c038b-49ed-4685-bfe6-514116eb0711
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '662'
ht-degree: 8%

---

# 建立網站體驗 {#create-web}

[!DNL Journey Optimizer] 可讓您透過傳入的網頁行銷活動，個人化您提供給客戶的網頁體驗。

>[!CAUTION]
>
>目前在 [!DNL Journey Optimizer] 您只能使用 **行銷活動**.

[透過此影片了解如何建立網頁行銷活動](#video)

## 建立網路行銷活動 {#create-web-campaign}

>[!CONTEXTUALHELP]
>id="ajo_web_surface"
>title="定義網路表面"
>abstract="網頁表面可能會和單次頁面 URL 或多個頁面相符，可讓您在一個或多個網頁上傳遞內容修改。"

>[!CONTEXTUALHELP]
>id="ajo_web_surface_rule"
>title="建置頁面符合規則"
>abstract="頁面比對規則可讓您鎖定符合相同規則的多個URL，例如，如果您想要將變更套用至整個網站的主圖橫幅，或新增顯示在網站所有產品頁面上的頂端影像。"

若要開始透過促銷活動建立您的網頁體驗，請遵循下列步驟。

>[!NOTE]
>
>如果這是您第一次建立網頁體驗，請務必遵循 [本節](web-prerequisites.md).

1. 建立行銷活動. [了解更多](../campaigns/create-campaign.md)

1. 選取 **[!UICONTROL Web]** 動作。

1. 定義網路表面.

   >[!NOTE]
   >
   >Web表面是由要傳送內容的URL所識別的Web屬性。 它可以比對單一頁面URL或多個頁面，讓您可以在一或多個網頁間提供修改。

   您可以輸入 **[!UICONTROL 頁面URL]** 如果您只想將變更套用至單一頁面。

   ![](assets/web-campaign-surface.png)

1. 或者，您可以建置 **[!UICONTROL 頁面符合規則]** 若要鎖定符合相同規則的多個URL，例如，如果您想要將變更套用至整個網站的主圖橫幅，或新增顯示在網站所有產品頁面上的最上層影像。

   若要這麼做，請選取 **[!UICONTROL 頁面符合規則]** 按一下 **[!UICONTROL 建立規則]**.

   ![](assets/web-campaign-matching-rule.png)

1. 定義 **[!UICONTROL 網域]** 和 **[!UICONTROL 頁面]** 欄位。

   例如，如果您想要編輯Luma網站上所有女性產品頁面上顯示的元素，請選取 **[!UICONTROL 網域]** > **[!UICONTROL 開頭為]** > `luma` 和 **[!UICONTROL 頁面]** > **[!UICONTROL 包含]** > `women`.

   ![](assets/web-pages-matching-rule.png)

1. 儲存您的變更。規則會顯示在 **[!UICONTROL 建立行銷活動]** 螢幕。

   ![](assets/web-pages-matching-rule-example.png)

1. 定義網格曲面後，選取 **[!UICONTROL 建立]**.

1. 完成建立網頁促銷活動的步驟，例如促銷活動屬性、 [對象](../segment/about-segments.md)，和 [排程](../campaigns/create-campaign.md#schedule).

   ![](assets/web-campaign-steps.png)

如需如何設定促銷活動的詳細資訊，請參閱 [本頁](../campaigns/get-started-with-campaigns.md).

## 啟動網路行銷活動 {#activate-web-campaign}

在您定義 [網站行銷活動設定](#configure-web-campaign) 而且您可以視需要使用 [網頁設計工具](author-web.md)，您可以檢閱並啟動您的網頁行銷活動。 請遵循下列步驟。

>[!NOTE]
>
>您也可以先預覽網頁行銷活動內容，再加以啟用。 [了解更多](author-web.md#test-web-campaign)

1. 從您的網路行銷活動中，選取 **[!UICONTROL 審核以激活]**.

1. 視需要檢查和編輯內容、屬性、表面、對象和排程。

1. 選擇 **[!UICONTROL 啟動]**.

   ![](assets/web-campaign-activate.png)

   >[!NOTE]
   >
   >按一下 **[!UICONTROL 啟動]**，則網站上最多可能需要15分鐘才會上線提供網頁促銷活動變更。

您的網路行銷活動會 **[!UICONTROL 即時]** 狀態和現在會顯示給選取的對象。 行銷活動的每個收件者都可以透過 [!DNL Journey Optimizer] 網頁設計工具。

>[!NOTE]
>
>如果您定義了Web促銷活動的排程，則其具有 **[!UICONTROL 已排程]** 狀態直到達到開始日期和時間為止。
>
>如果您啟用的網頁促銷活動與另一個已上線的促銷活動影響相同的頁面，所有變更都會套用至您的網頁。

進一步了解如何在 [本節](../campaigns/review-activate-campaign.md).

## 停止網路行銷活動 {#stop-web-campaign}

當網頁行銷活動上線時，您可以停止行銷活動，以防止對象看到您的修改。 請遵循下列步驟。

1. 從清單中選取已上線的促銷活動。

1. 從頂端功能表中，選取 **[!UICONTROL 停止促銷活動]**.

   ![](assets/web-campaign-stop.png)

1. 您新增的修改將不再對您定義的對象顯示。

>[!NOTE]
>
>一旦停止Web促銷活動，您就無法再次編輯或啟動它。 您只能複製它並啟動複製的促銷活動。

## 作法影片{#video}

以下影片說明如何建立Web促銷活動、設定其屬性、檢閱及發佈。

>[!VIDEO](https://video.tv.adobe.com/v/3418800/?quality=12&learn=on)