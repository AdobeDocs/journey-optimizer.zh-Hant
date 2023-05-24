---
solution: Journey Optimizer
product: journey optimizer
title: 建立登陸頁面
description: 瞭解如何在Journey Optimizer配置和發佈登錄頁
feature: Landing Pages
topic: Content Management
role: User
level: Beginner
keywords: 登錄，登錄頁，建立，發佈
exl-id: 18f9bdff-f5c6-4601-919d-4f3124e484b5
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '1539'
ht-degree: 28%

---

# 建立和發佈登錄頁 {#create-lp}

## 訪問登錄頁 {#access-landing-pages}

要訪問登錄頁清單，請選擇 **[!UICONTROL 旅程管理]** > **[!UICONTROL 登錄頁]** 的下界。

![](assets/lp_access-list.png)

的 **[!UICONTROL 登錄頁]** 清單顯示所有建立的項目。 您可以根據其狀態或修改日期來篩選它們。

![](assets/lp_access-list-filter.png)

在此清單中，您可以訪問 [登錄頁即時報告](../reports/lp-report-live.md) 或 [登錄頁全局報告](../reports/lp-report-global.md) 的子菜單。

您還可以刪除、複製和取消發佈登錄頁。

>[!CAUTION]
>
>如果取消發佈消息中引用的登錄頁，則指向登錄頁的連結將斷開，並顯示錯誤頁。

按一下登錄頁旁邊的三個點以選擇所需的操作。

![](assets/lp_access-list-actions.png)

