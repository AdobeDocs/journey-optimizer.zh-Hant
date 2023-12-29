---
solution: Journey Optimizer
product: journey optimizer
title: 使用同意原則
description: 了解如何使用 Adobe Experience Platform 同意原則
feature: Journeys, Actions, Custom Actions, Privacy, Consent Management
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Experienced
keywords: 原則、治理、平台、Healthcare Shield、同意
exl-id: 01ca4b3e-3778-4537-81e9-97ef92c9aa9e
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '911'
ht-degree: 100%

---

# 使用同意原則 {#consent-management}

Adobe Experience Platform 可讓您輕鬆採用及強制執行行銷政策，以尊重客戶的同意偏好設定。 在 Adobe Experience Platform 中定義的同意原則。 請參閱[本文件](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/user-guide.html?lang=zh-Hant#consent-policy)。

在 Journey Optimizer 中，您可以將這些同意原則套用至自訂動作。 例如，若客戶尚未同意接收電子郵件、推播或簡訊通訊，您可定義同意原則以排除客戶。

>[!NOTE]
>
>同意原則目前僅適用於已購買 Healthcare Shield 附加元件產品的組織。

在 Journey Optimizer，同意定義於數個層級：

* 當您&#x200B;**設定自訂動作**&#x200B;時，您可定義管道與行銷動作。 請參閱[本章節](../action/consent.md#consent-custom-action)。
* 當您新增&#x200B;**自訂動作至歷程**，您可定義其他行銷動作。 請參閱[本章節](../action/consent.md#consent-journey)。

## 重要備註 {#important-notes}

在 Journey Optimizer，您可在自訂動作利用同意。 如果您想將其與內建訊息功能搭配使用，您需使用條件活動來篩選歷程客戶。

同意管理會分析兩種歷程活動：

* 讀取對象：擷取的對象會納入考量。
* 自訂動作：同意管理會考量所使用的屬性 ([動作參數](../action/about-custom-action-configuration.md#define-the-message-parameters))，以及已定義的行銷動作 (必要的行銷動作與其他行銷動作)。
* 不支援使用現成可用聯集結構的欄位群組所屬的屬性。 這些屬性將從介面中隱藏。 您需要使用不同方案建立其他欄位群組。
* 僅在自訂動作層級設定行銷動作 (必要或其他) 時，才適用同意原則。

歷程使用的所有其他活動都不會納入考量。 如果您以對象資格開始歷程，則不會將對象納入考量。

在歷程中，如果自訂動作的同意原則排除設定檔，則不會傳送訊息給他，但他會繼續歷程。 當使用條件時，設定檔不會前往逾時與錯誤路徑。

在重新整理位於歷程自訂動作的原則之前，請確定您的歷程無誤。

<!--
There are two types of latency regarding the use of consent policies:

* **User latency**: the delay from the time a profile changes a consent settings to the moment it is applied in Experience Platform. This can take up to 48h. 
* **Consent policy latency**: the delay from the time a consent policy is created or updated to the moment it is applied. This can take up to 6 hours
-->

## 設定自訂動作 {#consent-custom-action}

>[!CONTEXTUALHELP]
>id="ajo_consent_required_marketing_action"
>title="定義必要的行銷動作"
>abstract="此必要的行銷動作可讓您定義與自訂動作相關的行銷動作。 例如，如果您利用該自訂動作傳送電子郵件，則可選取電子郵件目標定位。當使用於歷程時，會擷取並運用與該行銷動作相關聯的所有同意原則。 無法在畫布修改。"

在設定自訂動作時，可利用兩個欄位進行同意管理。

此&#x200B;**頻道**&#x200B;欄位可讓您選取與此自訂動作相關的頻道：**電子郵件**、**簡訊**，或&#x200B;**推播通知**。它會以所選頻道的預設行銷動作，預先填入&#x200B;**必要的行銷動作**&#x200B;欄位。 如果您選取&#x200B;**其他**，預設情況下不會定義任何行銷動作。 

![](assets/consent1.png)

此&#x200B;**必要的行銷動作**&#x200B;可讓您定義與自訂動作相關的行銷動作。 例如，如果您利用該自訂動作傳送電子郵件，則可選取&#x200B;**電子郵件目標定位**。當使用於歷程時，會擷取並運用與該行銷動作相關聯的所有同意原則。 已選取預設行銷動作，但您可按一下向下箭頭，從清單選取任何可用的行銷動作。

![](assets/consent2.png)

對於特定類型的重要通訊 (例如傳送異動訊息以重設用戶端密碼)，您可能不需要套用同意原則。 那麼，您可在&#x200B;**必要行銷動作**&#x200B;欄位選取&#x200B;**無**。

[本節](../action/about-custom-action-configuration.md#consent-management)詳細介紹了設定自訂動作的其他步驟。

### 建立歷程 {#consent-journey}

>[!CONTEXTUALHELP]
>id="ajo_consent_required_marketing_action_canvas"
>title="必要行銷動作"
>abstract="在建立自訂動作時會定義必要行銷動作。 無法從動作移除或修改此必要行銷動作。"

>[!CONTEXTUALHELP]
>id="ajo_consent_additional_marketing_action_canvas"
>title="其他行銷動作"
>abstract="除必要行銷動作外，新增其他行銷動作。 將強制執行與這兩個行銷動作相關的同意原則。"

>[!CONTEXTUALHELP]
>id="ajo_consent_refresh_policies_canvas"
>title="視覺化呈現要在執行階段套用的同意原則"
>abstract="行銷動作會引入同意原則，該原則會結合動作參數與個別設定檔同意值，以篩選使用者。 按一下按鈕重新整理，以取得這些原則的最新定義。"

當新增自訂動作至歷程時，您可利用數個選項管理同意。按一下&#x200B;**顯示唯讀欄位**&#x200B;以顯示所有參數。

此&#x200B;**頻道**&#x200B;與在設定自訂動作時定義的&#x200B;**必要的行銷動作**，會顯示在畫面頂端。 您無法修改這些欄位。

![](assets/consent4.png)

您可以定義&#x200B;**其他行銷動作**&#x200B;來設定自訂動作類型。 這可讓您定義此歷程中自訂動作的用途。 除了必要的行銷動作 (通常是頻道專用的) 之外，您還可以定義其他行銷動作，這些動作為此特定歷程中的自訂動作專用。 例如：運動訓練通訊、電子報、健身通訊等。 所需的行銷動作和其他行銷動作皆適用。

![](assets/consent3.png)

按一下畫面下方的&#x200B;**重新整理原則**&#x200B;按鈕，以更新並檢查此自訂動作納入考慮的原則清單。 這僅作為建立歷程時的資訊用途。 在即時歷程，每 6 小時會自動擷取並更新同意原則。

![](assets/consent5.png)

<!--
The following data is taken into account for consent:

* marketing actions and additional marketing actions defined in the custom action
* action parameters defined in the custom action, see this [section](../action/about-custom-action-configuration.md#define-the-message-parameters) 
* attributes used as criteria in a segment when the journey starts with a Read segment, see this [section](../building-journeys/read-audience.md) 

>[!NOTE]
>
>Please note that there can be a latency when updating the list of policies applied, refer to this [this section](../action/consent.md#important-notes).
-->

[本節](../building-journeys/using-custom-actions.md)詳細介紹了在歷程中設定自訂動作的其他步驟。
