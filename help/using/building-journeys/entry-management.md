---
solution: Journey Optimizer
product: journey optimizer
title: 設定檔項目管理
description: 了解如何管理設定檔項目
feature: Journeys
role: User
level: Intermediate
source-git-commit: f04454860ebe597d3306e62b58de5f32e08342ee
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%

---

# 設定檔項目管理 {#entry-management}

在單一歷程中：

* 如果已啟用重新進入，設定檔可以進入歷程數次，但必須完全退出歷程的先前例項，才能進行。

* 如果停用重新進入，設定檔就無法多次輸入相同的歷程

如需設定檔重新進入的詳細資訊，請參閱 [節](../building-journeys/journey-gs.md#change-properties).

在讀取區段歷程中：

* 對於非循環歷程：設定檔會進入歷程一次，而且只進入一次。
* 針對循環歷程：如果設定檔處於區段/預期狀態，則會在每次重複執行時進入歷程。 如果他仍在前一次的復期歷程中，會從頭開始重新開始。

在從讀取區段開始的商業事件歷程中：

知道此歷程是以接收業務事件為基礎，如果設定檔符合預期區段的資格，他將為收到的每個業務事件輸入歷程，這表示此設定檔可在相同歷程中多次，同時，但位在不同業務事件的情境中。

單一歷程（從事件或區段資格開始）包含防止同一事件多次錯誤觸發歷程的護欄。 設定檔重新進入預設會暫時封鎖5分鐘。 例如，如果某個事件在12:01對特定設定檔觸發歷程，而另一個事件在12:03到達（無論是相同事件或是不同事件觸發相同歷程），該歷程將不會對此設定檔重新開始。
