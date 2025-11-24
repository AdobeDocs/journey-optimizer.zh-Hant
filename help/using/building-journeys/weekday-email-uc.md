---
solution: Journey Optimizer
product: journey optimizer
title: 只在工作日傳送電子郵件
description: 瞭解如何設定歷程，以僅在Adobe Journey Optimizer中的工作日傳送電子郵件
feature: Journeys, Use Cases, Email
topic: Content Management
role: User
level: Intermediate
keywords: 歷程，使用案例，工作日，條件，電子郵件，排程
version: Journey Orchestration
hide: true
hidefromtoc: true
source-git-commit: ad902c1055ea2e883c028172297aab878a898b94
workflow-type: tm+mt
source-wordcount: '1121'
ht-degree: 0%

---

# 只在工作日傳送電子郵件 {#send-emails-only-on-weekdays}

此使用案例會示範如何在Adobe Journey Optimizer中設定只在工作日（星期一到星期五）傳送電子郵件的歷程。 對於在週末（星期六或星期日）進入歷程的設定檔，電子郵件會自動排入佇列，並在星期一的指定時間傳送。 這可透過在工作週期間傳遞訊息來確保最佳參與。

## 使用案例概觀

**挑戰**：確認電子郵件只會在平日傳送，即使設定檔可能會在週末進入歷程。 對於週末的登入點，電子郵件應在星期一的特定時間排入佇列並傳送。

**解決方案**：使用條件活動來識別星期幾。 對於週末專案，使用自訂公式的等待活動會將電子郵件延遲到星期一。 工作日專案會直接繼續進行電子郵件傳送步驟。

此方法可讓您使用條件活動來檢查當天是星期六還是星期日、使用自訂公式來實作等待活動以便週末輸入、將週末電子郵件排入佇列以便星期一在特定小時傳遞，以及立即傳送電子郵件以便平日輸入（星期一至星期五）。

此方法非常適合企業間(B2B)電子郵件行銷活動、專業電子報和通訊、企業相關公告、工作相關產品更新，以及任何不希望週末送貨的行銷活動。

