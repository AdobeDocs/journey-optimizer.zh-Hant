---
solution: Journey Optimizer
product: journey optimizer
title: 訊息最佳化
description: 運用訊息最佳化來建立個人化和最佳化的行銷活動。
feature: Message optimization
topic: Experimentation
role: User
level: Intermediate
keywords: 行銷活動最佳化、實驗、目標定位、A/B測試
source-git-commit: 378ead41924496f52f22026b3f0e05a9c9c76f89
workflow-type: tm+mt
source-wordcount: '918'
ht-degree: 0%

---

# 行銷活動中的最佳化 {#message-optimization}

最佳化可讓您使用工具，為行銷活動的對象提供個人化和最佳化的內容，<!--based on marketer-defined advanced decision configurations. This ensures that the right message reaches the right audience at the right time in order to maximize the effectiveness of your campaigns. (Removed for now as Decisioning is not yet supported)-->確保最大限度的參與和成功，以建立高度<!--customized and -->有效的行銷活動。

透過最佳化，您可以：

* 運用[目標定位](#targeting)規則
* 執行[內容實驗](#experimentation)
* 在單一行銷活動中使用[進階組合](#combination)的實驗和目標定位

行銷活動上線後，會根據定義的條件評估設定檔，並根據比對條件，提供行銷活動中的適當體驗或內容。

實驗與目標鎖定之間的差異概述如下：

* 實驗包括根據流量分配隨機分割提供內容&#x200B;。
* 鎖定目標會使用確定性技術，根據使用者設定檔、對象成員資格或內容型規則來傳送內容。

![](assets/msg-optimization-experiment-vs-targeting.png){width="110%" zoomable="yes"}

## 善用目標定位 {#targeting}

目標定位會根據使用者設定檔屬性或內容屬性，將個人化內容提供給特定對象區段。

實驗是隨機指派訊息內容，而目標定位則是將內容提供給正確受眾的確定性方式，與此不同。

透過鎖定目標，可根據下列專案定義特定規則：

* **使用者設定檔屬性**，例如位置(例如 地理定位)、年齡或偏好設定。 例如，美國的使用者會看到「Golden Gate」促銷活動，而法國的使用者會看到「Eiffel Tower」促銷活動。

* **內容資料**，例如裝置型別(例如 裝置定位)、一天中的時間或工作階段詳細資訊。 例如，案頭使用者會收到案頭最佳化內容，而行動使用者則會收到行動最佳化內容。

* **對象**，可用來包含或排除具有特定對象成員資格的設定檔。

若要在行銷活動中設定目標定位，請遵循下列步驟。

1. 建立行銷活動。 [深入瞭解](../campaigns/create-campaign.md) <!--Add link to API triggered?-->

1. 從&#x200B;**[!UICONTROL 動作]**&#x200B;索引標籤中，選取至少一個動作。

1. 在&#x200B;**[!UICONTROL 訊息最佳化]**&#x200B;區段中，選取&#x200B;**[!UICONTROL 鎖定目標]**。

   ![](assets/msg-optimization-select-targeting.png){width=85%}

1. 使用規則產生器來定義條件。 例如，定義美國居民的規則、法國居民的規則以及印度居民的規則。

   ![](assets/msg-optimization-create-targeting.png){width=85%}

1. 視需要選取&#x200B;**[!UICONTROL 啟用遞補內容]**。 後援內容可讓您的對象在沒有符合定位規則時接收預設內容。 如果您未選取此選項，則不符合上述定位規則的任何對象都不會收到內容。

1. 儲存您的目標規則設定。

1. 回到行銷活動&#x200B;**[!UICONTROL 動作]**&#x200B;索引標籤，選取&#x200B;**[!UICONTROL 編輯內容]**。

1. 為您目標規則設定所定義的每個群組設計適當的內容。

   ![](assets/msg-optimization-targeting-design.png){width=85%}

   在此範例中，請為美國居民設計特定內容、為法國居民設計不同內容，並為印度居民設計其他內容。

1. [啟動](review-activate-campaign.md)您的行銷活動。

行銷活動上線後，會傳送為每個目標量身打造的內容，好讓美國居民收到特定訊息、法國居民收到不同訊息等。

<!--Default content:

* If no targeting rules match, default content can be delivered.

* If default content is not enabled, passthrough behavior ensures lower-priority campaigns are evaluated.-->

## 使用實驗 {#experimentation}

實驗可讓您測試多個內容版本，以根據預先定義的成功量度判斷哪些版本的執行效果最佳。

若要在行銷活動中設定實驗，請遵循下列步驟。

假設您想在行銷活動中測試下列促銷訊息：

* **處理A**：「下次購買可享受20%的優惠」
* **處理B**：「超過$50美元訂單的免運費」
* **處理C**：「取得您的$10禮品卡」

若要設定實驗並確定哪些訊息促成了最多購買，請遵循以下步驟。

1. 建立行銷活動。 [深入瞭解](../campaigns/create-campaign.md) <!--Add link to API triggered?-->

1. 從&#x200B;**[!UICONTROL 動作]**&#x200B;索引標籤中，選取至少兩個輸入動作，例如[程式碼型體驗](../code-based/get-started-code-based.md)和[應用程式內](../in-app/get-started-in-app.md)。

1. 在&#x200B;**[!UICONTROL 訊息最佳化]**&#x200B;區段中，選取&#x200B;**[!UICONTROL Experimentation]**。

   ![](assets/msg-optimization-select-experiment.png){width=85%}

1. 視需要設計和設定您的內容實驗。 [了解作法](../content-management/content-experiment.md)

   ![](assets/msg-optimization-create-experiment.png){width=85%}

   定義實驗後，實驗將套用至該行銷活動中插入的所有動作，這表示相同的客戶會在所有表面上看到相同的選件。

   >[!NOTE]
   >
   >您可以選取其他動作：實驗會套用至新增至行銷活動的所有動作。

1. [啟動](review-activate-campaign.md)您的行銷活動。

行銷活動上線後，使用者會被隨機指派不同的內容變數。 [!DNL Journey Optimizer]會追蹤哪些變數可推動更多購買，並提供可操作的深入分析。

使用[實驗行銷活動報告](../reports/campaign-global-report-cja-experimentation.md)追蹤行銷活動是否成功。

## 結合目標定位與實驗 {#combination}

Journey Optimizer也可讓您在單一行銷活動中結合目標定位和實驗，以建立更複雜的策略。

事實上，您可以使用目標定位來建立數個變體，並針對每個變體使用實驗來進一步最佳化每個內容。 這可確保實驗專屬於每個鎖定目標規則，且不會橫跨促銷活動中的變體。

例如，您可以針對美國客戶測試「促銷活動50%折扣」與「50美元禮品卡」，並針對歐洲客戶執行其他測試，例如「超過50歐元訂單的免運費」與「下次購買折扣20%」。

若要在行銷活動中同時結合目標定位和實驗，請遵循下列步驟。

1. 建立行銷活動，您可在此定義數個鎖定目標規則。 [了解作法](#targeting)

   ![](assets/msg-optimization-create-targeting.png){width=85%}

1. 為第一個鎖定目標規則建立實驗。

1. 視需要設計和設定您的內容實驗。 [了解作法](../content-management/content-experiment.md)

   ![](assets/msg-optimization-targeting-with-experiment.png){width=85%}

   定義實驗後，該實驗將僅適用於第一個目標規則。

1. 回到行銷活動&#x200B;**[!UICONTROL 動作]**&#x200B;索引標籤，選取&#x200B;**[!UICONTROL 編輯內容]**。

1. 對於您第一個鎖定目標規則所定義的群組，您可以為實驗的每個變體定義特定的內容。

   如果您將多個入站動作新增至行銷活動，則定位和實驗會套用至每個動作。 不過，您需要為每個動作的每個變體定義特定內容。

   ![](assets/msg-optimization-targeting-experiment-design.png){width=85%}

1. 以類似方式處理其他鎖定目標規則，並為每個變體設計對應的內容。

1. 儲存您的變更並[啟動](review-activate-campaign.md)您的行銷活動。

行銷活動上線後，每個目標群組的使用者會被隨機指派為其所屬群組定義的不同內容變數。

<!--
## Reporting on Message optimization

E.g. explaining how a marketer can look at the report to determine which treatment (e.g. which message content) is performing the best for the targeting audience
-->

