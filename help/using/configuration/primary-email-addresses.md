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
source-git-commit: 953adc90278a984ca8b73576274ec73fe98c08a1
workflow-type: tm+mt
source-wordcount: '484'
ht-degree: 16%

---

# 變更執行地址 {#change-primary-email}

>[!CONTEXTUALHELP]
>id="ajo_admin_execution_address"
>title="定義要使用的地址"
>abstract="當資料庫 (個人、專業等) 中有多個電子郵件地址或電話號碼時，您可以選擇優先傳送哪一個。"

>[!CONTEXTUALHELP]
>id="ajo_admin_execution_address_header"
>title="定義要使用的地址"
>abstract="編輯用於確定輪廓的電子郵件地址或電話號碼的欄位以優先傳送。"

當您定位設定檔時，資料庫中可能會提供數個電子郵件地址或電話號碼（專業電子郵件地址、個人電話號碼等）。

在這種情況下，[!DNL Journey Optimizer]會使用&#x200B;**[!UICONTROL 執行欄位]**&#x200B;來決定要優先使用設定檔服務中的電子郵件地址或電話號碼。

若要檢查目前預設使用的欄位，請存取&#x200B;**[!UICONTROL 管理]** > **[!UICONTROL 管道]** > **[!UICONTROL 一般設定]** > **[!UICONTROL 執行欄位]**&#x200B;功能表。

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

## 覆寫預設值 {#override-default-execution-address}

### 在電子郵件設定中

定義電子郵件通道設定時，您可以變更在沙箱層級設定的預設執行欄位。 [了解更多](../email/email-settings.md#execution-address)

在設定層級定義執行位址時，執行位址會當作主要位址使用，並覆寫沙箱層級的一般設定。

### 在歷程引數中 {#journey-parameters}

僅針對特定使用案例，您可以全域覆寫執行欄位設定，並在歷程層級定義不同的值，尤其是電子郵件頻道。

將&#x200B;**[!UICONTROL 電子郵件]**&#x200B;動作新增至[歷程](../email/create-email.md#create-email-journey-campaign)時，主要電子郵件地址會顯示在歷程進階引數下。

在某些特定內容中，您可以使用&#x200B;**[!UICONTROL 位址]**&#x200B;欄位右側的&#x200B;**[!UICONTROL 啟用引數覆寫]**&#x200B;圖示來覆寫此值。

![](assets/journey-enable-parameter-override.png)

>[!CAUTION]
>
>電子郵件地址覆寫僅用於特定使用案例。 在大多數情況下，您不需要變更電子郵件地址，因為&#x200B;**[!UICONTROL 執行欄位]**&#x200B;中定義為主要電子郵件的值才是應該使用的值。

覆寫此值可能很實用，例如：

* 測試電子郵件。 您可以新增自己的電子郵件地址：發佈歷程後，會傳送電子郵件給您。
* 傳送電子郵件給清單的訂閱者。 在[此使用案例](../building-journeys/message-to-subscribers-uc.md)中了解更多。

