---
title: PTR記錄
description: 了解如何xxxx
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
source-git-commit: 6988a6ab9412e5d27f1ba9d1145cc11c7c06e7b7
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 0%

---


# PTR記錄

## 關於PTR記錄

指針記錄(PTR)是一種域名系統(DNS)記錄，它提供連結到IP地址的域名。

使用PTR記錄，接收郵件伺服器可以通過識別其IP地址是否與伺服器所連接的名稱相對應來檢查發送郵件伺服器的真實性。

## 訪問子網域的PTR記錄

在Customer Journey Management中委派子網域後，就會自動建立PTR記錄並與此子網域關聯。 您可以從&#x200B;**[!UICONTROL Channels]** / **[!UICONTROL PTR records]**&#x200B;功能表存取。

![](../assets/ptr-records.png)

該清單使用以下語法顯示為每個委派子域生成的PTR記錄：

* 「r」表示記錄，
* 「xx」表示IP地址的最後兩個數字，
* 子網域名稱。

您可以從清單中開啟PTR記錄，以顯示關聯的子域名和IP地址。

>[!NOTE]
>
>請注意，PTR記錄是只讀的，您不能修改與IP地址關聯的子域。
