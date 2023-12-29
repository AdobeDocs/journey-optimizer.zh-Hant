---
solution: Journey Optimizer
product: journey optimizer
title: 將 Google TXT 記錄新增至子網域
description: 瞭解如何將Google TXT記錄新增至子網域
feature: Subdomains, Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: 子網域， google， txt，記錄， gmail，傳遞能力
exl-id: 311eb2d1-e445-43e6-bc2c-c6288b637f47
source-git-commit: 8579acfa881f29ef3947f6597dc11d4c740c3d68
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 30%

---

# 將 Google TXT 記錄新增至子網域 {#google-txt-record}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_google"
>title="Google TXT 記錄"
>abstract="若要確保電子郵件成功傳遞到 Gmail 地址，您可以將特殊的 Google 網站驗證 TXT 記錄新增到您的子網域以確保它已通過驗證。"

TXT記錄是一種DNS記錄，用於提供關於網域的文字資訊，可以由外部來源讀取。

為了確保最佳傳遞能力並成功傳遞電子郵件至Gmail地址， [!DNL Journey Optimizer] 可讓您將特殊的Google網站驗證TXT記錄新增至您的子網域，以確保其經過驗證。

>[!CAUTION]
>
> 只有在子網域具備以下條件時，才能執行此作業： **[!UICONTROL 成功]** 狀態。 如需子網域狀態的詳細資訊，請參閱 [本節](about-subdomain-delegation.md#access-delegated-subdomains).

若要將Google TXT記錄新增至子網域，請執行下列步驟：

1. 從開啟子網域 **[!UICONTROL 頻道]** / **[!UICONTROL 子網域]** 功能表。

1. 在 **[!UICONTROL Google txt記錄]** 區段，輸入產生的驗證代碼 [Google工作區](https://support.google.com/a/answer/183895){target="_blank"}<!--G Suite Admin tools-->，然後按一下 **[!UICONTROL 儲存]**.

   ![](assets/subdomain-google-txt.png)

1. 新增 TXT 記錄後，該記錄必須獲得 Google 驗證。若要這麼做，請導覽至 [Google工作區](https://support.google.com/a/answer/183895){target="_blank"}<!--G Suite Admin tools-->，然後啟動驗證步驟。
