---
title: 應用程式內報告
description: 了解如何使用應用程式內報表的資料
feature: Reporting
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: 3d496efc-1bf9-4895-906c-3757f92c6fe3
source-git-commit: c4683e10e4a15f99206a3e8702c1ad20591f1d67
workflow-type: tm+mt
source-wordcount: '608'
ht-degree: 4%

---

# 應用程式內報告 {#inapp-report}

「促銷活動」報表中提供「應用程式內」報表。

將顯示「促銷活動」報表頁面，其中包含下列標籤：

* [Campaign](../reports/campaign-global-report.md#campaign-live)
* [電子郵件](../reports/campaign-global-report.md#email-live)
* [推播](../reports/campaign-global-report.md#push-live)
* [SMS](../reports/campaign-global-report.md#sms-live)
* [應用程式內](#in-app-global)

行銷活動 **[!UICONTROL 全域報表]** 會分為不同的小工具，詳細說明促銷活動的成功和錯誤。 如有需要，可對每個介面工具集調整大小並加以刪除。 有關詳細資訊，請參閱 [節](../reports/global-report.md#modify-dashboard).

如需Adobe Journey Optimizer中可用每個量度的詳細清單，請參閱 [本頁](../reports/global-report.md#list-of-components-global.md)

## 應用程式內索引標籤 {#inapp-global}

從您的行銷活動 **[!UICONTROL 全域報表]**, **[!UICONTROL 應用程式內]** 索引標籤會詳細列出與促銷活動中傳送的應用程式內傳送相關的主要資訊。

![](assets/campaign_report_global_6.png)

+++進一步了解「應用程式內」報表可用的不同量度和Widget。

此 **[!UICONTROL 應用程式內效能]** KPI會詳細說明與訪客對您應用程式內訊息的參與相關的主要資訊，例如：

* **[!UICONTROL 不重複曝光數]**:將應用程式內訊息傳送至的不重複使用者人數。

* **[!UICONTROL 曝光數]**:傳送給所有使用者的應用程式內訊息總數。

* **[!UICONTROL 點按率]**:與已看見訊息的使用者相比，與應用程式內訊息中包含的按鈕互動的使用者百分比。

* **[!UICONTROL 退出率]**:收件者已關閉的應用程式內訊息百分比。

此 **[!UICONTROL 應用程式內摘要]** 圖表顯示相關時段內應用程式內曝光數的演變。

此 **[!UICONTROL 按按鈕點按次數]** 圖形和表格包含每個按鈕的收件者行為可用資料：

* **[!UICONTROL 點按次數]**:與應用程式內訊息中包含的按鈕互動的收件者總數。

* **[!UICONTROL 點按率]**:與已看見訊息的使用者相比，與應用程式內訊息中包含的按鈕互動的使用者百分比。
+++

**相關主題：**

* [建立應用程式內訊息](../in-app/create-in-app.md)
* [設計應用程式內訊息](../in-app/design-in-app.md)
* [應用程式內設定](../in-app/inapp-configuration.md)


>[!BEGINTABS]

>[!TAB 新增推送至歷程]

1. 開啟您的歷程，然後從浮動視窗的「動作」區段拖放推播活動。

1. 提供訊息的基本資訊（標籤、說明、類別），然後選擇要使用的訊息表面。

>[!TAB 新增推送至促銷活動]

1. 建立新的排程或API觸發促銷活動，請選取 **[!UICONTROL 推播通知]** 作為您的動作，並選取 **[!UICONTROL 應用程式表面]** 來使用。

1. 按一下&#x200B;**[!UICONTROL 建立]**。

1. 從 **[!UICONTROL 屬性]** 區段，編輯您的促銷活動 **[!UICONTROL 標題]** 和 **[!UICONTROL 說明]**.

1. 按一下 **[!UICONTROL 選取對象]** 按鈕，從可用的Adobe Experience Platform區段清單中定義要鎖定的對象。

1. 在 **[!UICONTROL 身分命名空間]** 欄位中，選擇要使用的命名空間，以識別所選區段中的個人。

1. 促銷活動設計為在特定日期或循環頻率上執行。 了解如何設定 **[!UICONTROL 排程]** 你的競選。

1. 從 **[!UICONTROL 動作觸發器]** 菜單，選擇 **[!UICONTROL 頻率]** 推播通知的：

   * 一次
   * 每日
   * 每週
   * 每月

>[!ENDTABS]

測試2:

1. 這是個測試

>[!BEGINTABS]

>[!TAB 新增推送至歷程]

    1. 開啟您的歷程，然後從浮動視窗的「動作」區段拖放推播活動。
    
    1. 提供訊息的基本資訊（標籤、說明、類別），然後選擇要使用的訊息表面。

>[!TAB 新增推送至促銷活動]

    1. 建立新的排程或API觸發促銷活動，請選取**[!UICONTROL 推播通知]**作為您的動作，並選**[!UICONTROL 應用程式表面]**使用。
    
    1. 按一下**[!UICONTROL 建立]**。
    
    1. 從**[!UICONTROL 屬性]**區段，編輯促銷活動**[!UICONTROL 標題]**和**[!UICONTROL 說明]**。
    
    1. 按一下**[!UICONTROL 選取對象]**按鈕，從可用的Adobe Experience Platform區段清單中定義要鎖定的對象。
    
    1. 在**[!UICONTROL 身分命名空間]**欄位，選擇要使用的命名空間，以識別所選區段中的個人。
    
    1. 促銷活動設計為在特定日期或循環頻率上執行。 了解如何設定**[!UICONTROL 排程]**你的競選。
    
    1. 從**[!UICONTROL 動作觸發器]**菜單，選擇**[!UICONTROL 頻率]**推播通知：
    
    *一次
    *每日
    *每週
    *每月

>[!ENDTABS]

1. 這是測試的一部分
