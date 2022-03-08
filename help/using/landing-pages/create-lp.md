---
title: 建立登陸頁面
description: 瞭解如何在Journey Optimizer配置和發佈登錄頁
feature: Landing Pages
topic: Content Management
role: User
level: Beginner
hidefromtoc: true
hide: true
exl-id: 18f9bdff-f5c6-4601-919d-4f3124e484b5
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '931'
ht-degree: 3%

---

# 建立和發佈登錄頁 {#create-lp}

>[!CAUTION]
>
>登錄頁目前僅可供選定用戶提前訪問。 如果您想利用此功能，請與Adobe客戶經理聯繫。

## 訪問登錄頁 {#access-landing-pages}

要訪問登錄頁清單，請選擇 **[!UICONTROL Journey Management]** > **[!UICONTROL Landing pages]** 的下界。

![](assets/lp_access-list.png)

的 **[!UICONTROL Landing Pages]** 清單顯示所有建立的項目。 您可以根據其狀態或修改日期來篩選它們。

![](assets/lp_access-list-filter.png)

## 建立登陸頁面 {#create-landing-page}

建立登錄頁的步驟如下。

1. 在登錄頁清單中，按一下 **[!UICONTROL Create landing page]**。

   ![](assets/lp_create-lp.png)

1. 添加標題。 如果需要，可以添加說明。

   ![](assets/lp_create-lp-details.png)