➡️觀看逐步教學[影片](#how-to-video)

>[!NOTE]
>
>若要實作此使用案例，您需要具備已設定的[電子郵件頻道介面](../configuration/channel-surfaces.md)、[對象](../audience/about-audiences.md)或[事件](../event/about-events.md)的活動Adobe Journey Optimizer執行個體以觸發歷程，以及對[歷程條件](condition-activity.md)和[運算式](expression/expressionadvanced.md)的基本瞭解。


## 實施步驟

### 步驟1：建立您的歷程

1. 導覽至Adobe Journey Optimizer中的&#x200B;**[!UICONTROL 歷程管理]** > **[!UICONTROL 歷程]**。

1. 按一下&#x200B;**[!UICONTROL 建立歷程]**&#x200B;以建立新歷程。 [進一步瞭解如何建立歷程](journey-gs.md)

1. 設定[歷程屬性](journey-properties.md)。

1. 選擇您的歷程進入點：
   * **[讀取對象](read-audience.md)**：針對鎖定特定對象的批次行銷活動
   * **[事件](../event/about-events.md)**：針對根據客戶行為的即時觸發歷程

### 步驟2：新增「條件」活動以檢查一週中的某天

在歷程開始後，新增條件以檢查當天是星期六還是星期日。 這會相應地分支工作流程。

1. 將&#x200B;**[!UICONTROL 條件]**&#x200B;活動拖放到進入點之後的畫布上。 [進一步瞭解條件活動](condition-activity.md)

1. 按一下Condition活動以開啟其設定面板。

1. 選取&#x200B;**[!UICONTROL 時間條件]**&#x200B;作為條件型別。

1. 選取&#x200B;**一週中的某天**&#x200B;作為時間篩選選項。

1. 對於&#x200B;**第一個路徑（星期六）**，請只選取&#x200B;**星期六**。 將此路徑標示為「星期六」。

1. 按一下&#x200B;**[!UICONTROL 新增路徑]**&#x200B;以建立第二個條件。

1. 對於&#x200B;**秒路徑（星期日）**，請選取&#x200B;**一週中的某天**，然後只選取&#x200B;**星期日**。 將此路徑標示為「星期日」。

   ![在運算式編輯器中設定星期六和星期日的條件](assets/weekday-email-uc-condition-expression.png)


1. 檢查&#x200B;**[!UICONTROL 顯示上述案例以外的路徑]**，以建立工作日專案（星期一至星期五）的路徑。

>[!NOTE]
>
>用於星期評估的時區是在歷程屬性中的歷程層級定義，而不是在條件層級。 公式中使用的歷程時區是歷程的設定時區，而非收件者的時區。[進一步瞭解時區管理](timezone-management.md)。

### 步驟3：設定週末專案的等待活動

對於在星期六或星期日輸入的設定檔，使用包含自訂公式的等待活動，將電子郵件延遲到星期一您想要的時間。

在等待活動中，使用以下公式：

```javascript
toDateTimeOnly(setHours(nowWithDelta(X, "days"), H))
```

其中：

* **X**&#x200B;是等待的天數：
   * 星期六使用&#x200B;**2** （等到星期一）
   * 星期日使用&#x200B;**1** （等到星期一）
* **H**&#x200B;是您要傳送的小時（例如，上午9點為&#x200B;**9**）


**星期六的範例：**

```javascript
toDateTimeOnly(setHours(nowWithDelta(2, "days"), 9))
```

星期日的&#x200B;**範例：**

```javascript
toDateTimeOnly(setHours(nowWithDelta(1, "days"), 9))
```

若要在您的歷程中實作此專案：

1. 在&#x200B;**星期六路徑**&#x200B;上，在條件後面新增&#x200B;**[!UICONTROL 等待]**&#x200B;活動。

1. 選取&#x200B;**[!UICONTROL 持續時間]**&#x200B;作為等待型別。

1. 按一下&#x200B;**[!UICONTROL 進階模式]**&#x200B;以輸入自訂公式。

1. 輸入： `toDateTimeOnly(setHours(nowWithDelta(2, "days"), 9))`

   ![具有三個條件路徑的歷程 — 星期六、星期日和工作日](assets/weekday-email-uc-paths.png)

1. 對&#x200B;**星期日路徑**&#x200B;重複相同的步驟，使用： `toDateTimeOnly(setHours(nowWithDelta(1, "days"), 9))`

>[!TIP]
>
>針對更複雜的營業時間（例如，只在工作日的上午9點至下午5點之間傳送），您可以進一步增強公式和條件。

### 步驟4：工作日分支

對於進入星期一到星期五的設定檔，照常繼續進行電子郵件傳送步驟。

1. 在&#x200B;**工作日路徑** （「其他案例」路徑）上，直接繼續新增&#x200B;**[!UICONTROL 電子郵件]**&#x200B;動作活動。 工作日專案不需要等待活動。

1. 視需要設定您的電子郵件訊息。

### 步驟5：完成歷程流程

在星期六和星期日路徑上的等待活動後，所有三個路徑（星期六、星期日和工作日）都應流向相同的電子郵件動作活動。 在電子郵件後新增&#x200B;**[!UICONTROL End]**&#x200B;活動。

### 視覺化工作流程總覽

完整的歷程工作流程會遵循此邏輯：

* **開始** → **條件：是星期六還是星期日？**
   * **是（星期六）：**&#x200B;等到星期一上午9點→傳送電子郵件
   * **是（星期日）：**&#x200B;等到星期一上午9點→傳送電子郵件
   * **否（星期一至星期五）：**&#x200B;立即傳送電子郵件

這可確保所有電子郵件只會在平日傳送，週末的專案會自動排入星期一傳送的佇列。

### 步驟6：測試您的歷程

發佈之前，請在Adobe Journey Optimizer的測試模式下徹底測試您的歷程邏輯，以確認一切都如預期般運作：

1. 按一下右上角的&#x200B;**[!UICONTROL 測試]**&#x200B;按鈕。

1. 啟用測試模式。 [瞭解如何測試您的歷程](testing-the-journey.md)

1. 建立在一星期中不同日期具有模擬進入時間的[測試設定檔](../audience/creating-test-profiles.md)：
   * **星期六專案**：驗證設定檔是否遵循星期六路徑、在指定時間等待並接收星期一的電子郵件
   * **星期日專案**：驗證設定檔是否遵循星期日路徑、在指定時間等待並接收星期一的電子郵件
   * **星期一至星期五的專案**：確認電子郵件會立即傳送，無需任何等候

1. 檢閱歷程視覺效果，確保設定檔遵循正確的條件路徑（星期六、星期日或工作日）。

1. 檢查歷程中是否有任何錯誤或警告。 [了解疑難排解歷程](troubleshooting.md)

1. 確認「等待」公式計算所需星期一傳送時間的正確持續時間。

>[!IMPORTANT]
>
>一律在測試模式下測試您的歷程邏輯，以確保等待活動如預期般運作。 使用測試模式來模擬不同的登入案例，並驗證週末專案是否已正確排入星期一傳送的佇列。 [進一步瞭解歷程測試最佳實務](testing-the-journey.md)

### 步驟7：發佈您的歷程

測試完成後：

1. 按一下右上角的&#x200B;**[!UICONTROL 發佈]**。

1. 確認發佈。 [進一步瞭解發佈歷程](publish-journey.md)

1. 使用[歷程報告](report-journey.md)和[即時報告](../reports/journey-live-report.md)監視歷程績效。


## 相關主題

* [關於條件活動](condition-activity.md) — 瞭解如何在歷程中建立不同的路徑
* [在歷程中使用條件](conditions.md) — 歷程條件的詳細指南
* [等待活動](wait-activity.md) — 設定等待期間和公式
* [日期函式](functions/date-functions.md) — 完成日期與時間函式的參考
* [運算式編輯器](expression/expressionadvanced.md) — 建置複雜運算式
* [歷程最佳實務](journey-gs.md#best-practices) — 歷程設計的建議方法
* [社群部落格：如何在平日只傳送電子郵件](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/how-to-send-emails-only-on-weekdays-in-adobe-journey-optimizer/ba-p/760400){target="_blank"} — 包含詳細範例的原始部落格

