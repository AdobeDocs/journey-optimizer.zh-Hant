---
title: 委派子網域
description: 了解如何委派子網域
page-status-flag: never-activated
uuid: null
contentOwner: null
products: null
audience: administrators
content-type: reference
topic-tags: null
discoiquuid: null
internal: n
snippet: y
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 311eb2d1-e445-43e6-bc2c-c6288b637f47
source-git-commit: 1d7f661dc0a89e4754a76ecf2cdce1e43a5275ec
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 29%

---

# 將Google TXT記錄新增至子網域

TXT 記錄是一種 DNS 記錄，用於提供關於網域的文字資訊，可由外部來源讀取。

為確保良好的傳遞能力，並成功將電子郵件傳送至Gmail地址， [!DNL Journey Optimizer] 可讓您將特殊的Google網站驗證TXT記錄新增至子網域，以確保經過驗證。

>[!CAUTION]
>
> 只有在子網域具有 **[!UICONTROL Success]** 狀態。 如需子網域狀態的詳細資訊，請參閱 [本節](access-subdomains.md).

若要將Google TXT記錄新增至子網域，請執行下列步驟：

1. 從 **[!UICONTROL Channels]** / **[!UICONTROL Subdomains]** 功能表。

1. 在 **[!UICONTROL Google txt record]** 部分，輸入從 [Google Workspace](https://support.google.com/a/answer/183895){target=&quot;_blank&quot;}<!--G Suite Admin tools-->，然後按一下 **[!UICONTROL Save]**.

   ![](../assets/subdomain-google-txt.png)

1. 新增 TXT 記錄後，該記錄必須獲得 Google 驗證。若要這麼做，請導覽至 [Google Workspace](https://support.google.com/a/answer/183895){target=&quot;_blank&quot;}<!--G Suite Admin tools-->，然後啟動驗證步驟。
