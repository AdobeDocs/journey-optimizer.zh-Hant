---
solution: Journey Optimizer
title: 同意
description: 內容
feature: Actions
topic: Administration
role: Admin
level: Intermediate
hide: true
hidefromtoc: true
source-git-commit: 6958b03907bdc2e57e336efe27d7528cc60f86f2
workflow-type: tm+mt
source-wordcount: '848'
ht-degree: 0%

---

# 同意管理(beta) {#consent-management}

Adobe Experience Platform允許您輕鬆採用並實施營銷策略，以尊重客戶的同意偏好。 同意政策在Adobe Experience Platform定義。 請參閱 [本文檔](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/user-guide.html?lang=en#consent-policy)。

在Journey Optimizer，您可以將這些同意策略應用於自定義操作。 例如，您可以定義同意策略以排除未同意接收電子郵件、推送或SMS通信的客戶。

>[!NOTE]
>
>此功能作為私有測試版發佈。 並非所有Journey Optimizer客戶都可用。

在Journey Optimizer，同意在幾個層面被定義：

* 何時 **配置自定義操作**，您可以定義渠道和市場營銷活動。 查看 [節](../action/consent.md#consent-custom-action)。
* 添加時 **旅途中的定製操作**，您可以定義附加的市場營銷活動。 查看 [節](../action/consent.md#consent-journey)。

## 重要備註 {#important-notes}

在Journey Optimizer，在海關行動中可以利用同意。 如果要將其與內置消息功能一起使用，則需要使用條件活動來篩選旅途中的客戶。

在同意管理下，對兩種旅行活動進行了分析：

* 讀取段：檢索到的段被考慮在內。
* 自定義操作：同意管理考慮使用的屬性([動作參數](../action/about-custom-action-configuration.md#define-the-message-parameters))以及已定義的市場營銷操作（必需的市場營銷操作和其他市場營銷操作）。

旅行中使用的所有其他活動均未被考慮在內。 如果您以段資格開始您的旅程，則不會考慮段。

在旅程中，如果某個配置檔案在自定義操作中被同意策略排除，則不會將消息發送給他，但他會繼續此旅程。 使用條件時，配置檔案不會轉到超時和錯誤路徑。

在刷新位於行程中的自定義操作中的策略之前，請確保您的行程沒有錯誤。

<!--
There are two types of latency regarding the use of consent policies:

* **User latency**: the delay from the time a profile changes a consent settings to the moment it is applied in Experience Platform. This can take up to 48h. 
* **Consent policy latency**: the delay from the time a consent policy is created or updated to the moment it is applied. This can take up to 6 hours
-->

## 配置自定義操作 {#consent-custom-action}

>[!CONTEXTUALHELP]
>id="ajo_consent_required_marketing_action_admin"
>title="定義必需的市場營銷活動"
>abstract="「必需的市場營銷」活動允許您定義與自定義活動相關的市場營銷活動。 例如，如果您使用該自定義操作發送電子郵件，則可以選擇「電子郵件目標」。 在行程中使用時，將檢索並利用與該市場營銷操作相關的所有同意策略。 無法在畫布上修改此內容。"

配置自定義操作時，可以使用兩個欄位進行同意管理。

的 **頻道** 欄位允許您選擇與此自定義操作相關的通道： **電子郵件**。 **簡訊**&#x200B;或 **推送通知**。 它會預填充 **必需的市場營銷操作** 的子菜單。 如果選擇 **其他**，預設情況下不會定義市場營銷操作。

![](assets/consent1.png)

的 **必需的市場營銷操作** 允許您定義與自定義操作相關的市場營銷操作。 例如，如果您使用該自定義操作發送電子郵件，則可以選擇 **電子郵件目標**。 在行程中使用時，將檢索並利用與該市場營銷操作相關的所有同意策略。 選擇了預設的市場營銷操作，但您可以按一下向下箭頭從清單中選擇任何可用的市場營銷操作。

![](assets/consent2.png)

對於某些類型的重要通信，例如發送的事務性消息以重置客戶端的密碼，您可能不想應用同意策略。 然後，您將選擇 **無** 的 **必需的市場營銷操作** 的子菜單。

配置自定義操作的其他步驟在中詳細介紹 [此部分](../action/about-custom-action-configuration.md#consent-management)。

### 建立歷程 {#consent-journey}

>[!CONTEXTUALHELP]
>id="ajo_consent_required_marketing_action_canvas"
>title="必需的市場營銷操作"
>abstract="在建立自定義操作時定義所需的市場營銷操作。 無法從操作中刪除或修改此必需的市場營銷操作。"

>[!CONTEXTUALHELP]
>id="ajo_consent_additional_marketing_action_canvas"
>title="其他市場營銷活動"
>abstract="除了需要的操作之外，還添加其他市場營銷操作。 將強制執行與兩個市場營銷操作相關的同意策略。"

>[!CONTEXTUALHELP]
>id="ajo_consent_refresh_policies_canvas"
>title="可視化將在運行時應用的同意策略"
>abstract="市場營銷操作引入了將操作參數和個人配置檔案同意值相結合的同意策略，以過濾用戶。 通過按一下要刷新的按鈕獲取這些策略的最新定義。"

在行程中添加自定義操作時，有幾個選項允許您管理同意。 按一下 **顯示只讀欄位** 顯示所有參數。

的 **頻道** 和 **必需的市場營銷操作**，在配置自定義操作時定義的，將顯示在螢幕頂部。 不能修改這些欄位。

![](assets/consent4.png)

您可以定義 **其他市場營銷活動** 來設定自定義操作的類型。 這允許您定義此行程中自定義操作的目的。 除了通常特定於渠道的必需市場營銷活動之外，您還可以定義附加的市場營銷活動，該活動將特定於此特定行程中的自定義活動。 例如：健身通訊、通訊、健身通訊等。 所需的市場營銷活動和附加的市場營銷活動都將適用。

![](assets/consent3.png)

按一下 **刷新策略** 按鈕，以更新和檢查為此自定義操作考慮的策略清單。 這僅用於資訊目的，同時構建旅程。 對於即時旅程，每6小時自動檢索和更新一次同意策略。

![](assets/consent5.png)

<!--
The following data is taken into account for consent:

* marketing actions and additional marketing actions defined in the custom action
* action parameters defined in the custom action, see this [section](../action/about-custom-action-configuration.md#define-the-message-parameters) 
* attributes used as criteria in a segment when the journey starts with a Read segment, see this [section](../building-journeys/read-segment.md) 

>[!NOTE]
>
>Please note that there can be a latency when updating the list of policies applied, refer to this [this section](../action/consent.md#important-notes).
-->

在行程中配置自定義操作的其他步驟在中詳細介紹 [此部分](../building-journeys/using-custom-actions.md)。
