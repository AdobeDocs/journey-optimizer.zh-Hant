---
solution: Journey Optimizer
product: journey optimizer
title: 設定檔專案管理
description: 瞭解如何管理設定檔專案
feature: Journeys
role: User
level: Intermediate
keywords: 重新進入、歷程、設定檔、週期性
exl-id: 8874377c-6594-4a5a-9197-ba5b28258c02
source-git-commit: 35f52afe61bf3eda897cc96f5484778522e38d45
workflow-type: tm+mt
source-wordcount: '620'
ht-degree: 13%

---


# 設定檔專案管理 {#entry-management}

歷程有兩種主要型別：

* 事件型歷程：從事件開始，這些歷程是單一的，會與一個人建立關聯。 收到事件時，個人會進入歷程。 [閱讀全文](#entry-unitary)
* 讀取對象歷程：從讀取對象開始，這些是批次歷程。 屬於對象的個人都會進入相同歷程。 這些歷程可以是循環或單次。 [閱讀全文](#entry-read-segment)

在這兩種歷程型別中，設定檔無法在同一歷程中同時出現多次。

## 單一歷程{#entry-unitary}

在單一歷程中，您可以啟用或停用重新進入：

* 如果啟用重新進入，設定檔可以進入歷程多次，但必須完全退出歷程的上一個執行個體，才能進入歷程。

* 如果停用重新進入，則設定檔無法多次進入同一歷程。

依預設，新歷程允許重新進入。 您可以取消勾選「單次」歷程的選項，例如，如果想在某人造訪商店時提供一次性禮物。 在這種情況下，客戶必須無法重新進入歷程並再次收到選件。 歷程結束時，其狀態為 **[!UICONTROL 已關閉]**. 新的個人無法再進入歷程。 已在歷程中的人員會正常完成歷程。 [了解更多](journey-gs.md#entrance)

![](assets/journey-re-entrance.png)

在預設值之後 [全域逾時](journey-gs.md#global_timeout) 在30天中，歷程會切換至 **已完成** 狀態。 歷程中已有的設定檔會正常完成歷程。 新設定檔無法再進入歷程。 此行為僅設定30天（即歷程逾時預設值），因為有關進入歷程的設定檔的所有資訊都會在進入30天後移除。 在該時段後，設定檔可以重新進入歷程。 為避免此情況，並完全停用這些設定檔的重新進入，您可以使用設定檔或受眾資料，新增條件以測試是否已輸入設定檔。

<!--
Due to the 30-day journey timeout, when journey re-entrance is not allowed, we cannot make sure the re-entrance blocking will work more than 30 days. Indeed, as we remove all information about persons who entered the journey 30 days after they enter, we cannot know the person entered previously, more than 30 days ago. -->

單一歷程 (從事件或對象資格開始) 包含可防止同一事件多次錯誤觸發歷程的護欄。 在預設情況下，設定檔重新進入時會暫時封鎖 5 分鐘。 例如，如果某個事件在 12:01 觸發特定設定檔的歷程，而另一個事件在 12:03 達到時間限制 (無論是相同事件或是不同事件觸發相同歷程)，則此設定檔的歷程將不會再次開始。

金鑰也可用來檢查個人是否在歷程中。 事實上，一個人在同一歷程中不能位於兩個不同的位置。 因此，系統不允許相同的金鑰（例如金鑰CRMID=3224）位於相同歷程中的不同位置。

## 讀取對象歷程{#entry-read-segment}

在讀取對象歷程中：

* 對於非循環歷程：設定檔進入歷程一次，且只進入歷程一次。

* 對於週期性歷程：依預設，屬於對象的所有設定檔都會在每次週期性進入歷程。 使用者必須先完成歷程，才能在另一個發生次數中重新進入。

>[!NOTE]
>
>有兩個選項可用於循環讀取受眾歷程。 此 **在重複時強制重新進入** 選項可讓歷程中仍存在的所有設定檔在下次執行時自動退出。 此 **增量讀取** 選項只會鎖定自上次執行歷程以來進入對象的個人。 請參閱此 [區段](../building-journeys/read-audience.md#configuring-segment-trigger-activity)

在商業事件歷程中，以 **讀取對象** 活動：瞭解此歷程是根據接收業務事件，如果設定檔符合預期對象的資格，他們會針對收到的每個業務事件進入歷程，這表示此設定檔可能在同一歷程中同時出現多次，但位於不同業務事件的情境下。