>[!NOTE]
>
>無法刪除 [出版](#publish-landing-page) 登錄頁。 要刪除它，必須先取消發佈它。

## 建立登陸頁面 {#create-landing-page}

>[!CONTEXTUALHELP]
>id="ajo_lp_create"
>title="定義和設定您的登陸頁面"
>abstract="若要建立登陸頁面，您需要選取一個預設集，然後設定主要頁面和子頁面，最後在發佈頁面之前進行測試。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/landing-pages/lp-configuration/lp-presets.html#lp-create-preset" text="建立登陸頁面預設集"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/landing-pages/create-lp.html#publish-landing-page" text="發佈登陸頁面"

>[!CONTEXTUALHELP]
>id="ajo_lp_access_management_labels"
>title="為您的登陸頁面指派標籤"
>abstract="為了保護敏感的數位資產，您可以定義授權，以使用標籤來管理對登陸頁面的資料存取。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/access-control/object-based-access.html" text="物件等級存取控制"

建立登錄頁的主要步驟如下：

![](assets/lp-creation-process.png)

1. 在登錄頁清單中，按一下 **[!UICONTROL 建立登錄頁]**。

   ![](assets/lp_create-lp.png)

1. 添加標題。 如果需要，可以添加說明。

   ![](assets/lp_create-lp-details.png)

1. 要將自定義或核心資料使用標籤分配給登錄頁，請選擇 **[!UICONTROL 管理訪問]**。 [瞭解有關對象級訪問控制(OLAC)的詳細資訊](../administration/object-based-access.md)

   <!--You can add a tag. See AEP documentation?-->

1. 選擇預設。 瞭解如何在中建立登錄頁預設 [此部分](../landing-pages/lp-presets.md#lp-create-preset)。

   ![](assets/lp_create-lp-presets.png)

1. 按一下&#x200B;**[!UICONTROL 建立]**。

1. 顯示首頁及其屬性。 瞭解如何配置首頁設定 [這裡](#configure-primary-page)。

   ![](assets/lp_primary-page.png)

1. 按一下+表徵圖可添加子頁。 瞭解如何配置子頁設定 [這裡](#configure-subpages)。

   ![](assets/lp_add-subpage.png)

配置和設計 [首頁](#configure-primary-page)的 [子頁](#configure-subpages) 如果有，你可以 [test](#test-landing-page) 和 [發佈](#publish-landing-page) 登錄頁。

## 配置首頁 {#configure-primary-page}

>[!CONTEXTUALHELP]
>id="ajo_lp_primary_page"
>title="定義您的主要頁面設定"
>abstract="使用者點選您的登陸頁面連結 (例如從電子郵件或網站) 後，主要頁面會隨即向使用者顯示。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/landing-pages/landing-pages-design/design-lp.html" text="設計登陸頁面內容"

>[!CONTEXTUALHELP]
>id="ajo_lp_access_settings"
>title="定義您的登陸頁面 URL"
>abstract="在本區段中，定義一個唯一的登陸頁面 URL。URL 的第一部分需要您預先設定一個登陸頁面子網域作為您選取的預設集的一部分。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/landing-pages/lp-configuration/lp-subdomains.html" text="設定登陸頁面子網域"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/landing-pages/lp-configuration/lp-presets.html#lp-create-preset" text="建立登陸頁面預設集"

首頁面是用戶按一下登錄頁面的連結後立即顯示給用戶的頁面，如電子郵件或網站。

要定義首頁設定，請執行以下步驟。

1. 可以更改頁面名稱， **[!UICONTROL 首頁]** 預設值。

1. 使用內容設計器編輯頁面的內容。 瞭解如何定義登錄頁內容 [這裡](design-lp.md)。

   ![](assets/lp_open-designer.png)

1. 定義您的登陸頁面 URL. URL的第一部分要求您先前設定登錄頁子域作為 [預設](../landing-pages/lp-presets.md#lp-create-preset) 的上界。 [了解更多](../landing-pages/lp-subdomains.md)

   >[!CAUTION]
   >
   >登錄頁URL必須唯一。

   ![](assets/lp_access-url.png)

   >[!NOTE]
   >
   >即使已發佈，您也無法通過將此URL複製貼上到Web瀏覽器來訪問登錄頁。 相反，您可以使用預覽功能test它，如中所述 [此部分](#test-landing-page)。

1. 如果希望登錄頁預先載入已可用的表單資料，請選擇 **[!UICONTROL 預填充表單欄位，其中包含配置檔案資訊]**。

   ![](assets/lp_prefill-form-fields.png)

   啟用此選項後，如果配置檔案已選擇加入/退出或已添加到訂閱清單，則在顯示登錄頁時，將反映其選擇。

   例如，如果配置檔案選擇接收有關將來事件的通信，則在下次將登錄頁顯示到該配置檔案時，將已選中相應的複選框。

   ![](assets/lp_prefill-form-ex.png)

1. 您可以為頁面定義到期日期。 在這種情況下，必須在頁面到期時選擇操作：

   * **[!UICONTROL 重定向URL]**:輸入頁面過期時用戶將重定向到的頁面的URL。
   * **[!UICONTROL 自定義頁]**: [配置子頁](#configure-subpages) 並從顯示的下拉清單中選擇它。
   * **[!UICONTROL 瀏覽器錯誤]**:鍵入將顯示的錯誤文本，而不是頁面。

   ![](assets/lp_expiry-date.png)

1. 在 **[!UICONTROL 其他資料]** ，定義一個或多個鍵及其相應的參數值。 您將能夠使用 [表達式編輯器](../personalization/personalization-build-expressions.md)。 請參閱[此章節](lp-content.md#use-form-component#use-additional-data)深入瞭解。

   ![](assets/lp_create-lp-additional-data.png)

1. 如果您在 [設計首頁](design-lp.md)，它們顯示在 **[!UICONTROL 訂閱清單]** 的子菜單。

   ![](assets/lp_subscription-list.png)

1. 從登錄頁，您可以直接 [建立旅程](../building-journeys/journey-gs.md#jo-build) 在用戶提交表單時向其發送確認消息。 學習如何在此之後構建這樣的旅程 [用例](lp-use-cases.md#subscription-to-a-service)。

   ![](assets/lp_create-journey.png)

   按一下 **[!UICONTROL 建立行程]** 要重定向到 **[!UICONTROL 旅程管理]** > **[!UICONTROL 旅程]** 清單框。

## 配置子頁 {#configure-subpages}

>[!CONTEXTUALHELP]
>id="ajo_lp_subpage"
>title="定義子頁面設定"
>abstract="您最多可新增 2 個子頁面。例如，您可以建立一個「感謝」頁面，該頁面將在使用者提交表單後顯示，而且您可以定義一個錯誤頁面，如果登陸頁面出現問題，將呼叫該頁面。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/landing-pages/landing-pages-design/design-lp.html" text="設計登陸頁面內容"

>[!CONTEXTUALHELP]
>id="ajo_lp_access_settings-subpage"
>title="定義您的登陸頁面 URL"
>abstract="在本區段中，定義一個唯一的登陸頁面 URL。URL 的第一部分需要您預先設定一個登陸頁面子網域作為您選取的預設集的一部分。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/landing-pages/lp-configuration/lp-subdomains.html" text="設定登陸頁面子網域"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/landing-pages/lp-configuration/lp-presets.html#lp-create-preset" text="建立登陸頁面預設集"

您最多可新增 2 個子頁面。例如，您可以建立一個「感謝」頁面，該頁面將在使用者提交表單後顯示，而且您可以定義一個錯誤頁面，如果登陸頁面出現問題，將呼叫該頁面。

要定義子頁設定，請執行以下步驟。

1. 可以更改頁面名稱， **[!UICONTROL 子頁1]** 預設值。

1. 使用內容設計器編輯頁面的內容。 瞭解如何定義登錄頁內容 [這裡](design-lp.md)。

   >[!NOTE]
   >
   >可以從同一登錄頁的任何子頁插入指向首頁的連結。 例如，要重定向出錯並想重新訂閱的用戶，可以將確認子頁的連結添加到訂閱首頁。 瞭解如何在 [此部分](../email/message-tracking.md#insert-links)。

1. 定義您的登陸頁面 URL. URL的第一部分要求您先前設定登錄頁子域。 [了解更多](../landing-pages/lp-subdomains.md)

   >[!CAUTION]
   >
   >登錄頁URL必須唯一。

![](assets/lp_subpage-settings.png)

## Test登錄頁 {#test-landing-page}

>[!CONTEXTUALHELP]
>id="ac_preview_lp_profiles"
>title="預覽和測試您的登陸頁面"
>abstract="定義登陸頁面設定和內容後，您就可以使用測試設定檔進行預覽。 "
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/segment/profiles/creating-test-profiles.html" text="選取測試設定檔"

定義登錄頁設定和內容後，可以使用test配置式預覽它。 如果插入 [個性化內容](../personalization/personalize.md)，您將能夠使用test配置檔案資料檢查登錄頁中此內容的顯示方式。

>[!CAUTION]
>
>您必須具有test配置檔案才能預覽郵件和發送校樣。 瞭解如何 [建立test配置檔案](../segment/creating-test-profiles.md)。

1. 在登錄頁介面中，按一下 **[!UICONTROL 模擬內容]** 按鈕，來查看test配置檔案選擇。

   ![](assets/lp_simulate-button.png)

   >[!NOTE]
   >
   >的 **[!UICONTROL 模擬內容]** 按鈕也可以從內容設計器訪問。

1. 從 **[!UICONTROL 模擬]** 螢幕中，選擇一個或多個test配置檔案。

   ![](assets/lp_test-profiles.png)

   選擇test配置檔案的步驟與測試消息時的步驟相同。 詳細資訊 [此部分](../email/preview.md#select-test-profiles)。

1. 選擇 **[!UICONTROL 開啟預覽]** test登錄頁。

   ![](assets/lp_open-preview.png)

1. 登錄頁的預覽將在新頁籤中開啟。 個性化元素被所選test配置檔案資料替換。

   <!--![](assets/lp_preview.png)-->

1. 選擇其他test配置檔案以預覽登錄頁的每個變體的呈現。

## 檢查警報 {#check-alerts}

在建立登錄頁時，在發佈前必須執行重要操作時，會發出警告。

警報顯示在螢幕的右上方，如下所示：

![](assets/lp_alerts.png)

>[!NOTE]
>
>如果未看到此按鈕，則未檢測到任何警報。

可以發生兩種類型的警報：

* **警告** 請參閱建議和最佳做法。 <!--For example, a message will display if -->

* **錯誤** 只要未解決登錄頁，就阻止您發佈登錄頁。 例如，如果首頁URL丟失，則會收到警告。

<!--All possible warnings and errors are detailed [below](#alerts-and-warnings).-->

>[!CAUTION]
>
> 您必須解決所有 **錯誤** 發佈前發出警報。

<!--The settings and elements checked by the system are listed below. You will also find information on how to adapt your configuration to resolve the corresponding issues.

**Warnings**:

* 

**Errors**:

* 

>[!CAUTION]
>
> To be able to publish your message, you must resolve all **error** alerts.
-->

## 發佈登陸頁面 {#publish-landing-page}

登錄頁準備好後，您可以發佈它，使其在消息中可用。

![](assets/lp_publish.png)

>[!CAUTION]
>
>在發佈之前，請檢查並解決警報。 [了解更多](#check-alerts)

登錄頁發佈後，它將添加到登錄頁清單中 **[!UICONTROL 已發佈]** 狀態。

它現在可以在 [!DNL Journey Optimizer] 將通過 [旅程](../building-journeys/journey.md)。

>[!NOTE]
>
>您可以通過特定報告監控登錄頁的影響。 [了解更多](../reports/lp-report-live.md)

