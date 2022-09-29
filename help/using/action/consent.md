---
solution: Journey Optimizer
title: 同意
description: 同意
feature: Actions
topic: Administration
role: Admin
level: Intermediate
exl-id: 01ca4b3e-3778-4537-81e9-97ef92c9aa9e
source-git-commit: 30171e362e0dc70f5647bb2413031946062e8df3
workflow-type: tm+mt
source-wordcount: '899'
ht-degree: 1%

---

# 同意管理 {#consent-management}

Adobe Experience Platform可讓您輕鬆採用及強制執行行銷政策，以尊重客戶的同意偏好設定。 同意原則在Adobe Experience Platform中定義。 請參閱 [本檔案](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/user-guide.html?lang=en#consent-policy).

在Journey Optimizer中，您可以將這些同意政策套用至自訂動作。 例如，您可以定義同意原則，以排除尚未同意接收電子郵件、推播或簡訊通訊的客戶。

>[!NOTE]
>
>目前，僅購買了Healthcare Shield附加產品的組織才能使用同意策略。

在Journey Optimizer中，同意定義於數個層級：

* when **設定自訂動作**，您可以定義管道和行銷動作。 看這個 [節](../action/consent.md#consent-custom-action).
* 新增 **歷程中的自訂動作**，您可以定義其他行銷動作。 看這個 [節](../action/consent.md#consent-journey).

## 重要備註 {#important-notes}

在Journey Optimizer中，可在自訂動作中運用同意。 如果您想要將其與內建訊息功能搭配使用，您需要使用條件活動來篩選歷程中的客戶。

透過同意管理，會分析兩個歷程活動：

* 閱讀區段：擷取的區段會納入考量。
* 自訂動作：同意管理會考量所使用的屬性([動作參數](../action/about-custom-action-configuration.md#define-the-message-parameters))，以及已定義的行銷動作（必要的行銷動作和其他行銷動作）。
* 不支援使用現成可用聯合架構的欄位群組所屬的屬性。 這些屬性將從介面中隱藏。 您需要使用不同架構建立其他欄位群組。
* 只有在自訂動作層級設定行銷動作（必要或其他）時，才適用同意原則。

歷程中使用的所有其他活動都不會納入考量。 如果您以區段資格開始歷程，則不會考慮區段。

在歷程中，如果自訂動作中的同意政策排除設定檔，則不會將訊息傳送給他，但他會繼續歷程。 使用條件時，設定檔不會前往逾時和錯誤路徑。

在重新整理位於歷程中的自訂動作中的原則之前，請確定您的歷程沒有錯誤。

<!--
There are two types of latency regarding the use of consent policies:

* **User latency**: the delay from the time a profile changes a consent settings to the moment it is applied in Experience Platform. This can take up to 48h. 
* **Consent policy latency**: the delay from the time a consent policy is created or updated to the moment it is applied. This can take up to 6 hours
-->

## 設定自訂動作 {#consent-custom-action}

>[!CONTEXTUALHELP]
>id="ajo_consent_required_marketing_action_admin"
>title="定義必要的行銷動作"
>abstract="「必要」行銷動作可讓您定義與自訂動作相關的行銷動作。 例如，如果您使用該自訂動作來傳送電子郵件，則可以選取「電子郵件目標定位」。 在歷程中使用時，將會擷取並運用與該行銷動作相關聯的所有同意政策。 無法在畫布上修改。"

設定自訂動作時，可使用兩個欄位來管理同意。

此 **管道** 欄位可讓您選取與此自訂動作相關的通道： **電子郵件**, **簡訊**，或 **推播通知**. 它會預先填入 **必要的行銷動作** 欄位中填入所選管道的預設行銷動作。 如果您選取 **其他**，預設不會定義任何行銷動作。

![](assets/consent1.png)

此 **必要的行銷動作** 可讓您定義與自訂動作相關的行銷動作。 例如，如果您使用該自訂動作來傳送電子郵件，則可選取 **電子郵件目標定位**. 在歷程中使用時，將會擷取並運用與該行銷動作相關聯的所有同意政策。 已選取預設行銷動作，但您可以按一下向下箭頭，從清單中選取任何可用的行銷動作。

![](assets/consent2.png)

對於某些類型的重要通信（例如發送的交易式消息以重置客戶端的密碼），您可能不想應用同意策略。 然後您將選取 **無** 在 **必要的行銷動作** 欄位。

設定自訂動作的其他步驟於 [本節](../action/about-custom-action-configuration.md#consent-management).

### 建立歷程 {#consent-journey}

>[!CONTEXTUALHELP]
>id="ajo_consent_required_marketing_action_canvas"
>title="必要的行銷動作"
>abstract="建立自訂動作時會定義必要的行銷動作。 無法從動作中移除或修改此必要的行銷動作。"

>[!CONTEXTUALHELP]
>id="ajo_consent_additional_marketing_action_canvas"
>title="其他行銷動作"
>abstract="除了需要的行銷動作，還新增其他行銷動作。 將強制執行與這兩個行銷動作相關的同意政策。"

>[!CONTEXTUALHELP]
>id="ajo_consent_refresh_policies_canvas"
>title="將要在執行階段套用的同意原則視覺化呈現"
>abstract="行銷動作會引入同意政策，這些政策會結合動作參數和個別設定檔同意值，以篩選掉使用者。 按一下按鈕以重新整理，以取得這些原則的最新定義。"

在歷程中新增自訂動作時，有數個選項可讓您管理同意。 按一下 **顯示唯讀欄位** 以顯示所有參數。

此 **管道** 和 **必要的行銷動作**，在設定自訂動作時定義的，會顯示在畫面頂端。 您無法修改這些欄位。

![](assets/consent4.png)

您可以定義 **其他行銷動作** 來設定自訂動作類型。 這可讓您定義此歷程中自訂動作的用途。 除了必要的行銷動作（通常是管道專用的）之外，您還可以定義其他行銷動作，這將是特定歷程中的自訂動作專用。 例如：鍛鍊通訊、通訊、健身通訊等。 所需的行銷動作和其他行銷動作皆適用。

![](assets/consent3.png)

按一下 **刷新策略** 按鈕，以更新並檢查針對此自訂動作已考慮的原則清單。 這僅用於資訊用途，同時建立歷程。 在即時歷程中，會每6小時自動擷取和更新同意原則。

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

在歷程中設定自訂動作的其他步驟於 [本節](../building-journeys/using-custom-actions.md).
