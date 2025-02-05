---
solution: Journey Optimizer
product: journey optimizer
title: 設定檔專案管理
description: 瞭解如何管理設定檔專案
feature: Journeys, Profiles
role: User
level: Intermediate
keywords: 重新進入、歷程、設定檔、週期性
exl-id: 8874377c-6594-4a5a-9197-ba5b28258c02
source-git-commit: aec3d79ad07ec6904e55afd6fc61ba9b4f403fc8
workflow-type: tm+mt
source-wordcount: '699'
ht-degree: 5%

---


# 輪廓入口管理 {#entry-management}

設定檔入口管理取決於歷程型別。 在Adobe Journey Optimizer中，提供下列型別的歷程：

* **單一事件**&#x200B;歷程：這些歷程始於單一事件。 收到事件時，關聯的設定檔會進入歷程。 [閱讀全文](#entry-unitary)

* **商務事件**&#x200B;歷程：這些歷程的開頭為商務事件，緊接著是&#x200B;**讀取對象**&#x200B;活動。 收到事件時，屬於目標對象的設定檔會進入歷程。 系統會為每個設定檔建立一個歷程例項。 [閱讀全文](#entry-business)

* **讀取對象**&#x200B;歷程：這些歷程以&#x200B;**讀取對象**&#x200B;活動開始。 執行歷程時，屬於目標對象的設定檔會進入歷程。 系統會為每個設定檔建立一個歷程例項。 這些歷程可以是循環或「單次」。 [閱讀全文](#entry-read-audience)

* **對象資格**&#x200B;歷程：這些歷程以對象資格事件開始。 這些歷程會監聽對象中設定檔的入口和出口。 發生此情況時，關聯的設定檔會進入歷程。 [閱讀全文](#entry-unitary)

在所有歷程型別中，設定檔無法在同一歷程中同時出現多次。 若要檢查某人是否在歷程中，則會將設定檔身分識別當作金鑰。 系統不允許相同的索引鍵（例如索引鍵`CRMID=3224`）位於相同歷程中的不同位置。

## 單一事件和受眾資格歷程{#entry-unitary}

在&#x200B;**單一事件**&#x200B;和&#x200B;**對象資格**&#x200B;歷程中，您可以啟用或停用重新進入：

* 如果啟用重新進入，設定檔可以進入歷程多次，但必須完全退出歷程的上一個執行個體，才能進入。

* 如果停用重新進入，則設定檔無法在全域歷程逾時期間內多次進入相同歷程。 請參閱[本章節](../building-journeys/journey-properties.md#global_timeout)。

依預設，歷程允許重新進入。 啟動&#x200B;**允許重新進入**&#x200B;選項時，會顯示&#x200B;**重新進入等待期間**&#x200B;欄位。 它可讓您定義允許設定檔再次進入歷程之前的等待時間。 這可防止同一事件多次錯誤觸發歷程。預設情況下，欄位會設為 5 分鐘。 持續時間上限為91天（[全域逾時](journey-properties.md#global_timeout)）。

<!--
When a journey ends, its status is **[!UICONTROL Closed]**. New individuals can no longer enter the journey. Persons already in the journey automatically exit the journey. 
-->

![](assets/journey-re-entrance.png)

在重新進入期間後，設定檔可以重新進入歷程。 為避免此情況，並完全停用這些設定檔的重新進入，您可以使用設定檔或受眾資料，新增條件以測試是否已輸入設定檔。

<!--
Due to the 30-day journey timeout, when journey reentrance is not allowed, we cannot make sure the reentrance blocking will work more than 91 days. Indeed, as we remove all information about persons who entered the journey 91 days after they enter, we cannot know the person entered previously, more than 91 days ago. -->

## 業務歷程 {#entry-business}

<!--
Business events follow reentrance rules in the same way as for unitary events. If a journey allows reentrance, the next business event will be processed.
-->

在&#x200B;**商業歷程**&#x200B;中，若要允許多個商業事件執行，請在歷程屬性的&#x200B;**[!UICONTROL 執行]**&#x200B;區段中啟動對應的選項。

![](assets/business-entry.png)

若是業務事件，對於特定歷程，第一次執行所擷取的對象資料會在1小時時段內重複使用。

個人資料可能在同一歷程中同時出現多次，但在不同業務事件的情境下會出現。

如需詳細資訊，請參閱此[區段](../event/about-creating-business.md)

## 讀取對象歷程 {#entry-read-audience}

**讀取對象**&#x200B;歷程可以是週期性或「一次性」：

* 對於非循環/「單次」歷程：設定檔在歷程中只進入一次。

* 對於循環歷程：依預設，屬於對象的所有設定檔都會在每次循環時進入歷程。 使用者必須先完成歷程，才能在另一個發生次數中重新進入。

有兩個選項可用於循環讀取受眾歷程：

* **增量讀取**&#x200B;選項：當具有週期性&#x200B;**讀取對象**&#x200B;的歷程首次執行時，對象中的所有設定檔都會進入歷程。 此選項可讓您在第一次發生後，僅將目標設定為自上次執行歷程以來進入對象的個人。

  >[!NOTE]
  >
  >如果您在歷程中鎖定為[自訂上傳對象](../audience/about-audiences.md#segments-in-journey-optimizer)，則只有在循環歷程中啟用此選項時，才會擷取第一次循環的設定檔，因為這些對象已修正。

* **重複時強制重新進入**：此選項可讓您讓歷程中仍存在的所有設定檔在下次執行時自動退出。 如果設定檔在此歷程中的生命週期可能超過週期頻率（例如，如果您使用等待活動），請勿啟用此選項以確保設定檔可完成其歷程。

![](assets/read-audience-options.png)

如需詳細資訊，請參閱此[區段](../building-journeys/read-audience.md#configuring-segment-trigger-activity)

<!--
After 91 days, a Read audience journey switches to the **Finished** status. This behavior is set for 91 days only (i.e. journey timeout default value) as all information about profiles who entered the journey is removed 91 days after they entered. Persons still in the journey automatically are impacted. They exit the journey after the 30 day timeout. 
-->
