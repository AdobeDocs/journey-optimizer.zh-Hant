---
solution: Journey Optimizer
product: journey optimizer
title: 存取委派的子網域
description: 了解如何存取委派的子網域。
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: cb3248c5-f444-47aa-80b2-c1a9fbebfcc0
source-git-commit: 3a932747de33ced59d68835a96386b7ac560e4fe
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 4%

---

# 存取委派的子網域 {#access-delegated-subdomains}

所有委派的子網域都會顯示在 **[!UICONTROL 管理]** > **[!UICONTROL 管道]** > **[!UICONTROL 子網域]** 功能表。 篩選器可協助您調整清單（委派日期、使用者或狀態）。

![](assets/subdomain-list.png)

此 **[!UICONTROL 狀態]** 欄提供子網域委派程式的相關資訊：

* **[!UICONTROL 草稿]**:子網域委派已儲存為草稿。 按一下子網域名稱以繼續委派程式，
* **[!UICONTROL 處理]**:子網域會先執行數個設定檢查，才能使用。
* **[!UICONTROL 成功]**:子網域已成功完成檢查，且可用於傳送訊息、
* **[!UICONTROL 失敗]**:提交子網域委派後，一或數項檢查失敗。

若要使用存取子網域的詳細資訊， **[!UICONTROL 成功]** 狀態，從清單中開啟它。

![](assets/subdomain-delegated.png)

您可以：

* 擷取委派程式期間設定的子網域名稱（唯讀），以及產生的URL（資源、鏡像頁面、追蹤URL）,

* 將Google網站驗證TXT記錄新增至您的子網域，以確保該記錄已驗證(請參閱 [將Google TXT記錄新增至子網域](google-txt.md))。


>[!CAUTION]
>
>子網域設定是所有環境的共同設定。 因此，對子網域的任何修改也會影響生產沙箱。
