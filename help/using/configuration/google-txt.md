---
title: 將GoogleTXT記錄添加到子域
description: 瞭解如何將GoogleTXT記錄添加到子域
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 311eb2d1-e445-43e6-bc2c-c6288b637f47
source-git-commit: d568480005d9b4aad5982c26184a5add0be6c83a
workflow-type: tm+mt
source-wordcount: '205'
ht-degree: 21%

---

# 將GoogleTXT記錄添加到子域 {#google-txt-record}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_google"
>title="GoogleTXT記錄"
>abstract="為確保成功將電子郵件發送到Gmail地址，您可以將特殊的Google站點驗證TXT記錄添加到子域，以確保已驗證。"

TXT 記錄是一種 DNS 記錄，用於提供關於網域的文字資訊，可由外部來源讀取。

為了確保電子郵件的最佳傳遞和成功的傳遞， [!DNL Journey Optimizer] 允許您向子域添加特殊的Google站點驗證TXT記錄，以確保已驗證。

>[!CAUTION]
>
> 只有子域具有 **[!UICONTROL Success]** 狀態。 有關子域狀態的詳細資訊，請參閱 [此部分](access-subdomains.md)。

要將GoogleTXT記錄添加到子域，請執行以下步驟：

1. 從 **[!UICONTROL Channels]** / **[!UICONTROL Subdomains]** 的子菜單。

1. 在 **[!UICONTROL Google txt record]** 部分，輸入從 [Google工作區](https://support.google.com/a/answer/183895){target=&quot;_blank&quot;<!--G Suite Admin tools-->，然後按一下 **[!UICONTROL Save]**。

   ![](assets/subdomain-google-txt.png)

1. 新增 TXT 記錄後，該記錄必須獲得 Google 驗證。要執行此操作，請導航至 [Google工作區](https://support.google.com/a/answer/183895){target=&quot;_blank&quot;<!--G Suite Admin tools-->，然後啟動驗證步驟。
