---
solution: Journey Optimizer
product: journey optimizer
title: 開始使用多語言內容
description: 進一步瞭解Journey Optimizer中的多語言內容
feature: Multilingual
topic: Content Management
role: User
level: Beginner
keywords: 開始使用、開始、內容、實驗
hide: true
hidefromtoc: true
source-git-commit: 3b1acd7ada0637ce22e360e6e1bb35921dde2315
workflow-type: tm+mt
source-wordcount: '769'
ht-degree: 1%

---

# 建立多語言內容 {#multilingual}

多語言功能可讓您在單一行銷活動中，輕鬆建立多種語言的內容。 透過此功能，您可以在編輯行銷活動時切換語言、簡化整個編輯流程，並提高有效管理多語言內容的能力。

## 建立地區設定 {#create-locale}

設定語言設定時，如 [建立您的語言設定](#language-settings) 區段，如果特定地區設定無法供多語言內容使用，您就可以彈性地使用 **[!UICONTROL 翻譯]** 功能表。

1. 從 **[!UICONTROL 管理]** 功能表，存取 **[!UICONTROL 頻道]**.

   翻譯功能表可讓您存取已啟動地區設定的清單。

1. 從 **[!UICONTROL 地區設定字典]** 標籤，按一下 **[!UICONTROL 新增地區設定]**.

   ![](assets/locale_1.png)

1. 從中選擇您的地區設定代碼 **[!UICONTROL 語言]** 清單和相關聯的 **[!UICONTROL 地區]**.

1. 按一下 **[!UICONTROL 儲存]** 以建立您的地區設定。

   ![](assets/locale_2.png)

## 建立語言設定 {#language-settings}

您可以在此段落中設定主要語言及其相關語言環境，以管理多語言內容。 您也可以選擇您要用來查閱與設定檔語言相關資訊的屬性

1. 從 **[!UICONTROL 管理]** 功能表，存取 **[!UICONTROL 頻道]**.

1. 在 **[!UICONTROL 語言設定]** 功能表，按一下 **[!UICONTROL 建立語言設定]**.

   ![](assets/multilingual-settings-1.png)

1. 輸入您的名稱 **[!UICONTROL 語言設定]**.

1. 選取 **[!UICONTROL 地區]** 與此設定相關聯。 您最多可以新增50個地區設定。

   如果 **[!UICONTROL 地區設定]** 遺失，您可以預先從 **[!UICONTROL 翻譯]** 功能表或API。 請參閱 [建立新的地區設定](#create-locale).

   ![](assets/multilingual-settings-2.png)

1. 從 **[!UICONTROL 傳送偏好設定]** 功能表，選取您要查詢以尋找設定檔語言資訊的屬性。

   ![](assets/multilingual-settings-3.png)

1. 按一下 **[!UICONTROL 編輯]** 位於您的 **[!UICONTROL 地區設定]** 以進一步個人化並新增 **[!UICONTROL 設定檔偏好設定]**.

   ![](assets/multilingual-settings-4.png)

1. 選取其他 **[!UICONTROL 地區]** 從設定檔偏好設定下拉式清單，然後按一下 **[!UICONTROL 新增設定檔]**.

1. 存取您的進階功能表 **[!UICONTROL 地區設定]** 以定義您的 **[!UICONTROL 主要地區設定]**，即預設語言（如果未指定設定檔屬性）。

   您也可以從此進階功能表刪除您的地區設定。

   ![](assets/multilingual-settings-5.png)

1. 按一下 **[!UICONTROL 提交]** 建立您的 **[!UICONTROL 語言設定]**.

<!--
1. Access the **[!UICONTROL Channel surfaces]** menu and create a new channel surface or select an existing one.

1. In the **[!UICONTROL Header parameters]** section, select the **[!UICONTROL Enable multilingual]** option.

1. Select your **[!UICONTROL Locales dictionary]** and add as many as needed.
-->

## 建立多語言行銷活動 {#create-multilingual-campaign}

1. 首先，根據您的需求建立和設定行銷活動。 [了解更多](../campaigns/create-campaign.md)

1. 導覽至 **[!UICONTROL 動作]** 功能表，然後選取 **[!UICONTROL 編輯內容]**.

   ![](assets/multilingual-campaign-1.png)

1. 建立或匯入原始內容，並視需要加以個人化。

1. 建立主要內容後，按一下 **[!UICONTROL 儲存]** 並返回campaign設定畫面。

   ![](assets/multilingual-campaign-2.png)

1. 按一下 **[!UICONTROL 新增語言]** 並選取您先前建立的 **[!UICONTROL 語言設定]**. [了解更多](#create-language-settings)

   ![](assets/multilingual-campaign-3.png)

1. 存取的進階設定 **[!UICONTROL 地區]** 功能表並選取 **[!UICONTROL 將主要複製到所有地區設定]**.

   ![](assets/multilingual-campaign-4.png)

1. 現在，您的主要內容會在您選取的整個過程中重複  **[!UICONTROL 地區]**，存取每個地區設定並按一下 **[!UICONTROL 編輯電子郵件內文]** 以翻譯您的內容。

   ![](assets/multilingual-campaign-5.png)

1. 您可以選擇停用或啟用語言環境， **[!UICONTROL 更多動作]** 您選取地區設定的功能表。

   ![](assets/multilingual-campaign-6.png)

1. 若要停用您的多語言設定，請按一下 **[!UICONTROL 新增語言]** 並選取您要保留為當地語言的語言。

   ![](assets/multilingual-campaign-7.png)

1. 按一下 **[!UICONTROL 檢閱以啟動]** 以顯示行銷活動的摘要。

   摘要可讓您視需要修改行銷活動，以及檢查是否有任何引數不正確或遺失。

1. 瀏覽您的多語言內容，檢視每種語言的轉譯。

   ![](assets/multilingual-campaign-8.png)

1. 檢查您的行銷活動是否已正確設定，然後按一下 **[!UICONTROL 啟動]**.

您的行銷活動現在已啟用。 行銷活動中設定的訊息會立即傳送，或於指定日期傳送。 請注意，您的行銷活動一旦上線，就無法修改。 若要重複使用內容，您可以複製Campaign。

傳送後，您可以在行銷活動報表中測量行銷活動的影響。

## 多語言行銷活動報告 {#multilingual-campaign-report}

全域報告，可從存取 **所有時間** 標籤，顯示至少兩小時前發生的事件，以及所選時段內的封面事件。 行銷活動全域報告可透過以下直接從行銷活動存取： **[!UICONTROL 檢視報告]** 按鈕。

如需促銷活動報表中可用資料的詳細資訊，請參閱 [此頁面](../reports/campaign-global-report.md).

+++進一步瞭解多語言內容可用的不同量度和Widget。

![](assets/report_multilingual.png)

此 **[!UICONTROL 依語言的電子郵件傳送統計資料]** Widget會根據您的 **[!UICONTROL 地區]**：

* **[!UICONTROL 已傳遞]**：成功傳送的訊息數，與已傳送訊息總數相關。

* **[!UICONTROL 跳出數]**：與已傳送訊息總數相關的傳送和自動回訪處理期間累計的錯誤總數。

* **[!UICONTROL 錯誤]**：在傳送期間發生且無法傳送至設定檔的錯誤總數。

此 **[!UICONTROL 依語言的電子郵件追蹤統計資料]** widget包含您的傳遞適用的收件者活動可用資料，具體取決於您的 **[!UICONTROL 地區]**：

* **[!UICONTROL 取消訂閱]**：對取消訂閱連結的點按次數。

* **[!UICONTROL 開啟次數]**：訊息開啟的次數。

* **[!UICONTROL 點按次數]**：內容被點按的次數。
+++


<!--
# Create a multilingual journey {#create-multilingual-journey}

1. Create your journey with a Delivery and personalize your content as needed.
1. From your delivery action, click Edit content.
1. Click Add languages.

# Translation project/ Create translation project:

1. From the Translation projects menu, click Create project.
1. Type-in a Name and Description.
1. Select the Source locale.
1. Click Add language to access the menu and define the languages for your translation project.
1. Select from the list your Target locale(s) and choose which Translation provider you want to use.
1. Click Add language when you finished linking your Target locale with the correct Translation provider.
1. Click Save.
1. From the Advanced menu of your Translation project, you can choose to Edit, deactive or delete it.
-->
