---
solution: Journey Optimizer
product: journey optimizer
title: 更改執行地址
description: 了解如何從設定檔服務中決定要使用的電子郵件地址。
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
keywords: 主要，執行，電子郵件，目標，設定檔，優化程式
exl-id: fe2f6516-7790-4501-a3a1-3d7cb94d7874
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '431'
ht-degree: 23%

---

# 更改執行地址 {#change-primary-email}

>[!CONTEXTUALHELP]
>id="ajo_admin_execution_address"
>title="定義要使用的地址"
>abstract="當資料庫 (個人、專業等) 中有多個電子郵件地址或電話號碼時，您可以選擇優先傳送哪一個。"

>[!CONTEXTUALHELP]
>id="ajo_admin_execution_address_header"
>title="定義要使用的地址"
>abstract="編輯用於確定設定檔的電子郵件地址或電話號碼的欄位以優先傳送。"

當您定位設定檔時，資料庫中可能會有數個電子郵件地址或電話號碼（專業電子郵件地址、個人電話號碼等）。

在這種情況下， [!DNL Journey Optimizer] uses **[!UICONTROL 執行欄位]** 以決定要優先從設定檔服務使用的電子郵件地址或電話號碼。

若要檢查預設目前使用的欄位，請存取 **[!UICONTROL 管理]** > **[!UICONTROL 管道]** > **[!UICONTROL 一般]** > **[!UICONTROL 執行欄位]** 功能表。

![](assets/primary-address-execution-fields.png)

目前的值會用於沙箱層級的所有傳送。 您可以視需要更新這些欄位。

在大多數情況下，您會全域變更執行欄位，並定義應用於所有電子郵件或簡訊的值。 <!--[Learn how](#admin-settings)-->

<!--In some specific use cases only, you can override the value set globally and define a different value at the journey level. [Learn more](#journey-parameters)-->

## 更新管理設定 {#admin-settings}

若要在沙箱層級全域變更執行欄位，請遵循下列步驟。

1. 存取  **[!UICONTROL 管道]** > **[!UICONTROL 一般]** > **[!UICONTROL 執行欄位]** 功能表。

1. 按一下 **[!UICONTROL 編輯]** 來更改預設值。

   ![](assets/primary-address.png)

1. 按一下您選取的目前欄位或編輯圖示，以選取新欄位。

   ![](assets/primary-address-edit.png)

1. 可用的電子郵件類型XDM欄位清單隨即顯示。 選取要使用的欄位。

   ![](assets/primary-address-select-field.png)

1. 按一下 **[!UICONTROL 儲存]** 確認您的選擇。

執行欄位會更新，現在會作為主要位址使用。

<!--1. You can also select an additional field to use as secondary email address. This allows you to determine which field to use if the primary field is empty for a profile. -->

## 覆寫歷程參數中的值 {#journey-parameters}

僅限特定使用案例，您可以覆寫全域設定的執行欄位，並在歷程層級定義不同的值，尤其是電子郵件通道。

新增 **[!UICONTROL 電子郵件]** 動作 [歷程](../email/create-email.md#create-email-journey-campaign)，主要電子郵件地址會顯示在歷程進階參數下。

在某些特定內容中，您可以使用 **[!UICONTROL 啟用參數覆蓋]** 表徵圖 **[!UICONTROL 地址]** 欄位。

![](assets/journey-enable-parameter-override.png)

>[!CAUTION]
>
>電子郵件地址覆寫僅用於特定使用案例。 在大多數情況下，您不需要變更電子郵件地址，因為&#x200B;**[!UICONTROL 執行欄位]**&#x200B;中定義為主要電子郵件的值才是應該使用的值。 

覆寫此值可能會很有用，例如：

* 測試電子郵件。 您可以新增自己的電子郵件地址：在您發佈歷程後，會傳送電子郵件給您。
* 傳送電子郵件給清單的訂閱者。 在[此使用案例](../building-journeys/message-to-subscribers-uc.md)中了解更多。
