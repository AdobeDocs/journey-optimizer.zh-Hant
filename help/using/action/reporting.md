---
solution: Journey Optimizer
product: journey optimizer
title: 歷程報告
description: 瞭解如何使用歷程報告中的資料
feature: Reporting, Journeys
topic: Content Management
role: User
level: Intermediate
badge: label="有限可用性" type="Informative"
source-git-commit: b93d2288156713ac7479eef491f6104df1955a18
workflow-type: tm+mt
source-wordcount: '431'
ht-degree: 1%

---

# 監視您的自訂動作 {#reporting}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_custom_actions_monitor"
>title="監視您的自訂動作"
>abstract="**[!UICONTROL 自訂動作]**&#x200B;報告頁面可讓您追蹤歷程對協力廠商系統發出的API呼叫效能和可靠性。"

>[!AVAILABILITY]
>
>自訂動作報告目前僅適用於一組組織（可用性限制）。

**[!UICONTROL 自訂動作]**&#x200B;報告頁面可讓您監視從歷程對第三方系統發出的API呼叫的可靠性和效能。 這些報告可協助您快速識別可能影響傳送的整合問題、延遲瓶頸或節流/上限限制。

「自訂動作」報表頁面的功能與Journey Optimizer中的其他所有時間報表相同。 如需儀表板功能的詳細資訊，請參閱[本檔案](../reports/report-cja-manage.md)。

若要存取&#x200B;**[!UICONTROL 自訂動作]**&#x200B;報告頁面，請從您的![](assets/do-not-localize/Smock_Monitoring_18_N.svg)動作&#x200B;**[!UICONTROL 首頁中按一下]**。

![](assets/monitor-1.png)

➡️ [進一步瞭解如何設定自訂動作](../action/about-custom-action-configuration.md)

## KPI {#kpis}

![](assets/monitor-2.png)

**[!UICONTROL 自訂動作]**&#x200B;關鍵績效指標(KPI)可作為集中式儀表板，提供自訂動作呼叫的運作狀況與可靠性的整合檢視。 這些量度可讓您評估效能、找出瓶頸，並確保與外部系統的穩定整合。

+++ 進一步瞭解自訂動作KPI

* **[!UICONTROL 成功的呼叫]**：傳回有效回應且沒有錯誤的HTTP呼叫總數。

* **[!UICONTROL 4xx/5xx錯誤]**：由於使用者端(4xx)或伺服器端(5xx)錯誤，強調設定問題或端點失敗而失敗的呼叫數目。

* **[!UICONTROL 逾時]**：因超過最大回應時間而失敗的呼叫數。 這有助於顯示外部端點的延遲或效能問題。

* **[!UICONTROL 已設定上限]**：由於上限限制而被封鎖的呼叫數目，可確保下游系統不會超載。

* **[!UICONTROL 平均RPS]**：在選取的時間範圍內，自訂動作每秒處理的要求數目。

+++

## 通話超時 {#calls}

![](assets/monitor-3.png)

**[!UICONTROL 加班通話]**&#x200B;圖表顯示報告所選時段內的HTTP通話KPI趨勢。 時間序列的詳細程度取決於所選的時間範圍。 例如：

* 對於7天報表，每個資料點都會顯示一天的KPI。
* 如果您選取1天時間範圍，圖表會顯示每小時的KPI。
* 如果您選取1小時時間範圍，圖表將顯示每分鐘的KPI。

➡️[如需HTTP呼叫量度的說明，請參閱KPI區段](#kpis)

## 呼叫劃分 {#breakdown}

![](assets/monitor-4.png)

**[!UICONTROL 呼叫劃分]**&#x200B;表格提供HTTP呼叫量度的階層式劃分，從最上層每個端點的整體量度，到使用每個端點的每個自訂動作的量度，再到最底層依賴這些量度的歷程。

➡️[如需HTTP呼叫量度的說明，請參閱KPI區段](#kpis)


