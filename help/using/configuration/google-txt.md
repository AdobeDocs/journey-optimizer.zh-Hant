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
feature: 應用程式設定
topic: 管理
role: Admin
level: Intermediate
source-git-commit: 63de381ea3a87b9a77bc6f1643272597b50ed575
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 27%

---


# 將Google TXT記錄新增至子網域

TXT 記錄是一種 DNS 記錄，用於提供關於網域的文字資訊，可由外部來源讀取。

為了確保良好的傳遞能力，並成功將電子郵件傳送至Gmail地址，Customer Journeys Management可讓您將特殊的Google網站驗證TXT記錄新增至您的子網域，以確保進行驗證。

>[!NOTE]
>
> 只有在子域具有&#x200B;**[!UICONTROL Success]**&#x200B;狀態時，才能執行此操作。 如需子網域狀態的詳細資訊，請參閱[此區段](access-subdomains.md)。

若要將Google TXT記錄新增至您的子網域，請執行下列步驟：

1. 從&#x200B;**[!UICONTROL Channels]** / **[!UICONTROL Subdomains]**&#x200B;功能表開啟子網域。

1. 在Google txt記錄區段中，輸入在[G Suite管理工具](https://support.google.com/a/answer/183895)中產生的驗證代碼，然後按一下&#x200B;**[!UICONTROL Save]**。

   ![](../assets/subdomain-google-txt.png)

1. 新增 TXT 記錄後，該記錄必須獲得 Google 驗證。若要這麼做，請導覽至G Suite管理工具，然後啟動驗證步驟。
