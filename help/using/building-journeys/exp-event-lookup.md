---
solution: Journey Optimizer
product: journey optimizer
title: 歷程中的體驗事件查閱
description: 瞭解如何在歷程中使用體驗事件查閱
exl-id: 35e2e347-0669-44a3-92ba-aee52e54c219
version: Journey Orchestration
source-git-commit: 62783c5731a8b78a8171fdadb1da8a680d249efd
workflow-type: tm+mt
source-wordcount: '929'
ht-degree: 6%

---

# 歷程中的體驗事件查閱 {#ee-journeys}

>[!CAUTION]
>
>自2025年7月8日起，在新的客戶組織中，歷程條件中使用的運算式編輯器不再支援使用體驗事件建立運算式。 因此，[Experience Platform 資料來源](../datasource/adobe-experience-platform-data-source.md)中的體驗事件無法用於建立運算式。使用體驗事件建立運算式/邏輯的替代方法和最佳實務參考如下。
>
>需要更多詳細資訊嗎？ [閱讀常見問答集](#faq-ee)。

此頁面概述常見的模式和可擴充的方法，協助您充份運用Adobe Journey Optimizer中的體驗事件。 這些使用案例旨在協助您解決經常遇到的挑戰，例如管理選擇退出、控制訊息頻率、根據使用者行為個人化內容以及對即時訊號做出反應。

運用這些策略，您可以將行為資料轉換為有意義的動作，也就是根據設定檔觸發的事件或屬性隱藏、限定或排除設定檔。 無論您是建置購買臨界值、放棄觸發程式或跳出處理的邏輯，這些範例都能提供您可因應需求的實用指引。

在評估哪種方法最適合時，請考慮使用案例的延遲需求，以確保您的歷程保持回應式且有效。

## 選擇退出隱藏

若要隱藏已選擇退出行銷通訊的設定檔，請使用內建的同意管理。 選擇退出偏好設定會在設定檔的同意欄位中自動擷取；它們可以在歷程條件中直接參考，並在訊息傳送期間由Journey Optimizer自動強制執行。

了解更多：

* [管理同意](../privacy/opt-out.md)
* [電子郵件選擇退出管理](../email/email-opt-out.md)
* [文字訊息的選擇退出管理](../sms/sms-opt-out.md)


## 跳出型隱藏

若要排除經歷過電子郵件跳出的設定檔，請運用Adobe Journey Optimizer的自動隱藏清單來隱藏跳出的地址。 此內建機制可確保將無效或無法存取的電子郵件從未來的傳送中排除，而不需要自訂邏輯。

了解更多：

* [管理禁止名單](../configuration/manage-suppression-list.md)


## 一般隱藏

若要隱藏已示範特定行為的設定檔，請使用具有事件型邏輯的批次對象，以擷取符合隱藏條件的設定檔。 在歷程條件中參考此對象。

了解更多：

* Adobe Experience Platform [區段產生器 — 事件](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/segment-builder#events){target="_blank"}

* Adobe Experience Platform [區段產生器 — 時間限制](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/segment-builder#time-constraints){target="_blank"}

* [在條件中使用對象](../building-journeys/condition-activity.md#using-audiences-in-conditions)

* [inAudience()函式](../building-journeys/functions/functioninaudience.md)


## 通訊收到的排除

若要防止傳送訊息給在最近一段時間內收到任何通訊的設定檔：

* 使用具有時間型條件的批次對象，並在歷程條件中參照它們。
* 套用頻率上限商業規則以強制執行每日或每週訊息限制。


使用對象深入瞭解：

* Adobe Experience Platform [區段產生器 — 事件](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/segment-builder#events){target="_blank"}

* Adobe Experience Platform [區段產生器 — 時間限制](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/segment-builder#time-constraints){target="_blank"}

* [在條件中使用對象](../building-journeys/condition-activity.md#using-audiences-in-conditions)

* [inAudience()函式](../building-journeys/functions/functioninaudience.md)


另請參閱：

* [依據頻道、通訊類型，設定頻率上限](../conflict-prioritization/channel-capping.md)



## 訊息特定包含/排除

若要根據設定檔是否收到特定訊息來包含或排除設定檔，請建立封裝此邏輯的批次對象，並在歷程條件中參考這些對象。


了解更多：

* Adobe Experience Platform [區段產生器 — 事件](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/segment-builder#events){target="_blank"}

* Adobe Experience Platform [區段產生器 — 時間限制](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/segment-builder#time-constraints){target="_blank"}

* [在條件中使用對象](../building-journeys/condition-activity.md#using-audiences-in-conditions)

* [inAudience()函式](../building-journeys/functions/functioninaudience.md)

## 購物車或瀏覽放棄個人化

若要根據最新的購物車進行個人化通訊，或跨多種購物車型別或產品檢視瀏覽事件：

* 如果您可以存取[Adobe Experience Platform Data Distiller](https://experienceleague.adobe.com/en/docs/experience-platform/query/data-distiller/overview){target="_blank"}，請設定自動查詢以從事件擷取所需資料、處理資料以符合使用案例，並將其寫入已啟用設定檔的資料集以進行啟用。
* 如果可以在具有純量屬性的設定檔上建立放棄資料的模型，請考慮使用計算屬性來擷取最新資訊，然後在歷程中參照這些屬性來建構通訊。 [請到 Adobe Experience Platform 文件](https://experienceleague.adobe.com/en/docs/experience-platform/profile/computed-attributes/overview){target="_blank"}那邊，了解更多相關資訊。


## 行為型歷程退出

若要在設定檔顯示特定行為時將其從歷程中移除，可在收到特定事件或設定檔符合特定對象資格時，利用退出條件從歷程中退出設定檔。

了解更多：

* [設定您的歷程屬性 — 退出條件](journey-properties.md#exit-criteria)

## 以購買為基礎的資格，含值臨界值

若要根據購買觸發歷程並隱藏值是否高於/低於臨界值，請定義計算屬性以加總特定時段內的購買。 建立受眾，其中包含支出金額符合特定條件的設定檔。

了解更多：

* Adobe Experience Platform [計算屬性總覽](https://experienceleague.adobe.com/en/docs/experience-platform/profile/computed-attributes/overview){target="_blank"}



## 常見問題 {#faq-ee}

不再支援在歷程運算式/條件中使用體驗事件。 影響會列於以下的常見問題集中：

+++哪些特定功能會受到影響？ 

只有運算式編輯器中的體驗事件查詢會受到影響。 下列功能&#x200B;**不**&#x200B;受影響，且保持不變：

* 觀察與設定檔UI中特定設定檔相關聯的體驗事件

* 在計算屬性規則中使用體驗事件並存取歷程中的計算屬性

* 觸發具有單一或業務事件的歷程

* 在運算式和個人化編輯器中使用來自觸發歷程之事件的歷程內容資料

* 聆聽歷程中的事件

* 設定事件以觸發歷程

* 偵測行銷通訊的一般使用者反應事件（例如電子郵件開啟）

+++

+++我現有的Adobe組織是否會受到此更新的影響？ 

只有當您尚未使用體驗事件查詢時，才會影響您的Adobe組織。 如果您已在[Experience Platform資料來源](../datasource/adobe-experience-platform-data-source.md)中使用體驗事件，您的Adobe組織會繼續支援體驗事件查閱。

+++

+++我有一個新的Adobe組織。 如何解決需要體驗事件資料的使用案例？ 

上述提供體驗事件的替代方法和最佳實務，有助於達成理想的使用案例。

+++

+++ 如果替代方法不適用於我的使用案例，該怎麼辦？

如果您的使用案例無法使用上述的替代方法之一解決，請洽詢您的Adobe代表。

+++
