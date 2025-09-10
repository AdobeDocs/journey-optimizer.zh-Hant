---
solution: Journey Optimizer
product: journey optimizer
title: 變更執行地址
description: 瞭解如何從設定檔服務決定要使用的電子郵件地址。
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
keywords: 主要，執行，電子郵件，目標，設定檔，最佳化工具
exl-id: fe2f6516-7790-4501-a3a1-3d7cb94d7874
source-git-commit: c39a71da901b888ff440a1488658b577ff72cc32
workflow-type: tm+mt
source-wordcount: '522'
ht-degree: 27%

---

# 變更執行地址 {#change-primary-email}

>[!CONTEXTUALHELP]
>id="ajo_admin_execution_address"
>title="定義要使用的地址"
>abstract="當資料庫 (個人、專業等) 中有多個電子郵件地址或電話號碼時，您可以選擇優先傳送哪一個。"

>[!CONTEXTUALHELP]
>id="ajo_admin_execution_address_header"
>title="定義要使用的地址"
>abstract="編輯用於確定設定檔的電子郵件地址或電話號碼的欄位以優先傳送。"

當您定位設定檔時，資料庫中可能會提供數個電子郵件地址或電話號碼（專業電子郵件地址、個人電話號碼等）。

在這種情況下，[!DNL Journey Optimizer]會使用&#x200B;**[!UICONTROL 執行欄位]**&#x200B;來決定要優先使用設定檔服務中的電子郵件地址或電話號碼。

若要檢查目前預設使用的欄位，請存取&#x200B;**[!UICONTROL 管理]** > **[!UICONTROL 管道]** > **[!UICONTROL 一般設定]** > **[!UICONTROL 執行欄位]**&#x200B;選單。


![](assets/primary-address-execution-fields.png)

目前的值會用於沙箱層級的所有傳送。 您可以視需要更新這些欄位。

在大多數情況下，您將會全域變更執行欄位，並定義用於所有電子郵件或簡訊訊息的值。<!--[Learn how](#admin-settings)-->

<!--In some specific use cases only, you can override the value set globally and define a different value at the journey level. [Learn more](#journey-parameters)-->

## 更新管理設定 {#admin-settings}

若要在沙箱層級全域變更執行欄位，請遵循下列步驟。

1. 存取&#x200B;**[!UICONTROL 管道]** > **[!UICONTROL 一般設定]** > **[!UICONTROL 執行欄位]**&#x200B;功能表。

1. 按一下&#x200B;**[!UICONTROL 編輯]**&#x200B;以變更預設值。

   ![](assets/primary-address.png)

1. 按一下您選取的目前欄位或編輯圖示以選取新欄位。

   ![](assets/primary-address-edit.png)

1. 可用的電子郵件型別XDM欄位清單隨即顯示。 選取要使用的欄位。

   ![](assets/primary-address-select-field.png)

1. 按一下&#x200B;**[!UICONTROL 儲存]**&#x200B;以確認您的選擇。

執行欄位已更新，現在會作為主要地址使用。

<!--1. You can also select an additional field to use as secondary email address. This allows you to determine which field to use if the primary field is empty for a profile. -->

## 覆寫預設執行欄位 {#override-default-execution-address}

>[!CONTEXTUALHELP]
>id="ajo_journey_execution_address"
>title="定義自訂值"
>abstract="在某些特定情況下，您可以覆寫預設執行地址。使用欄位右側的「**啟用參數覆寫**」圖示定義自訂的主要地址。"
>additional-url="https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer/using/configuration/primary-email-addresses#journey-parameters" text="關於執行地址"

對於特定使用案例，您可以全域覆寫執行欄位設定，並在電子郵件設定層級或歷程層級定義不同的值。

覆寫此值可能很實用，例如：

* 測試電子郵件。 您可以新增自己的電子郵件地址：在您發佈歷程後，系統會傳送電子郵件給您。
* 傳送電子郵件給清單的訂閱者。 在[此使用案例](../building-journeys/message-to-subscribers-uc.md)中了解更多。

### 在電子郵件設定中

定義電子郵件通道設定時，您可以變更[一般設定](#admin-settings)中的預設執行欄位集。 [了解更多](../email/email-settings.md#execution-address)

在電子郵件設定中定義執行地址時，會用作主要地址並覆寫沙箱層級的一般設定。

### 在歷程引數中 {#journey-parameters}

將&#x200B;**[!UICONTROL 電子郵件]**&#x200B;或&#x200B;**[!UICONTROL 簡訊]**&#x200B;動作新增至[歷程](../email/create-email.md#create-email-journey-campaign)時，主要電子郵件地址會顯示在歷程進階引數下。

在某些特定內容中，您可以使用欄位右側的&#x200B;**[!UICONTROL 啟用引數覆寫]**&#x200B;圖示來覆寫此值。

![](assets/journey-enable-parameter-override.png)

>[!CAUTION]
>
>電子郵件地址覆寫僅用於特定使用案例。 在大多數情況下，您不需要變更電子郵件地址，因為&#x200B;**[!UICONTROL 執行欄位]**&#x200B;中定義為主要電子郵件的值才是應該使用的值。


