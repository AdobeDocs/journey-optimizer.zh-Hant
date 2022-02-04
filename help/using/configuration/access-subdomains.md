---
title: 存取委派的子網域
description: 瞭解如何訪問委派的子域。
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: cb3248c5-f444-47aa-80b2-c1a9fbebfcc0
source-git-commit: dcdbf4a0cd6a93e56cbe97535515c1a6143db81b
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 4%

---

# 存取委派的子網域 {#access-delegated-subdomains}

所有委派的子域都顯示在 **[!UICONTROL Channels]** / **[!UICONTROL Subdomains]** 的子菜單。 篩選器可幫助您細化清單（委派日期、用戶或狀態）。

![](../assets/subdomain-list.png)

的 **[!UICONTROL Status]** 列提供有關子域委派進程的資訊：

* **[!UICONTROL Draft]**:子域委託已保存為草稿。 按一下子域名以繼續委派進程，
* **[!UICONTROL Processing]**:子域在使用前正在進行多次配置檢查，
* **[!UICONTROL Success]**:子域已成功通過檢查，可用於傳遞消息，
* **[!UICONTROL Failed]**:提交子域委派後，一個或多個檢查失敗。

要訪問有關子域的詳細資訊，請從清單中將其開啟。 您可以：

* 檢索在委派過程中配置的子域名（只讀）以及生成的URL（資源、鏡像頁、跟蹤URL）,

* 將Google站點驗證TXT記錄添加到子域以確保其已驗證(請參閱 [將GoogleTXT記錄添加到子域](google-txt.md))。

![](../assets/subdomain-delegated.png)
