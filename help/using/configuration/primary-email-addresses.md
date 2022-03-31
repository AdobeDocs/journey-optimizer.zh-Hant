---
title: '更改主電子郵件地址 '
description: 瞭解如何從配置檔案服務中確定要使用的電子郵件地址。
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: fe2f6516-7790-4501-a3a1-3d7cb94d7874
source-git-commit: 5071de634c9dbb13908d3190fe1157831c372c7d
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 7%

---

# 更改主電子郵件地址 {#change-primary-email}

當您針對配置檔案時，資料庫中可能有幾個電子郵件地址（個人、專業電子郵件地址等）。

與 [!DNL Journey Optimizer]，您可以確定從配置檔案服務使用的電子郵件地址，並在幾個地址可用時確定優先順序。 請依照下列步驟以執行此操作。

1. 存取 **[!UICONTROL Channels]** > **[!UICONTROL General]** > **[!UICONTROL Executions fields]** 功能表。

   ![](assets/primary-address-execution-fields.png)

1. 預設情況下，當前用於確定配置檔案電子郵件地址的欄位將顯示在此螢幕上。 按一下 **[!UICONTROL Edit]** 來改變它。

   ![](assets/primary-address.png)

1. 按一下當前欄位或編輯表徵圖以選擇新欄位。

   ![](assets/primary-address-edit.png)

1. 將顯示可用電子郵件類型XDM欄位的清單。 選擇要使用的欄位。

   ![](assets/primary-address-field.png)

1. 按一下 **[!UICONTROL Save]** 確認你的選擇。

   ![](assets/primary-address-save.png)

   執行欄位已更新，現在將用作主地址。

<!--1. You can also select an additional field to use as secondary email address. This allows you to determine which field to use if the primary field is empty for a profile. -->
