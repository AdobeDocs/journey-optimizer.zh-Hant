---
title: 使用者介面
description: 深入了解優惠方案庫使用者介面
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 722f9c3b-b505-48c0-b126-31a7a841c245
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '662'
ht-degree: 35%

---

# 使用者介面 {#user-interface}

此 **[!UICONTROL 決策管理]** 區段（位於左側邊欄）提供兩個功能表，供您存取決策管理功能：

使用 **[!UICONTROL 選件]** 功能表來管理和傳送優惠方案：


![](../assets/offers_menu.png)

* **[!UICONTROL 概述]**:新增至 [!DNL decision management]? 請依照畫面上的步驟，開始設定版位、選件和系列。 已熟悉時 [!DNL decision management]，取得最新選件、集合和決策的概觀。 [了解更多](#overview)
* **[!UICONTROL 選件]**:建立並存取您的個人化和備援優惠方案。 了解如何建立 [優惠](../offer-library/creating-personalized-offers.md) 和 [回退優惠方案](../offer-library/creating-fallback-offers.md)
* **[!UICONTROL 集合]**:將優惠方案組織為靜態和動態集合。 [了解更多](../offer-library/creating-collections.md)
* **[!UICONTROL 決策]**:建立和管理傳遞優惠方案的決策。 [了解更多](../offer-activities/create-offer-activities.md)
* **[!UICONTROL 批次決策]**:將優惠方案決策傳送至指定Adobe Experience Platform區段中的所有設定檔。 [了解更多](../batch-delivery.md)
* **[!UICONTROL 模擬]**:模擬哪些優惠方案將傳遞至指定位置的測試設定檔，以驗證決策邏輯。 [了解更多](../offer-activities/simulation.md)

使用 **[!UICONTROL 元件]** 功能表，用來建立和管理建立選件和決策所需的元件：

![](../assets/offer_activities.png)

* **[!UICONTROL 版位]**:建立和管理將顯示優惠方案的版位。 [了解更多](../offer-library/creating-placements.md)
* **[!UICONTROL 收集限定符]**:建立和管理集合限定符（先前稱為「標籤」），以組織和篩選您的優惠方案。 [了解更多](../offer-library/creating-tags.md)
* **[!UICONTROL 規則]**:管理顯示優惠方案的條件。 [了解更多](../offer-library/creating-decision-rules.md)
* **[!UICONTROL 排名]**:建立並管理排名公式，以決定應先針對指定版位呈現哪個優惠方案。 [了解更多](../ranking/create-ranking-formulas.md)

>[!NOTE]
>
>如果您在存取決策管理或其部分功能時遇到問題，請向管理員使用者確認您已獲得必要的權限。 請參閱 [授予Decision Management的存取權](starting-offer-decisioning.md#granting-acess-to-decision-management).

## 總覽 {#overview}

當您剛接觸 [!DNL decision management], **[!UICONTROL 概述]** 標籤會引導您完成開始建立第一個優惠方案決策所需的主要步驟。 請依照畫面上的步驟開始建立版位、優惠方案和集合。 完成前述步驟後，系統會提示您建立選件決策。

>[!NOTE]
>
>建立選件及在決策中使用選件的主要步驟顯示在 [本節](../offer-library/key-steps.md).

當您更熟悉 [!DNL decision management] 而您已建立至少一個選件決策， **[!UICONTROL 概述]** 索引標籤會顯示您最近的選件、集合和決策。

按一下選件或決定直接存取所選項目的詳細資訊。

按一下 **[!UICONTROL 查看全部]** 按鈕來存取選件、集合或決策清單。

![](../assets/overview_view-all.png)

## 搜尋和篩選資訊 {#search-and-filter-information}

使用&#x200B;**搜尋列**&#x200B;來尋找特定項目。

按一下清單左上方的篩選圖示，即可存取 **篩選器**。可讓您根據不同的標準篩選顯示的元素。例如，您可以篩選為電子郵件通訊頻道和影像類型內容所建立的位置。

![](../assets/filters.png)

## 自訂顯示的資訊 {#customize-displayed-information}

可使用清單右上角的設定按鈕個人化「決定管理」功能表中的清單。

可讓您根據需求選擇要顯示的資訊。

請注意，會針對每位使用者儲存欄位自訂。

![](../assets/columns.png)

## 資訊窗格 {#information-pane}

在不同的清單中選取元素以顯示資訊窗格，讓您擷取資訊並對元素執行基本動作。

![](../assets/information-pane.png)

優惠與決定清單還可讓您對多個元素執行批量動作。若要這麼做，請選取所要的優惠或決定，然後從資訊窗格中選取您要執行的動作。

請注意，您也可以複製現有選件或決策，以便使用 **[!UICONTROL 草稿]** 狀態。 您可以從資訊窗格或優惠或決定的詳細檢視來執行此動作。

## 優惠和決定變更記錄 {#changes-logs}

優惠方案程式庫可讓您視覺化對優惠方案或決策所做的所有變更。 若要這麼做，請按一下清單中的選件名稱，然後選取 **[!UICONTROL 變更記錄]** 標籤。

所有已進行的變更及執行變更的使用者名稱都會顯示在此畫面中。

![](../assets/change-logs.png)
