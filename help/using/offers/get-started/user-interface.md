---
title: 提供庫用戶介面
description: 瞭解有關提供庫用戶介面的詳細資訊
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 722f9c3b-b505-48c0-b126-31a7a841c245
source-git-commit: b5fa17bfc888236994e73474c35b1aaafcda3ebe
workflow-type: tm+mt
source-wordcount: '666'
ht-degree: 35%

---

# 提供庫用戶介面 {#user-interface}

的 **[!UICONTROL 決策管理]** 左滑軌部分提供了兩個菜單，可讓您訪問決策管理功能：

使用 **[!UICONTROL 優惠]** 管理和提供您的產品：


![](../assets/offers_menu.png)

* **[!UICONTROL 概述]**:新到 [!DNL decision management]? 按照螢幕上的步驟開始設定放置、優惠和收藏。 當已熟悉 [!DNL decision management]，獲取有關您最近的優惠、收集和決策的概述。 [了解更多](#overview)
* **[!UICONTROL 優惠]**:建立並訪問您的個性化和備用優惠。 瞭解如何建立 [提供](../offer-library/creating-personalized-offers.md) 和 [回退服務](../offer-library/creating-fallback-offers.md)
* **[!UICONTROL 集合]**:將您的產品組織為靜態和動態集合。 [了解更多](../offer-library/creating-collections.md)
* **[!UICONTROL 決定]**:建立和管理決策以提供您的產品。 [了解更多](../offer-activities/create-offer-activities.md)
* **[!UICONTROL 批量決策]**:向給定Adobe Experience Platform段中的所有配置檔案提供優惠決定。 [了解更多](../batch-delivery.md)
* **[!UICONTROL 模擬]**:通過模擬將哪些優惠交付給給定位置的test配置檔案來驗證您的決策邏輯。 [了解更多](../offer-activities/simulation.md)

使用 **[!UICONTROL 元件]** 菜單，用於建立和管理建立聘用和決策所需的元件：

![](../assets/offer_activities.png)

* **[!UICONTROL 放置]**:建立並管理將在其中顯示您的優惠的位置。 [了解更多](../offer-library/creating-placements.md)
* **[!UICONTROL 收集限定詞]**:建立和管理收集限定詞（以前稱為「標籤」），以組織和篩選您的優惠。 [了解更多](../offer-library/creating-tags.md)
* **[!UICONTROL 規則]**:管理您提供優惠的條件。 [了解更多](../offer-library/creating-decision-rules.md)
* **[!UICONTROL 排名]**:建立和管理排名公式，以確定應首先為給定位置提供哪項服務。 [了解更多](../ranking/create-ranking-formulas.md)

>[!NOTE]
>
>如果您在訪問決策管理或其某些功能時遇到問題，請與管理員用戶聯繫，確認您已被授予了所需的權限。 請參閱 [授予對決策管理的訪問權限](starting-offer-decisioning.md#granting-acess-to-decision-management)。

## 總覽 {#overview}

當您剛進入 [!DNL decision management]，也請參見Wiki頁。 **[!UICONTROL 概述]** 頁籤將引導您完成開始制定第一個聘用決定所需的主要步驟。 按照螢幕上的步驟開始建立放置、聘用和收藏。 完成這些第一步後，系統會提示您建立提供決策。

>[!NOTE]
>
>在中介紹了建立優惠和在決策中使用它們的主要步驟 [此部分](../offer-library/key-steps.md)。

當你更熟悉 [!DNL decision management] 你至少已經做出了一個報價決定 **[!UICONTROL 概述]** 頁籤顯示您最近的優惠、收集和決策。

按一下優惠或決定直接訪問選定項目的詳細資訊。

按一下 **[!UICONTROL 查看全部]** 按鈕，查看聘用、收集或決策清單。

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

請注意，您還可以複製現有優惠或決策，以便使用 **[!UICONTROL 草稿]** 狀態。 您可以從資訊窗格或優惠或決定的詳細檢視來執行此動作。

## 優惠和決定變更記錄 {#changes-logs}

「聘用庫」(Offer Library)允許您直觀地顯示對聘用或決策所做的所有更改。 為此，請按一下清單中的聘用或決定名稱，然後選擇 **[!UICONTROL 更改日誌]** 頁籤。

所有已進行的變更及執行變更的使用者名稱都會顯示在此畫面中。

![](../assets/change-logs.png)
