---
title: 建立新的直接郵件訊息
description: 瞭解如何在Journey Optimizer中建立直接郵件訊息
feature: Overview
topic: Content Management
role: User
level: Beginner
keywords: 直接郵件、訊息、行銷活動
exl-id: 6b438268-d983-4ab8-9276-c4b7de74e6bd
source-git-commit: 804ff95d2a19601d036e739bb1d5a629930247b9
workflow-type: tm+mt
source-wordcount: '720'
ht-degree: 8%

---

# 建立新的直接郵件訊息 {#create-direct}

>[!CONTEXTUALHELP]
>id="ajo_direct_mail"
>title="直接郵件建立"
>abstract="在排程的行銷活動中建立直接郵件訊息，並設計直接郵件提供者向您的客戶傳送郵件所需的解壓縮檔案。"

若要建立直接郵件訊息、建立排程的行銷活動，並設定解壓縮檔案。 直接郵件提供者需要此檔案，才能將郵件傳送給您的客戶。

>[!IMPORTANT]
>
>在建立直接郵件訊息之前，請確定您已設定：
>
>1. A [檔案路由設定](../direct-mail/direct-mail-configuration.md#file-routing-configuration) 會指定應該上傳及儲存解壓縮檔案的伺服器，
>1. A [直接郵件訊息表面](../direct-mail/direct-mail-configuration.md#direct-mail-surface) 會參照檔案路由組態。


## 建立直接郵件行銷活動{#create-dm-campaign}

若要建立直接郵件行銷活動，請遵循下列步驟：

1. 建立新的排程行銷活動，然後選擇 **[!UICONTROL 直接郵件]** 作為動作。

1. 選取 **[!UICONTROL 直接郵件表面]** 使用並按一下 **[!UICONTROL 建立]**. [瞭解如何建立直接郵件表面](direct-mail-configuration.md#direct-mail-surface).

   ![](assets/direct-mail-campaign.png){width="800" align="center"}

1. 在 **[!UICONTROL 屬性]** 區段，編輯您的行銷活動 **[!UICONTROL 標題]** 和 **[!UICONTROL 說明]**.

1. 若要定義目標對象，請按一下 **[!UICONTROL 選取對象]** 按鈕，然後從可用的Adobe Experience Platform受眾中選擇。 [了解更多](../audience/about-audiences.md)。

   >[!IMPORTANT]
   >
   >目前，受眾選擇限製為3百萬個設定檔。 如有要求，您的Adobe代表可自行解除此限制。

1. 在 **[!UICONTROL 身分名稱空間]** 欄位中，選取適當的名稱空間以識別所選對象中的個人。 [了解更多](../event/about-creating.md#select-the-namespace)。

   ![](assets/direct-mail-campaign-properties.png){width="800" align="center"}

1. 行銷活動可以排程為特定日期，或設定為定期重複。 瞭解如何設定 **[!UICONTROL 排程]** 中的行銷活動 [本節](../campaigns/create-campaign.md#schedule).

您現在可以開始設定擷取檔案，以傳送給直接郵件提供者。

## 設定擷取檔案 {#extraction-file}

>[!CONTEXTUALHELP]
>id="ajo_direct_mail_data_fields"
>title="資料欄位"
>abstract="新增並設定要在擷取檔案中顯示的欄和資訊，直接郵件提供商需要這些欄和資訊來傳送郵件給您的客戶。 您最多可以新增50欄。"

>[!CONTEXTUALHELP]
>id="ajo_direct_mail_formatting"
>title="擷取檔案格式"
>abstract="對於每個欄位，指定標籤和資訊以使用「運算式編輯器」顯示。 <br/><br/> 此 <b>排序依據：</b> 選項可讓您使用選取的欄位來排序解壓縮檔案的欄。"

1. 設定要在擷取檔案中顯示的欄和資訊：

   1. 按一下 **[!UICONTROL 新增]** 按鈕以建立新欄。

   1. 此 **[!UICONTROL 格式化]** 窗格會顯示在右側，讓您設定選取的欄。 指定 **[!UICONTROL 標籤]** 欄的範本。

   1. 在 **[!UICONTROL 資料]** 欄位中，選擇要顯示的設定檔屬性， [運算式編輯器](../personalization/personalization-build-expressions.md).

   1. 若要使用欄排序解壓縮檔案，請選取該欄並開啟 **[!UICONTROL 排序依據：]** 選項。 此 **[!UICONTROL 排序方式]** 圖示會顯示在中的欄標籤旁 **[!UICONTROL 資料欄位]** 區段。







直接郵件供應商需要擷取檔案，才能傳送郵件給您的客戶。 若要定義解壓縮檔案組態，請執行下列步驟：

1. 在行銷活動設定畫面中，按一下 **[!UICONTROL 編輯內容]** 按鈕以設定擷取檔案內容。

1. 調整解壓縮檔案屬性：

   1. 指定所需的 **[!UICONTROL 檔案名稱]** 用於擷取檔案。

   1. 選擇性地啟用 **[!UICONTROL 附加時間戳記以匯出檔案名稱]** 選項，如果要將自動時間戳記新增至指定的檔案名稱。

   1. 有時候，您可能需要在解壓縮檔案的開頭或結尾新增資訊。若要這麼做，請使用 **[!UICONTROL 附註]** 欄位，然後指定是否要以頁首或頁尾形式包含附註。

      ![](assets/direct-mail-properties.png){width="800" align="center"}

1. 設定要在擷取檔案中顯示的欄和資訊：

   1. 按一下 **[!UICONTROL 新增]** 按鈕以建立新欄。

   1. 此 **[!UICONTROL 格式化]** 窗格會顯示在右側，讓您設定選取的欄。 指定 **[!UICONTROL 標籤]** 欄的範本。

   1. 在 **[!UICONTROL 資料]** 欄位中，選擇要顯示的設定檔屬性， [運算式編輯器](../personalization/personalization-build-expressions.md).

   1. 若要使用欄排序解壓縮檔案，請選取該欄並開啟 **[!UICONTROL 排序依據：]** 選項。 此 **[!UICONTROL 排序方式]** 圖示會顯示在中的欄標籤旁 **[!UICONTROL 資料欄位]** 區段。

      ![](assets/direct-mail-content.png){width="800" align="center"}

   1. 重複這些步驟，視需要為解壓縮檔案新增任意數目的欄。 請注意，您最多可以新增50欄。

      若要變更欄的位置，請將其拖放到中所需的位置 **[!UICONTROL 資料欄位]** 區段。 若要刪除欄，請選取該欄並按一下 **[!UICONTROL 移除]** 中的按鈕 **[!UICONTROL 格式化]** 窗格。

您現在可以測試直接郵件訊息，並將其傳送給您的對象。 [瞭解如何測試和傳送直接郵件訊息](test-send-direct-mail.md)
