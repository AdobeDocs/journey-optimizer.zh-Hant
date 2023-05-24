---
title: 建立網站體驗
description: 瞭解如何在Journey Optimizer建立網頁並編輯其內容
feature: Web Channel
topic: Content Management
role: User
level: Beginner
exl-id: e28c038b-49ed-4685-bfe6-514116eb0711
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '662'
ht-degree: 20%

---

# 建立網站體驗 {#create-web}

[!DNL Journey Optimizer] 允許您通過入站Web活動個性化您向客戶提供的Web體驗。

>[!CAUTION]
>
>目前在 [!DNL Journey Optimizer]，您只能使用&#x200B;**行銷活動**&#x200B;建立網路體驗。

[瞭解如何在此視頻中建立Web活動](#video)

## 建立網路行銷活動 {#create-web-campaign}

>[!CONTEXTUALHELP]
>id="ajo_web_surface"
>title="定義網路表面"
>abstract="網頁表面可能會和單次頁面 URL 或多個頁面相符，可讓您在一個或多個網頁上傳遞內容修改。"

>[!CONTEXTUALHELP]
>id="ajo_web_surface_rule"
>title="建置頁面符合規則"
>abstract="頁面符合規則可以找出符合相同規則的多個 URL - 例如，如果您想要將變更套用到整個網站的主要橫幅，或新增顯示在網站所有產品頁面的頂端影像。"

要通過活動開始構建您的Web體驗，請執行以下步驟。

>[!NOTE]
>
>如果這是您第一次建立網頁體驗，請務必遵循[本章節](web-prerequisites.md)所說明的必要條件。

1. 建立行銷活動. [了解更多](../campaigns/create-campaign.md)

1. 選擇 **[!UICONTROL Web]** 操作。

1. 定義網路表面.

   >[!NOTE]
   >
   >Web曲面是由內容將在其中傳遞的URL標識的Web屬性。 它可以匹配單頁URL或多頁，允許您跨一個或多個網頁進行修改。

   您可以輸入 **[!UICONTROL 頁面URL]** 的子菜單。

   ![](assets/web-campaign-surface.png)

1. 或者你可以 **[!UICONTROL 頁面匹配規則]** 以針對匹配同一規則的多個URL，例如，如果要將更改應用於整個網站的英雄橫幅，或添加顯示在網站所有產品頁面上的頂部影像。

   要執行此操作，請選擇 **[!UICONTROL 頁面匹配規則]** 按一下 **[!UICONTROL 建立規則]**。

   ![](assets/web-campaign-matching-rule.png)

1. 為 **[!UICONTROL 域]** 和 **[!UICONTROL 頁面]** 的子菜單。

   例如，如果要編輯Luma網站所有女性產品頁面上顯示的元素，請選擇 **[!UICONTROL 域]** > **[!UICONTROL 開始於]** > `luma` 和 **[!UICONTROL 頁面]** > **[!UICONTROL 包含]** > `women`。

   ![](assets/web-pages-matching-rule.png)

1. 儲存您的變更。規則顯示在 **[!UICONTROL 建立市場活動]** 的上界。

   ![](assets/web-pages-matching-rule-example.png)

1. 定義網格曲面後，選取 **[!UICONTROL 建立]**。

1. 完成建立Web市場活動的步驟，如市場活動屬性、 [觀眾](../segment/about-segments.md), [計畫](../campaigns/create-campaign.md#schedule)。

   ![](assets/web-campaign-steps.png)

有關如何配置市場活動的詳細資訊，請參閱 [此頁](../campaigns/get-started-with-campaigns.md)。

## 激活Web市場活動 {#activate-web-campaign}

一旦你定義了 [Web活動設定](#configure-web-campaign) 並根據需要使用 [web設計器](author-web.md)，您可以複查並激活您的Web活動。 按照以下步驟操作。

>[!NOTE]
>
>您還可以在激活Web促銷活動內容之前預覽它。 [了解更多](author-web.md#test-web-campaign)

1. 從Web市場活動中，選擇 **[!UICONTROL 複查以激活]**。

1. 如果需要，請檢查並編輯內容、屬性、表面、受眾和時間表。

1. 選擇 **[!UICONTROL 激活]**。

   ![](assets/web-campaign-activate.png)

   >[!NOTE]
   >
   >按一下後 **[!UICONTROL 激活]**，網站上的網站活動更改最多需要15分鐘。

您的Web活動將 **[!UICONTROL 實況]** 狀態，現在對選定的受眾可見。 您活動的每個收件人都可以使用 [!DNL Journey Optimizer] web設計器。

>[!NOTE]
>
>如果為Web促銷活動定義了計畫，則 **[!UICONTROL 計畫]** 直到達到開始日期和時間。
>
>如果激活一個與另一個已進行的市場活動影響相同頁面的Web市場活動，則所有更改都將應用於您的網頁。

瞭解有關在中激活市場活動的更多資訊 [此部分](../campaigns/review-activate-campaign.md)。

## 停止Web活動 {#stop-web-campaign}

當Web活動正在進行時，您可以停止它以防止觀眾看到您的修改。 按照以下步驟操作。

1. 從清單中選擇即時市場活動。

1. 從頂部菜單中，選擇 **[!UICONTROL 停止市場活動]**。

   ![](assets/web-campaign-stop.png)

1. 您添加的修改將不再對您定義的受眾可見。

>[!NOTE]
>
>停止Web市場活動後，您將不能再編輯或激活它。 您只能複製並激活複製的市場活動。

## 操作說明影片{#video}

以下視頻顯示如何建立Web市場活動、配置其屬性、查看和發佈。

>[!VIDEO](https://video.tv.adobe.com/v/3418800/?quality=12&learn=on)