---
title: 將GoogleTXT記錄添加到子域
description: 瞭解如何將GoogleTXT記錄添加到子域
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 311eb2d1-e445-43e6-bc2c-c6288b637f47
source-git-commit: dcdbf4a0cd6a93e56cbe97535515c1a6143db81b
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 26%

---

# 將GoogleTXT記錄添加到子域 {#google-txt-record}

TXT 記錄是一種 DNS 記錄，用於提供關於網域的文字資訊，可由外部來源讀取。

為了確保電子郵件的良好傳送和成功地傳送到Gmail地址， [!DNL Journey Optimizer] 允許您向子域添加特殊的Google站點驗證TXT記錄，以確保驗證。

>[!CAUTION]
>
> 只有子域具有 **[!UICONTROL Success]** 狀態。 有關子域狀態的詳細資訊，請參閱 [此部分](access-subdomains.md)。

要將GoogleTXT記錄添加到子域，請執行以下步驟：

1. 從 **[!UICONTROL Channels]** / **[!UICONTROL Subdomains]** 的子菜單。

1. 在 **[!UICONTROL Google txt record]** 部分，輸入從 [Google工作區](https://support.google.com/a/answer/183895){target=&quot;_blank&quot;<!--G Suite Admin tools-->，然後按一下 **[!UICONTROL Save]**。

   ![](../assets/subdomain-google-txt.png)

1. 新增 TXT 記錄後，該記錄必須獲得 Google 驗證。要執行此操作，請導航至 [Google工作區](https://support.google.com/a/answer/183895){target=&quot;_blank&quot;<!--G Suite Admin tools-->，然後啟動驗證步驟。