1. 選擇預設。

   ![](assets/lp_create-lp-presets.png)

   >[!NOTE]
   >
   >要定義登錄頁預設，請與Adobe客戶代表或 [Adobe客戶服務支援團隊](https://helpx.adobe.com/tw/enterprise/admin-guide.html/enterprise/using/support-for-experience-cloud.ug.html){target=&quot;_blank&quot;}。

1. 按一下「**[!UICONTROL Create]**」。

1. 顯示首頁及其屬性。 瞭解如何配置首頁設定 [這裡](#configure-primary-page)。

   ![](assets/lp_primary-page.png)

1. 按一下+表徵圖可添加子頁。 瞭解如何配置子頁設定 [這裡](#configure-subpages)。

   ![](assets/lp_add-subpage.png)

配置和設計 [首頁](#configure-primary-page)的 [子頁](#configure-subpages) 如果有，你可以 [test](#test-landing-page) 和 [發佈](#publish-landing-page) 登錄頁。

## 配置首頁 {#configure-primary-page}

首頁面是用戶按一下登錄頁面的連結後立即顯示給用戶的頁面，如電子郵件或網站。

要定義首頁設定，請執行以下步驟。

1. 可以更改頁面名稱， **[!UICONTROL Primary page]** 預設值。

1. 使用內容設計器編輯頁面的內容。 瞭解如何定義登錄頁內容 [這裡](design-lp.md)。

   ![](assets/lp_open-designer.png)

1. 定義登錄頁URL。 URL的第一部分要求執行域委派。 它已預填充，無法通過用戶介面編輯。 要設定它，請與Adobe帳戶代表或 [Adobe客戶服務支援團隊](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/support-for-experience-cloud.ug.html){target=&quot;_blank&quot;}。

   >[!CAUTION]
   >
   >登錄頁URL必須唯一。

   ![](assets/lp_access-url.png)

1. 您可以為頁面定義到期日期。 在這種情況下，必須在頁面到期時選擇操作：

   * **[!UICONTROL Redirect URL]**:輸入頁面過期時用戶將重定向到的頁面的URL。
   * **[!UICONTROL Custom page]**: [配置子頁](#configure-subpages) 並從顯示的下拉清單中選擇它。
   * **[!UICONTROL Browser error]**:鍵入將顯示的錯誤文本，而不是頁面。

   ![](assets/lp_expiry-date.png)

   <!--1. In the **[!UICONTROL Additional data]** section, define a **[!UICONTROL Key]** and the corresponding **[!UICONTROL Parameter value]**. // you can define how the data entered in the landing page is managed once it has been submitted by a user??-->

1. 如果您在 [設計首頁](design-lp.md)，它們顯示在 **[!UICONTROL Subscription list]** 的子菜單。

   ![](assets/lp_subscription-list.png)

1. 從登錄頁，您可以直接 [建立旅程](../building-journeys/journey-gs.md#jo-build) 在用戶提交表單時向其發送確認消息。 學習如何在此之後構建這樣的旅程 [用例](lp-use-cases.md#subscription-to-a-service)。

   ![](assets/lp_create-journey.png)

   按一下 **[!UICONTROL Create journey]** 要重定向到 **[!UICONTROL Journey Management]** > **[!UICONTROL Journeys]** 清單框。

## 配置子頁 {#configure-subpages}

最多可以添加2個子頁。 例如，您可以建立一個「感謝」頁面，在用戶提交表單後，該頁面將顯示，並且您可以定義一個錯誤頁面，如果登錄頁出現問題，將調用該錯誤頁面。

要定義子頁設定，請執行以下步驟。

1. 可以更改頁面名稱， **[!UICONTROL Subpage 1]** 預設值。

1. 使用內容設計器編輯頁面的內容。 瞭解如何定義登錄頁內容 [這裡](design-lp.md)。

1. 定義登錄頁URL。 URL的第一部分要求執行域委派。 它已預填充，無法通過用戶介面編輯。 要設定它，請與Adobe帳戶代表或 [Adobe客戶服務支援團隊](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/support-for-experience-cloud.ug.html){target=&quot;_blank&quot;}。

   >[!CAUTION]
   >
   >登錄頁URL必須唯一。

![](assets/lp_subpage-settings.png)

## Test登錄頁 {#test-landing-page}

定義登錄頁設定和內容後，可以使用test配置式預覽它。 如果插入 [個性化內容](../personalization/personalize.md)，您將能夠利用test配置檔案資料檢查登錄頁中此內容的顯示方式。

>[!CAUTION]
>
>您需要有test配置檔案才能預覽郵件和發送校樣。 瞭解如何 [建立test配置檔案](../building-journeys/creating-test-profiles.md)。

1. 在登錄頁介面中，按一下 **[!UICONTROL Preview & test]** 按鈕，來查看test配置檔案選擇。

   ![](assets/lp_preview-button.png)

   >[!NOTE]
   >
   >的 **[!UICONTROL Preview]** 按鈕也可以從內容設計器訪問。

1. 從 **[!UICONTROL Preview & test]** 螢幕中，選擇一個或多個test配置檔案。

   ![](assets/lp_test-profiles.png)

   選擇test配置檔案的步驟與測試消息時的步驟相同。 詳細資訊 [此部分](../messages/preview.md#select-test-profiles)。

1. 選擇 **[!UICONTROL Preview]** 頁籤 **[!UICONTROL Open preview]** test登錄頁。

   ![](assets/lp_open-preview.png)

1. 登錄頁的預覽將在新頁籤中開啟。 個性化元素被所選test配置檔案資料替換。

   ![](assets/lp_preview.png)

1. 選擇其他test配置檔案以預覽登錄頁的每個變體的呈現。

## 檢查警報 {#check-alerts}

在建立登錄頁時，在發佈前需要採取重要操作時，會發出警告。

警報顯示在螢幕的右上方，如下所示：

![](assets/lp_alerts.png)

>[!NOTE]
>
>如果未看到此按鈕，則未檢測到任何警報。

可以發生兩種類型的警報：

* **警告** 請參閱建議和最佳做法。 <!--For example, a message will display if -->

* **錯誤** 只要郵件未解決，就阻止您發佈。 例如，如果首頁URL丟失，則會收到警告。

<!--All possible warnings and errors are detailed [below](#alerts-and-warnings).-->

>[!CAUTION]
>
> 你需要解決所有 **錯誤** 發佈前發出警報。

<!--The settings and elements checked by the system are listed below. You will also find information on how to adapt your configuration to resolve the corresponding issues.

**Warnings**:

* 

**Errors**:

* 

>[!CAUTION]
>
> To be able to publish your message, you need to resolve all **error** alerts.
-->

## 發佈登錄頁 {#publish-landing-page}

登錄頁準備好後，您可以發佈它，使其在消息中可用。

![](assets/lp_publish.png)

>[!CAUTION]
>
>在發佈之前，請檢查並解決警報。 [了解更多](#check-alerts)

登錄頁發佈後，它將添加到登錄頁清單中 **[!UICONTROL Published]** 狀態。

它現在可以在 [!DNL Journey Optimizer] [消息](../messages/create-message.md) 將通過 [旅程](../building-journeys/journey.md)。

>[!NOTE]
>
>您可以通過特定報告監控登錄頁的影響。 [了解更多](lp-report.md)

