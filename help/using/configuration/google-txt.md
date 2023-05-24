---
solution: Journey Optimizer
product: journey optimizer
title: 將GoogleTXT記錄添加到子域
description: 瞭解如何將GoogleTXT記錄添加到子域
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
keywords: 子域，google,txt，記錄，gmail，可交付性
exl-id: 311eb2d1-e445-43e6-bc2c-c6288b637f47
source-git-commit: b8065a68ed73102cb2c9da2c2d2675ce8e5fbaad
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 24%

---

# 將GoogleTXT記錄添加到子域 {#google-txt-record}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_google"
>title="Google TXT 記錄"
>abstract="若要確保電子郵件成功傳遞到 Gmail 地址，您可以將特殊的 Google 網站驗證 TXT 記錄新增到您的子網域以確保它已通過驗證。"

TXT記錄是一種DNS記錄，用於提供域的文本資訊，外部源可以讀取這些資訊。

為了確保電子郵件的最佳傳遞和成功的傳遞， [!DNL Journey Optimizer] 允許您向子域添加特殊的Google站點驗證TXT記錄，以確保已驗證。

>[!CAUTION]
>
> 只有子域具有 **[!UICONTROL 成功]** 狀態。 有關子域狀態的詳細資訊，請參閱 [此部分](about-subdomain-delegation.md#access-delegated-subdomains)。

要將GoogleTXT記錄添加到子域，請執行以下步驟：

1. 從 **[!UICONTROL 頻道]** / **[!UICONTROL 子域]** 的子菜單。

1. 在 **[!UICONTROL Googletxt]** 部分，輸入從 [Google工作區](https://support.google.com/a/answer/183895){target="_blank"}<!--G Suite Admin tools-->，然後按一下 **[!UICONTROL 保存]**。

   ![](assets/subdomain-google-txt.png)

1. 新增 TXT 記錄後，該記錄必須獲得 Google 驗證。要執行此操作，請導航至 [Google工作區](https://support.google.com/a/answer/183895){target="_blank"}<!--G Suite Admin tools-->，然後啟動驗證步驟。
