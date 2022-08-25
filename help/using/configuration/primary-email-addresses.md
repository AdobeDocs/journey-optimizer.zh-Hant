---
title: '更改主電子郵件地址 '
description: 瞭解如何從配置檔案服務中確定要使用的電子郵件地址。
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: fe2f6516-7790-4501-a3a1-3d7cb94d7874
source-git-commit: 5abcef4ff057bb351abaafbf4dcb99e1ab61c6a9
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 5%

---

# 更改主地址 {#change-primary-email}

>[!CONTEXTUALHELP]
>id="ajo_admin_execution_address"
>title="定義要使用的地址"
>abstract="當資料庫中有多個地址（個人地址、專業地址等）可用時，您可以選擇發送的優先順序。"

當您針對配置檔案時，資料庫中可能會有幾個電子郵件地址或電話號碼（專業電子郵件地址、個人電話號碼等）。

與 [!DNL Journey Optimizer]，您可以確定從配置檔案服務中使用的電子郵件地址或電話號碼，並確定當有多個地址可用時的優先順序。 請依照下列步驟以執行此操作。

1. 存取 **[!UICONTROL Channels]** > **[!UICONTROL General]** > **[!UICONTROL Executions fields]** 功能表。

   ![](assets/primary-address-execution-fields.png)

1. 預設情況下，當前用於確定此螢幕上配置檔案的電子郵件地址和電話號碼的欄位。 按一下 **[!UICONTROL Edit]** 來改變他們。

   ![](assets/primary-address.png)

1. 按一下所選的當前欄位或編輯表徵圖以選擇新欄位。

   ![](assets/primary-address-edit.png)

1. 將顯示可用電子郵件類型XDM欄位的清單。 選擇要使用的欄位。

   ![](assets/primary-address-select-field.png)

1. 按一下 **[!UICONTROL Save]** 確認你的選擇。

執行欄位已更新，現在將用作主地址。

<!--1. You can also select an additional field to use as secondary email address. This allows you to determine which field to use if the primary field is empty for a profile. -->
