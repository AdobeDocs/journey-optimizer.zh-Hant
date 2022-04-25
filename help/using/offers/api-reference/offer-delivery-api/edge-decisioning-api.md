---
title: 使用邊緣決策API提供服務
description: Adobe Experience PlatformWeb SDK允許您檢索和呈現您使用API或服務庫建立的個性化服務。
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
source-git-commit: b02981f2c0cf74c8dba657570157709bc422d94c
workflow-type: tm+mt
source-wordcount: '730'
ht-degree: 3%

---


# 使用邊緣決策API提供服務 {#edge-decisioning-api}

## 入門和先決條件 {#aep-web-sdk-overview-and-prerequisites}

的 [Adobe Experience PlatformWeb SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html#video-overview) 是客戶端JavaScript庫，它允許Adobe Experience Cloud客戶通過Experience Platform邊緣網路與Experience Cloud中的各種服務進行交互。

Experience PlatformWeb SDK支援在Adobe查詢個性化解決方案，包括決策管理，允許您檢索和呈現您使用API或服務庫建立的個性化服務。 有關更詳細的說明，請參閱 [建立聘用](../../get-started/starting-offer-decisioning.md)。

有兩種方法可與 [平台Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html#video-overview)。 一種方法是面向開發者，需要瞭解網站和寫程式。 另一種方法是使用Adobe Experience Platform用戶介面來設定提供，它只需在HTML頁的標題中引用一個小指令碼即可。

請參閱上 [offer decisioning](https://experienceleague.adobe.com/docs/experience-platform/edge/personalization/offer-decisioning/offer-decisioning-overview.html?lang=en#enabling-offer-decisioning) 有關如何使用平台Web SDK提供個性化服務的詳細資訊。

>[!NOTE]
>
>Adobe Experience PlatformWeb SDK中的決策管理目前可以提前訪問選定用戶。 此功能並非所有IMS組織都可用。

## Adobe Experience Platform Web SDK  {#aep-web-sdk-overview-and-prerequisites}

平台Web SDK取代了以下SDK:

* Visitor.js
* AppMeasurement.js
* AT.js
* DIL.js

SDK沒有將這些庫合併，而是從頭開始的新實現。 要使用它，必須首先執行以下步驟：

1. 確保您的組織具有使用SDK的適當權限，並且您已正確配置了權限。

   <!-- For more detailed instructions, refer to the documentation on using the [Adobe Experience Platform Web SDK](). -->

1. [配置資料流](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/datastreams.html?lang=en) 在您在Adobe Experience Cloud的帳戶中的「資料收集」頁籤中。

1. 安裝SDK。 有多種方法可以執行此操作， [安裝SDK頁](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/installing-the-sdk.html?lang=en)。 本頁將繼續介紹每種不同的實現方法。

要使用SDK，必須有 [架構](../../../start/get-started-schemas.md) 和 [資料流](../../../start/get-started-datasets.md) 定義。

<!-- ****TODO - Configure schema**** -->

要個性化服務，必須單獨配置個性化/配置檔案。

<!-- Refer to the [doc](www.link.com) for detailed instructions.  -->

要配置SDK進行Offer decisioning，請執行以下兩步之一：

## 選項1 — 使用啟動安裝標籤擴展和實施

對於編碼體驗可能較少的人，此選項更方便用戶。

1. [建立標籤屬性](https://experienceleague.adobe.com/docs/experience-platform/tags/admin/companies-and-properties.html?lang=en)

1. [添加嵌入代碼](https://experienceleague.adobe.com/docs/core-services-learn/implementing-in-websites-with-launch/configure-launch/launch-add-embed.html?lang=en)

1. 從「Datastream」下拉清單中選擇配置，使用您建立的Datastream安裝和配置平台Web SDK擴展。 請參閱 [擴展](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/extensions/overview.html?lang=en)。

   ![Adobe Experience Platform Web SDK](../../assets/installed-catalog-web-sdk.png)

   ![配置擴展](../../assets/configure-sdk-extension.png)

1. 建立必要 [資料元素](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/data-elements.html?lang=en)。 至少，必須建立平台Web SDK標識映射和平台Web SDK XDM對象資料元素。

   ![身分對應](../../assets/sdk-identity-map.png)

   ![XDM 物件](../../assets/xdm-object.png)

1. 建立 [規則](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/rules.html?lang=en):

   添加平台Web SDK發送事件操作，並將相關decisionScope添加到該操作的配置中

   ![呈現優惠](../../assets/rule-render-offer.png)

   ![請求優惠](../../assets/rule-request-offer.png)

1. [建立和發佈](https://experienceleague.adobe.com/docs/experience-platform/tags/publish/libraries.html?lang=en) 包含您配置的所有相關規則、資料元素和擴展的庫。

## 選項2 — 使用預構建的獨立版本手動實施

以下是使用預構建的Web SDK獨立安裝使用Offer decisioning所需的步驟。 本指南假定這是您首次實施SDK，因此所有步驟可能都不適用於您。 本指南還假定了一些發展經驗。

在選項2中包括以下JavaScript代碼段：上預構建的獨立版本 [此頁](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/installing-the-sdk.html?lang=en) 的 `<head>` 的子菜單。


## 限制

移動體驗邊緣工作流當前不支援某些服務約束，例如封頂。 「上限設定」欄位值指定可在所有用戶間顯示優惠的次數。 有關詳細資訊，請參閱 [向優惠添加約束](../../offer-library/add-constraints.md#capping)。
