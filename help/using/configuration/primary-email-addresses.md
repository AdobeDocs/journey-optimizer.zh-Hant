---
solution: Journey Optimizer
product: journey optimizer
title: 變更主要電子郵件地址
description: 了解如何從設定檔服務中決定要使用的電子郵件地址。
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
keywords: 主要，執行，電子郵件，目標，設定檔，優化程式
exl-id: fe2f6516-7790-4501-a3a1-3d7cb94d7874
source-git-commit: b8065a68ed73102cb2c9da2c2d2675ce8e5fbaad
workflow-type: tm+mt
source-wordcount: '216'
ht-degree: 26%

---

# 更改主地址 {#change-primary-email}

>[!CONTEXTUALHELP]
>id="ajo_admin_execution_address"
>title="定義要使用的地址"
>abstract="當資料庫 (個人、專業等) 中有多個電子郵件地址或電話號碼時，您可以選擇優先傳送哪一個。"

>[!CONTEXTUALHELP]
>id="ajo_admin_execution_address_header"
>title="定義要使用的地址"
>abstract="編輯用於確定設定檔的電子郵件地址或電話號碼的欄位以優先傳送。"

當您定位設定檔時，資料庫中可能會有數個電子郵件地址或電話號碼（專業電子郵件地址、個人電話號碼等）。

使用 [!DNL Journey Optimizer]，您可以決定要從設定檔服務使用的電子郵件地址或電話號碼，以及在有數個地址時排定優先順序。 請依照下列步驟以執行此操作。

1. 存取  **[!UICONTROL 管道]** > **[!UICONTROL 一般]** > **[!UICONTROL 執行欄位]** 功能表。

   ![](assets/primary-address-execution-fields.png)

1. 依預設，目前用於判斷設定檔電子郵件地址和電話號碼的欄位會顯示在此畫面上。 按一下 **[!UICONTROL 編輯]** 來改變他們。

   ![](assets/primary-address.png)

1. 按一下您選取的目前欄位或編輯圖示，以選取新欄位。

   ![](assets/primary-address-edit.png)

1. 可用的電子郵件類型XDM欄位清單隨即顯示。 選取要使用的欄位。

   ![](assets/primary-address-select-field.png)

1. 按一下 **[!UICONTROL 儲存]** 確認您的選擇。

執行欄位會更新，現在會作為主要位址使用。

<!--1. You can also select an additional field to use as secondary email address. This allows you to determine which field to use if the primary field is empty for a profile. -->
