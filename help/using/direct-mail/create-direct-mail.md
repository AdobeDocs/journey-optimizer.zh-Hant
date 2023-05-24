---
title: 建立直郵郵件
description: 瞭解如何在Journey Optimizer建立直郵郵件
feature: Overview
topic: Content Management
role: User
level: Beginner
keywords: 直接郵件，郵件，促銷活動
hide: true
hidefromtoc: true
exl-id: 6b438268-d983-4ab8-9276-c4b7de74e6bd
badge: label="Beta" type="Informative"
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '517'
ht-degree: 11%

---

# 建立直郵郵件 {#create-direct}

>[!CONTEXTUALHELP]
>id="ajo_direct_mail"
>title="直接郵件建立"
>abstract="在排程的行銷活動中建立直接郵件訊息，並設計直接郵件提供者向您的客戶傳送郵件所需的解壓縮檔案。"

>[!BEGINSHADEBOX]

本文件提供下列內容：

* **[建立直接郵件](create-direct-mail.md)**
* [設定直接郵件](direct-mail-configuration.md)

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>直郵目前可作為專用測試版使用，並且可能會經常更新，恕不另行通知。

直接郵件是一種離線渠道，允許您個性化和生成直接郵件提供商向客戶發送郵件所需的提取檔案。

建立直郵時，Journey Optimizer會生成包含所有目標配置檔案和所選資料（例如，郵政地址、配置檔案屬性）的檔案。 您的直郵提供商將能夠檢索該檔案並處理實際發送。

只能在計畫的市場活動上下文中建立直接郵件消息。 它們不能用於API觸發的市場活動或旅程。

>[!IMPORTANT]
>
>在發送直郵郵件之前，請確保已配置：
>
>1. A [檔案路由配置](../direct-mail/direct-mail-configuration.md#file-routing-configuration) 指定抽取檔案應上載和儲存的伺服器，
>1. A [直接郵件消息表](../direct-mail/direct-mail-configuration.md#direct-mail-surface) 將引用檔案路由配置。


## 建立直郵郵件 {#create}

建立和發送直郵郵件的步驟如下：

1. 建立新的計畫市場活動，選擇 **[!UICONTROL 直郵]** 頁籤。 [瞭解如何建立直郵表面](../direct-mail/direct-mail-configuration.md#direct-mail-surface)

   ![](assets/direct-mail-campaign.png)

1. 按一下 **[!UICONTROL 建立]** 然後定義有關市場活動的基本資訊（名稱、說明）。 [瞭解如何配置市場活動](../campaigns/create-campaign.md)

1. 按一下 **[!UICONTROL 編輯內容]** 按鈕，來配置要發送給直接郵件提供商的抽取檔案。

1. 在 **[!UICONTROL 檔案名]** 的子菜單。

   有時候，您可能需要在解壓縮檔案的開頭或結尾新增資訊。要執行此操作，請使用 **[!UICONTROL 注釋]** 欄位，然後指定是否要將注釋作為頁眉或頁腳包含。

   <!--Click on the button to the right of the Output file field and enter the desired label. You can use personalization fields, content blocks and dynamic text (see Defining content). For example, you can complete the label with the delivery ID or the extraction date.-->

   ![](assets/direct-mail-properties.png)

1. 使用左側區域定義要作為列顯示到抽取檔案中的資訊：

   1. 按一下 **[!UICONTROL 添加]** 按鈕來添加新列，然後從清單中選擇它。

   1. 在 **[!UICONTROL 格式]** 中，指定列的標籤，然後使用 [表達式編輯器](../personalization/personalization-build-expressions.md)。

      ![](assets/direct-mail-content.png)

   1. 要使用選定列對抽取檔案進行排序，請切換 **[!UICONTROL 排序依據]** 的上界。 的 **[!UICONTROL 排序依據]** 表徵圖將顯示在檔案結構中列標籤的旁邊。

1. 重複這些步驟，以根據需要添加多列以生成抽取檔案。 請注意，最多可以添加50列。

   通過選擇列並按一下 **[!UICONTROL 刪除]** 按鈕 **[!UICONTROL 格式]** 的子菜單。

   ![](assets/direct-mail-complete.png)

1. 定義直郵內容後，請完成市場活動的配置。

   當市場活動開始時，抽取檔案將自動生成並導出到您在 [檔案路由配置](../direct-mail/direct-mail-configuration.md)。
