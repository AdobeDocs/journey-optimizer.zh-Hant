---
solution: Journey Optimizer
product: journey optimizer
title: 使用自定義操作
description: 瞭解如何使用自定義操作
feature: Actions
topic: Content Management
role: User, Developer
level: Intermediate
keywords: 操作，自定義， API，旅程，配置，服務
exl-id: 2b1b3613-3096-43ec-a860-600dda1d83b2
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '400'
ht-degree: 25%

---

# 使用自定義操作 {#use-custom-actions}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_custom"
>title="自訂動作"
>abstract="自訂動作可讓您設定協力廠商系統的連線，以傳送訊息或 API 呼叫。您可以使用任何提供者提供的任何服務來設定動作，這些服務可透過具有 JSON 格式的裝載，透過 REST API 進行呼叫。"

自訂動作可讓您設定協力廠商系統的連線，以傳送訊息或 API 呼叫。您可以使用任何提供者提供的任何服務來設定動作，這些服務可透過具有 JSON 格式的裝載，透過 REST API 進行呼叫。

## 同意和資料治理 {#privacy}

在Journey Optimizer，您可以將資料治理和同意策略應用到您的自定義操作，以防止特定欄位導出到第三方系統或排除未同意接收電子郵件、推送或SMS通信的客戶。 有關詳細資訊，請參閱以下頁：

* [資料治理](../action/action-privacy.md)。
* [同意](../action/consent.md).

## URL 組態

的配置窗格 **自定義操作** 活動顯示為自定義操作配置的URL配置參數和驗證參數。 您不能在行程中設定URL的靜態部分，而是在自定義操作的全局配置中。 [了解更多](../action/about-custom-action-configuration.md)。

### 動態路徑

如果URL包含動態路徑，請在 **[!UICONTROL 路徑]** 的子菜單。

要連接欄位和純文字檔案字串，請使用String函式或高級表達式編輯器中的加號(+)。 將純文字檔案字串用單引號(&#39;)或雙引號(&quot;)括起來。 [了解更多](expression/expressionadvanced.md)。

下表顯示了配置示例：

| 欄位 | 值 |
| --- | --- |
| URL | `https://xxx.yyy.com:8080/somethingstatic/` |
| 路徑 | `The id of marketingCampaign + '/messages'` |

連接的URL具有以下表單：

`https://xxx.yyy.com:8080/somethingstatic/`\&lt;campaign id=&quot;&quot;>`/messages`

![](assets/journey-custom-action-url.png)

### 標題和查詢參數 {#headers}

的 **[!UICONTROL URL配置]** 部分顯示動態標題和查詢參數欄位，但不顯示常數欄位。 動態標題和查詢參數欄位在操作配置螢幕中定義為變數。 [了解更多](../action/about-custom-action-configuration.md#url-configuration)

要指定動態標題和查詢參數欄位的值，請在欄位內或鉛筆表徵圖上按一下，然後選擇所需欄位。

![](assets/journey-dynamicheaderfield.png)

## 操作參數

在 **[!UICONTROL 操作參數]** 部分，您將看到定義為 _&quot;變數&quot;_。 對於這些參數，可以定義獲取此資訊的位置(例如：事件、資料源)、手動傳遞值或使用高級表達式編輯器進行高級使用案例。 高級使用案例可以是資料操作和其他函式使用。 請參閱此 [頁](expression/expressionadvanced.md)。

**相關主題**

[設定動作](../action/about-custom-action-configuration.md)
