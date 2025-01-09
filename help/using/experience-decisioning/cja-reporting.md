---
title: Decisioning 上的報告
description: 瞭解如何針對決策製作報表。
feature: Decisioning
topic: Integrations
role: User
level: Experienced
badge: label="有限可用性"
exl-id: 7c45cd8a-8e86-4646-ba0a-db393e92d9da
source-git-commit: bfc16476f525328b2b8451bfdd57b6b2027db916
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 5%

---


# Decisioning 上的報告 {#decisioning-report}

## 程式碼型行銷活動報表 {#campaigns}

一旦程式碼型體驗上線，您就可以存取專用報告，以全方位控制面板的形式監控關鍵績效指標(KPI)，提供與行銷活動相關之基本量度的分析。

其中包括與決定專案效能相關的細節，以及使用者如何與它們互動。 [瞭解如何使用程式碼型體驗報告](../reports/campaign-global-report-cja-code.md)

![](../reports/assets/cja-decisioning-item-performance.png)

## 客戶歷程分析報告 {#cja}

如果您正在使用Customer Journey Analytics，可以利用Decisioning為您的程式碼型行銷活動建立自訂報告儀表板。

主要步驟列於下方。 有關如何使用Customer Journey Analytics的詳細資訊，請參閱[Customer Journey Analytics檔案](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-landing){target="_blank"}。

1. 在Customer Journey Analytics中建立並設定&#x200B;**連線**。 這可讓您連線至您要製作報表的資料集。 [瞭解如何建立連線](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-connections/create-connection){target="_blank"}

1. 建立&#x200B;**資料檢視**，並將其與先前建立的連線建立關聯。 在&#x200B;**[!UICONTROL 元件]**&#x200B;索引標籤中，選擇您要顯示在報告中的相關結構描述欄位。 針對決策，請確定您包含&#x200B;**propositioninteract**&#x200B;和&#x200B;**propositiondisplay**&#x200B;欄位。 [瞭解如何建立和設定資料檢視](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dataviews/create-dataview){target="_blank"}

1. 在&#x200B;**工作區專案**&#x200B;中結合資料元件、表格和視覺效果，以建立和共用程式碼型行銷活動的報告。 [瞭解如何建立工作區專案](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/build-workspace-project/create-projects){target="_blank"}
