---
title: 建立網站體驗
description: 瞭解如何在Journey Optimizer中編寫網頁及編輯其內容
feature: Web Channel
topic: Content Management
role: User
level: Beginner
exl-id: e28c038b-49ed-4685-bfe6-514116eb0711
source-git-commit: 27447578dad6bd2612989d79cd0dc8ddbe78d629
workflow-type: tm+mt
source-wordcount: '833'
ht-degree: 17%

---

# 建立網站體驗 {#create-web}

[!DNL Journey Optimizer]可讓您透過傳入的網頁行銷活動，個人化您提供給客戶的網頁體驗。

>[!CAUTION]
>
>目前在 [!DNL Journey Optimizer]，您只能使用&#x200B;**行銷活動**&#x200B;建立網路體驗。

[透過此影片瞭解如何建立網路行銷活動](#video)

## 建立網路行銷活動 {#create-web-campaign}

>[!CONTEXTUALHELP]
>id="ajo_web_surface"
>title="定義網頁表面"
>abstract="網頁表面可能會和單個頁面 URL 或多個頁面相符，可讓您在一個或多個網頁上傳遞內容修改。"

>[!CONTEXTUALHELP]
>id="ajo_web_surface_rule"
>title="建置頁面比對規則"
>abstract="頁面比對規則可以找出符合相同規則的多個 URL - 例如，如果您想要將變更套用到整個網站的主要橫幅，或新增顯示在網站所有產品頁面的頂端影像。"

若要透過行銷活動開始建立您的Web體驗，請遵循下列步驟。

>[!NOTE]
>
>如果這是您第一次建立網頁體驗，請務必遵循[本章節](web-prerequisites.md)所說明的先決條件。

1. 建立行銷活動。 [了解更多](../campaigns/create-campaign.md)

1. 選取&#x200B;**[!UICONTROL Web]**&#x200B;動作。

1. 定義網頁表面。

   >[!NOTE]
   >
   >Web介面是由要傳送內容的URL所識別的Web屬性。 它可以比對單一頁面URL或多個頁面，讓您在一或多個網頁間提供修改內容。

   如果您只想將變更套用至單一頁面，可以輸入&#x200B;**[!UICONTROL 頁面URL]**。

   ![](assets/web-campaign-surface.png)

1. 或者，您可以建置符合規則&#x200B;]**的**[!UICONTROL &#x200B;頁面，以符合相同規則的多個URL為目標 — 例如，如果您想要將變更套用至整個網站的主圖橫幅，或新增顯示在網站所有產品頁面上的最上層影像。

   若要這麼做，請選取&#x200B;**[!UICONTROL 符合規則]**&#x200B;的頁面，然後按一下&#x200B;**[!UICONTROL 建立規則]**。

   ![](assets/web-campaign-matching-rule.png)

1. 定義&#x200B;**[!UICONTROL 網域]**&#x200B;和&#x200B;**[!UICONTROL 頁面]**&#x200B;欄位的條件。

   例如，如果您想要編輯顯示在Luma網站所有女性產品頁面上的元素，請選取&#x200B;**[!UICONTROL 網域]** > **[!UICONTROL 開頭為]** > `luma`和&#x200B;**[!UICONTROL 頁面]** > **[!UICONTROL 包含]** > `women`。

   ![](assets/web-pages-matching-rule.png)

1. 儲存您的變更。規則會顯示在&#x200B;**[!UICONTROL 建立行銷活動]**&#x200B;畫面中。

   ![](assets/web-pages-matching-rule-example.png)

1. 定義網頁表面之後，請選取&#x200B;**[!UICONTROL 建立]**。

1. 完成步驟以建立網路行銷活動，例如行銷活動屬性、[對象](../audience/about-audiences.md)和[排程](../campaigns/create-campaign.md#schedule)。

   ![](assets/web-campaign-steps.png)

如需如何設定行銷活動的詳細資訊，請參閱[此頁面](../campaigns/get-started-with-campaigns.md)。

## 測試網路行銷活動 {#test-web-campaign}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_preview"
>title="預覽您的網頁體驗"
>abstract="取得您的網頁體驗的模擬。"

使用網頁設計工具[編寫您的網頁體驗](edit-web-content.md)後，您可以使用測試設定檔來預覽您修改的網頁。 如果您已插入個人化內容，您可以使用測試設定檔資料檢查此內容的顯示方式。

若要這麼做，請從網頁行銷活動編輯內容畫面或網頁設計工具按一下&#x200B;**[!UICONTROL 模擬內容]**，然後新增測試設定檔，以使用測試設定檔資料檢查您的網頁。

![](assets/web-designer-preview.png)

您也可以在預設瀏覽器中開啟測試網址，或複製測試URL以貼到任何瀏覽器中。 這可讓您與團隊和利害關係人共用連結，這些利害關係人將能夠在行銷活動上線之前在任何瀏覽器中預覽新的網頁體驗。

>[!NOTE]
>
>複製測試URL時，顯示的內容是在[!DNL Journey Optimizer]中產生內容模擬時所使用之測試設定檔的個人化內容。

有關如何選取測試設定檔及預覽內容的詳細資訊，請參閱[內容管理](../content-management/preview-test.md)區段。

## 啟動網站行銷活動 {#activate-web-campaign}

一旦您定義了[網頁行銷活動設定](#configure-web-campaign)，並視需要使用[網頁設計工具](edit-web-content.md#work-with-web-designer)編輯您的內容後，您就可以檢閱並啟用您的網頁行銷活動。 請遵循下列步驟。

<!--
>[!NOTE]
>
>You can also preview your web campaign content before activating it. [Learn more](#test-web-campaign)-->

1. 從您的網路行銷活動中，選取&#x200B;**[!UICONTROL 檢閱以啟動]**。

1. 視需要檢查並編輯內容、屬性、表面、對象和排程。

1. 選取&#x200B;**[!UICONTROL 啟動]**。

   ![](assets/web-campaign-activate.png)

   >[!NOTE]
   >
   >按一下&#x200B;**[!UICONTROL 啟用]**&#x200B;後，最多可能需要15分鐘的時間才能讓網站上的網路行銷活動變更上線。

您的網路行銷活動會採用&#x200B;**[!UICONTROL 即時]**&#x200B;狀態，現在選定的對象可以看到。 行銷活動的每位收件者都可以看到您使用[!DNL Journey Optimizer]網頁設計工具新增至網站的修改。

>[!NOTE]
>
>如果您為網路行銷活動定義排程，在到達開始日期和時間之前，其狀態為&#x200B;**[!UICONTROL 已排程]**。
>
>如果您啟動某個網路行銷活動，其影響的頁面與另一個已上線的行銷活動相同，則所有變更將會套用至您的網頁。

在[本節](../campaigns/review-activate-campaign.md)中進一步瞭解啟用行銷活動。

## 停止網站行銷活動 {#stop-web-campaign}

當網站行銷活動上線時，您可以停止它以防止您的對象看到您的修改。 請遵循下列步驟。

1. 從清單中選取即時行銷活動。

1. 從頂端功能表選取&#x200B;**[!UICONTROL 停止行銷活動]**。

   ![](assets/web-campaign-stop.png)

1. 您所定義的對象將看不到您所新增的修改。

>[!NOTE]
>
>網路行銷活動停止後，您就無法再次編輯或啟動它。 您只能複製該檔案並啟動複製的促銷活動。

## 操作說明影片{#video}

以下影片說明如何建立網站行銷活動、設定其屬性、檢閱及發佈。

>[!VIDEO](https://video.tv.adobe.com/v/3418800/?quality=12&learn=on)