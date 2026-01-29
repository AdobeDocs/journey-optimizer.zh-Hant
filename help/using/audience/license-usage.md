---
solution: Journey Optimizer
product: journey optimizer
title: 授權使用量儀表板
description: 瞭解Journey Optimizer授權使用控制面板
feature: Audiences, Profiles
topic: Content Management
role: User
level: Beginner
exl-id: 7e91face-c8f4-4e70-9123-9e36bae7e67e
source-git-commit: db1e4ee5b2b4bb3a3d7d9e86aded14ad3c613765
workflow-type: tm+mt
source-wordcount: '795'
ht-degree: 1%

---

# 授權使用量儀表板 {#license-usage}

[!DNL Adobe Journey Optimizer] [使用者介面](../start/user-interface.md)提供儀表板，顯示貴組織授權使用狀況的重要資訊，如每日快照期間所擷取。

若要存取此儀表板，請移至&#x200B;**[!UICONTROL 管理]** > **[!UICONTROL 授權使用情況]**。 這會開啟&#x200B;**[!UICONTROL 概觀]**&#x200B;標籤，顯示儀表板。

![授權使用量儀表板總覽](assets/license-usage-dashboard.png)

>[!NOTE]
>
>* 若要檢視儀表板，您必須擁有[檢視授權使用儀表板](https://experienceleague.adobe.com/docs/experience-platform/dashboards/permissions.html?lang=zh-Hant#available-permissions){target="_blank"}許可權。
>
>* 如配額欄中的`N/A`所指示，某些量度（例如計算時數、電子郵件）不會顯示給開發沙箱。 控制面板中只會顯示非null的值：當量度為零或接近零時，系統不會填入量度。


對於[!DNL Adobe Journey Optimizer]，儀表板可讓您檢查&#x200B;**可參與的設定檔**&#x200B;的數量。

## 什麼是可參與設定檔？ {#what-is-engageable-profile}

**可參與的設定檔**&#x200B;是代表個人資訊的記錄，該資訊儲存在設定檔服務中，且已由歷程或行銷活動參與。

可參與設定檔的主要特性：

* **12個月的滾動期間**：可參與的設定檔是根據過去12個月的參與計算的。 此量度會顯示您嘗試使用Journey Optimizer的編寫、決策、傳送、實驗或協調功能參與的不重複設定檔數量。

* **每個沙箱的不重複計數**：如果設定檔在沙箱中進入多個歷程或行銷活動，則只會計算為該沙箱的單一可參與設定檔一次。

* **根據可定址的受眾**：可參與的設定檔是根據您的可定址受眾所計算。 此計數代表過去12個月使用任何Journey Optimizer功能參與的受眾（在可定址的受眾總數中）。

* **量度行為**：可參與的設定檔計數：
   * 當新設定檔透過歷程或行銷活動參與時，可能會增加
   * 除非未與某些設定檔進行超過12個月的互動，否則無法減少
   * 當假名設定檔連結到已知設定檔時，可能會減少

>[!NOTE]
>
>如果您發現可參與設定檔計數突然尖峰，請參閱下方的[疑難排解區段](#troubleshooting-engageable-profiles)，以取得有關瞭解和解決問題的詳細指引。

## 疑難排解：參與設定檔計數大幅增加 {#troubleshooting-engageable-profiles}

如果您觀察到可參與設定檔計數突然激增（例如，設定檔從一天數十萬增加到數百萬個），本節提供指南來瞭解和解決問題。

### 瞭解增加

可參與設定檔量度會反映過去12個月中歷程或行銷活動所參與的不重複設定檔數量。 突然增加可能是由於：

* 新歷程或行銷活動所瞄準的大型對象
* 為設定檔服務啟用的資料集變更
* 批次處理最近未參與的對象

### 解決方法步驟

若要解決此問題，請遵循下列步驟：

1. **瞭解設定檔計數邏輯：**

   * 可參與設定檔是根據過去12個月中歷程或行銷活動參與的不重複設定檔來計算。
   * 如果設定檔進入多個歷程，則會計為該Sandbox的一個「可參與」設定檔。
   * 除非已超過12個月沒有與某些設定檔互動，或假名設定檔已連結到已知設定檔，否則量度無法減少。
   * 可參與設定檔是使用客戶的可定址對象來計算。
   * 過去12個月使用任何Journey Optimizer功能的參與對象（在可定址對象總數中）會決定可參與設定檔的數量。

2. **調查以大型對象為目標的歷程、行銷活動和決策：**

   * 使用[可參與的設定檔查詢](../reports/query-examples.md#engageable-profiles-queries)或[查詢服務](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/query/home){target="_blank"}，檢閱以大量設定檔為目標的最近歷程和行銷活動。
   * 識別造成設定檔計數尖峰的特定歷程版本。
   * 涉及新設定檔的歷程、行銷活動和決策，可能會導致Journeys資料集中的事件計數增加，進而導致「參與設定檔」計數上升。

3. **在歷程與行銷活動層級篩選對象：**

   * 在起始歷程或行銷活動之前在對象層級套用篩選器，以防止可參與設定檔不必要的增加。
   * 確保在參與期間僅鎖定相關對象。

4. **減少可定址對象大小：**

   * 必要時刪除假名設定檔。 請注意，此動作會同時影響Journey Optimizer和Real-Time Customer Data Platform。
   * 在即時客戶設定檔指南中進一步瞭解[假名設定檔資料有效期](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/profile/pseudonymous-profiles){target="_blank"}。
   * **注意：**&#x200B;無法透過Platform UI或API設定假名設定檔資料的有效期。 您必須聯絡支援才能啟用此功能。

5. **監視資料集變更：**

   * 驗證已啟用資料集以進行效能分析，並確定資料集未包含過多的ECID (Experience Cloud ID)。
   * 如有需要，請刪除具有高ECID計數的資料集，然後使用減少的記錄來重新建立這些資料集。

6. **開發長期縮減策略：**

   * 如果某些設定檔閒置超過12個月，「可參與的設定檔」計數自然會減少。

**另請參閱：**

* [可參與設定檔查詢範例](../reports/query-examples.md#engageable-profiles-queries) — 可監視和分析可參與設定檔的範例查詢
* [Adobe Experience Platform查詢服務總覽](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/query/home){target="_blank"}

## 相關檔案 {#related-documentation}

在Adobe Experience Platform檔案中進一步瞭解：

* [授權使用量儀表板總覽](https://experienceleague.adobe.com/docs/experience-platform/dashboards/guides/license-usage.html?lang=zh-Hant){target="_blank"}
* [探索授權使用儀表板](https://experienceleague.adobe.com/docs/experience-platform/dashboards/guides/license-usage.html?lang=zh-Hant#exploring-the-license-usage-dashboard){target="_blank"}
* [可用的量度](https://experienceleague.adobe.com/docs/experience-platform/dashboards/guides/license-usage.html?lang=zh-Hant#available-metrics){target="_blank"}
* [假名設定檔資料有效期](https://experienceleague.adobe.com/docs/experience-platform/profile/pseudonymous-profiles.html?lang=zh-Hant){target="_blank"}
