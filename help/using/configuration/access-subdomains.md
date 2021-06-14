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
role: Administrator
level: Intermediate
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 3%

---


# 存取委派的子網域

所有委派的子網域都會顯示在&#x200B;**[!UICONTROL Channels]** / **[!UICONTROL Subdomains]**&#x200B;功能表中。 篩選器可協助您調整清單（委派日期、使用者或狀態）。

![](../assets/subdomain-list.png)

**[!UICONTROL Status]**&#x200B;欄提供子網域委派程式的相關資訊：

* **[!UICONTROL Draft]**:子網域委派已儲存為草稿。按一下子網域名稱以繼續委派程式，
* **[!UICONTROL Processing]**:子網域會先執行數個設定檢查，才能使用。
* **[!UICONTROL Success]**:子網域已成功完成檢查，且可用於傳送訊息、
* **[!UICONTROL Failed]**:提交子網域委派後，一或數項檢查失敗。

若要存取子網域的詳細資訊，請從清單中開啟該子網域。 您可以：

* 擷取委派程式期間設定的子網域名稱（唯讀），以及產生的URL（資源、鏡像頁面、追蹤URL）,

* 將Google網站驗證TXT記錄新增至您的子網域，以確保該記錄已驗證（請參閱[將Google TXT記錄新增至子網域](google-txt.md)）。

![](../assets/subdomain-delegated.png)
