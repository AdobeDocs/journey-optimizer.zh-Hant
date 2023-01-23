---
solution: Journey Optimizer
product: journey optimizer
title: 將Google TXT記錄新增至子網域
description: 了解如何將Google TXT記錄新增至子網域
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
keywords: 子網域，google,txt，記錄，gmail，傳遞能力
exl-id: 311eb2d1-e445-43e6-bc2c-c6288b637f47
source-git-commit: b8065a68ed73102cb2c9da2c2d2675ce8e5fbaad
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 10%

---

# 將Google TXT記錄新增至子網域 {#google-txt-record}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_google"
>title="Google TXT記錄"
>abstract="若要確保將電子郵件成功傳送至Gmail地址，您可以將特殊的Google網站驗證TXT記錄新增至子網域，以確認其已驗證。"

TXT記錄是一種DNS記錄，用於提供網域的文字資訊，可由外部來源讀取。

為確保最佳傳遞能力，以及成功傳送電子郵件至Gmail地址， [!DNL Journey Optimizer] 可讓您將特殊的Google網站驗證TXT記錄新增至子網域，以確認其已驗證。

>[!CAUTION]
>
> 只有在子網域具有 **[!UICONTROL 成功]** 狀態。 如需子網域狀態的詳細資訊，請參閱 [本節](about-subdomain-delegation.md#access-delegated-subdomains).

若要將Google TXT記錄新增至子網域，請執行下列步驟：

1. 從 **[!UICONTROL 管道]** / **[!UICONTROL 子網域]** 功能表。

1. 在 **[!UICONTROL Google txt記錄]** 部分，輸入從 [Google Workspace](https://support.google.com/a/answer/183895){target="_blank"}<!--G Suite Admin tools-->，然後按一下 **[!UICONTROL 儲存]**.

   ![](assets/subdomain-google-txt.png)

1. 新增 TXT 記錄後，該記錄必須獲得 Google 驗證。若要這麼做，請導覽至 [Google Workspace](https://support.google.com/a/answer/183895){target="_blank"}<!--G Suite Admin tools-->，然後啟動驗證步驟。
