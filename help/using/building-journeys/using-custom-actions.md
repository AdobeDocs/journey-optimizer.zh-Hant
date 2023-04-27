---
solution: Journey Optimizer
product: journey optimizer
title: 使用自訂動作
description: 了解如何使用自訂動作
feature: Actions
topic: Content Management
role: User, Developer
level: Intermediate
keywords: 動作，自訂， API，歷程，設定，服務
exl-id: 2b1b3613-3096-43ec-a860-600dda1d83b2
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '400'
ht-degree: 25%

---

# 使用自訂動作 {#use-custom-actions}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_custom"
>title="自訂動作"
>abstract="自訂動作可讓您設定協力廠商系統的連線，以傳送訊息或 API 呼叫。您可以使用任何提供者提供的任何服務來設定動作，這些服務可透過具有 JSON 格式的裝載，透過 REST API 進行呼叫。"

自訂動作可讓您設定協力廠商系統的連線，以傳送訊息或 API 呼叫。您可以使用任何提供者提供的任何服務來設定動作，這些服務可透過具有 JSON 格式的裝載，透過 REST API 進行呼叫。

## 同意與資料控管 {#privacy}

在Journey Optimizer中，您可以將資料控管和同意政策套用至您的自訂動作，以防止特定欄位匯出至協力廠商系統，或排除未同意接收電子郵件、推播或簡訊通訊的客戶。 如需詳細資訊，請參閱下列頁面：

* [資料控管](../action/action-privacy.md).
* [同意](../action/consent.md).

## URL 組態

的設定窗格 **自訂動作** 活動會顯示URL設定參數以及為自訂動作設定的驗證參數。 您無法在歷程中設定URL的靜態部分，但是在自訂動作的全域設定中。 [了解更多](../action/about-custom-action-configuration.md)。

### 動態路徑

如果URL包含動態路徑，請在 **[!UICONTROL 路徑]** 欄位。

若要串連欄位和純文字字串，請使用進階運算式編輯器中的字串函式或加號(+)。 用單引號(&#39;)或雙引號(&quot;)將純文字字串括住。 [了解更多](expression/expressionadvanced.md)。

下表顯示配置的示例：

| 欄位 | 值 |
| --- | --- |
| URL | `https://xxx.yyy.com:8080/somethingstatic/` |
| 路徑 | `The id of marketingCampaign + '/messages'` |

串連的URL有下清單單：

`https://xxx.yyy.com:8080/somethingstatic/`\&lt;campaign id=&quot;&quot;>`/messages`

![](assets/journey-custom-action-url.png)

### 標題和查詢參數 {#headers}

此 **[!UICONTROL URL設定]** 區段顯示動態標題和查詢參數欄位，但不顯示常數欄位。 動態標題和查詢參數欄位在動作設定畫面中定義為變數。 [了解更多](../action/about-custom-action-configuration.md#url-configuration)

若要指定動態標題和查詢參數欄位的值，請在欄位內按一下，或在鉛筆圖示上按一下，然後選取所需欄位。

![](assets/journey-dynamicheaderfield.png)

## 動作參數

在 **[!UICONTROL 動作參數]** 小節中，您會看到定義為 _&quot;變數&quot;_. 對於這些參數，您可以定義取得此資訊的位置(範例：事件、資料來源)、手動傳遞值，或使用進階運算式編輯器來處理進階使用案例。 進階使用案例可以是資料操作和其他函式使用。 請參閱 [頁面](expression/expressionadvanced.md).

**相關主題**

[設定動作](../action/about-custom-action-configuration.md)
