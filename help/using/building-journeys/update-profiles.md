---
solution: Journey Optimizer
product: journey optimizer
title: 更新輪廓
description: 瞭解如何在歷程中使用更新設定檔活動
feature: Journeys, Profiles, Activities
topic: Content Management
role: User
level: Intermediate
keywords: 設定檔，更新，歷程，活動
exl-id: 8b2b2d1e-9bd1-439d-a15e-acdbab387c4b
source-git-commit: 0571a11eabffeb5e318bebe341a8df18da7db598
workflow-type: tm+mt
source-wordcount: '610'
ht-degree: 6%

---

# 更新輪廓 {#update-profile}

>[!CONTEXTUALHELP]
>id="ajo_journey_update_profiles"
>title="更新輪廓活動"
>abstract="更新輪廓的動作活動可讓您利用來自事件的資訊、資料源或使用特定值來更新現有的 Adobe Experience Platform 輪廓。"

使用&#x200B;**[!UICONTROL 更新設定檔]**&#x200B;動作活動，使用來自事件、資料來源的資訊或特定值來更新現有的Adobe Experience Platform設定檔。

## 建議

* **更新設定檔**&#x200B;動作只能用於具有名稱空間的歷程中。
* 該動作只會更新現有欄位，不會建立新的設定檔欄位。
* 您無法使用&#x200B;**更新設定檔**&#x200B;動作來產生體驗事件，例如購買。
* 如同任何其他動作，您可以定義發生錯誤或逾時時的替代路徑，而且您無法同時放置兩個動作。
* 傳送至Adobe Experience Platform的更新要求為立即/在一秒內。 這通常需要幾秒鐘的時間，但有時更長，無法保證。 因此，舉例來說，如果動作使用「欄位1」，而此欄位是由之前放置的&#x200B;**更新設定檔**&#x200B;動作所更新，您就不應該預期動作中會更新「欄位1」。
* **更新設定檔**&#x200B;活動不支援定義為列舉的XDM欄位。
* **[!UICONTROL 更新設定檔]**&#x200B;活動只會更新[設定檔存放區](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html#profile-data-store){target="_blank"}，不會更新Data Lake。
* 在&#x200B;**[!UICONTROL 更新設定檔]**&#x200B;活動中選取資料集時，建議使用未由資料擷取流程鎖定的資料集。 由於&#x200B;**更新設定檔**&#x200B;更新僅儲存在[設定檔存放區](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html#profile-data-store){target="_blank"}，因此可能會以資料擷取流程覆寫這類變更。

  此外，**更新設定檔**&#x200B;活動設定不需要身分名稱空間。 因此，請確保選取的資料集使用啟動歷程的動作所使用的相同身分名稱空間，因為這些更新將使用此名稱空間。 身分對應也可以由選取的資料集使用。 若未選取具有正確名稱空間或使用身分對應的資料集，將導致&#x200B;**更新設定檔**&#x200B;活動失敗。



## 使用設定檔更新

1. 從事件開始設計您的歷程。 請參閱[本章節](../building-journeys/journey.md)。

1. 在調色盤的&#x200B;**動作**&#x200B;區段中，將&#x200B;**更新設定檔**&#x200B;活動拖放到畫布中。

   ![](assets/profileupdate0.png)

1. 從清單中選取結構描述。

1. 按一下&#x200B;**欄位**&#x200B;以選取要更新的欄位。 只能選取一個欄位。

   ![](assets/profileupdate2.png)

1. 從清單中選取資料集。

   >[!NOTE]
   >
   >**更新設定檔**&#x200B;動作會即時更新設定檔資料，但不會更新資料集。 需要選取資料集，因為設定檔是和資料集相關的記錄。

1. 按一下&#x200B;**值**&#x200B;欄位以定義您要使用的值：

   * 使用簡單運算式編輯器，您可以從資料來源或傳入事件中選取欄位。

     ![](assets/profileupdate4.png)

   * 若要定義特定值或運用進階函式，請按一下&#x200B;**進階模式**。

     ![](assets/profileupdate3.png)

**更新設定檔**&#x200B;現已設定完成。

![](assets/profileupdate1.png)


## 使用測試模式 {#using-the-test-mode}

在測試模式中，將不會模擬設定檔更新。 更新將在測試設定檔上執行。

只有測試設定檔才能進入歷程測試模式。 您可以建立新的測試設定檔，或將現有的設定檔轉換為測試設定檔。 在Adobe Experience Platform中，您可以透過csv檔案匯入或API呼叫來更新設定檔屬性。 更簡單的方法是使用&#x200B;**更新設定檔**&#x200B;動作活動，並將測試設定檔布林欄位從false變更為true。

有關如何將現有設定檔轉換為測試設定檔的詳細資訊，請參閱此[區段](../audience/creating-test-profiles.md#create-test-profiles-csv)。
