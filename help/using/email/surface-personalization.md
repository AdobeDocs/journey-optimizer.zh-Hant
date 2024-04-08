---
solution: Journey Optimizer
product: journey optimizer
title: 設定電子郵件動態子網域
description: 瞭解如何在電子郵件頻道介面層級設定動態子網域
feature: Surface, Subdomains
topic: Administration
role: Admin
level: Experienced
keywords: 設定，電子郵件，設定，子網域
hide: true
hidefromtoc: true
badge: label="Beta"
exl-id: 1e004a76-5d6d-43a1-b198-5c9b41f5332c
source-git-commit: 94d39089d94b4fe42eb3fb95603426012b104517
workflow-type: tm+mt
source-wordcount: '815'
ht-degree: 0%

---

# 個人化電子郵件表面設定 {#surface-personalization}

為了增加彈性並控制您的電子郵件設定， [!DNL Journey Optimizer] 可讓您定義子網域和標題的個人化值<!--and URL tracking parameters--> 建立電子郵件介面時。

>[!AVAILABILITY]
>
>此功能目前僅供特定使用者測試版。 <!--To join the beta program, contact Adobe Customer Care.-->

## 新增動態子網域 {#dynamic-subdomains}

>[!CONTEXTUALHELP]
>id="ajo_surface_perso_not_available"
>title="無法使用個人化"
>abstract="此表面是在沒有任何個人化屬性的情況下建立的。 如需瞭解需要個人化時的解決步驟，請參閱檔案。"

>[!CONTEXTUALHELP]
>id="ajo_surface_dynamic_subdomain"
>title="啟用動態子網域"
>abstract="建立電子郵件表面時，您可以根據使用「運算式編輯器」定義的條件來設定動態子網域。 您最多可以新增50個動態子網域。"

>[!CONTEXTUALHELP]
>id="ajo_surface_dynamic_subdomain_list"
>title="部分子網域可能無法使用"
>abstract="由於暫止的回饋回圈註冊，某些子網域目前無法供選取。 此程式最多可能需要10個工作日。 完成後，您可以從所有可用的子網域中進行選擇。"

建立電子郵件介面時，您可以根據特定條件設定動態子網域。

例如，如果您有從每個國家/地區的專屬電子郵件地址傳送訊息的法律限制，則可以使用動態子網域。 這可讓您建立單一表面，其中包含對應不同國家/地區的數個傳送子網域，而非為每個國家/地區建立多個表面。 然後，您可以將不同國家/地區的目標客戶整合為單一行銷活動。

若要定義電子郵件頻道介面中的動態子網域，請遵循下列步驟。

1. 在建立介面之前，請先根據您的使用案例設定您要用於傳送電子郵件的子網域。 [了解作法](../configuration/about-subdomain-delegation.md)

   例如，假設您想針對不同的國家/地區使用不同的子網域：設定一個美國特定的子網域、一個英國特定的子網域等。

1. 建立管道表面。 [了解作法](../configuration/channel-surfaces.md)

1. 選取 **[!UICONTROL 電子郵件]** 頻道。

1. 在 **子網域** 區段，啟用 **[!UICONTROL 動態子網域]** 選項。

   ![](assets/surface-email-dynamic-subdomain.png)

1. 選擇第一個旁邊的編輯圖示 **[!UICONTROL 條件]** 欄位。

1. 此 [運算式編輯器](../personalization/personalization-build-expressions.md) 隨即開啟。 在此範例中，設定條件，例如 `Country` 等於 `US`.

   ![](assets/surface-email-edit-condition.png)

1. 選取您要與此條件關聯的子網域。 [進一步瞭解子網域](../configuration/about-subdomain-delegation.md)

   >[!NOTE]
   >
   >由於擱置中，某些子網域目前無法供選取 [回饋迴路](../reports/deliverability.md#feedback-loops) 註冊。 此程式最多可能需要10個工作日。 完成後，您可以從所有可用的子網域中進行選擇。 <!--where FL registration happens? is it when delegating a subdomain and you're awaiting from subdomain validation? or is it on ISP side only?-->

   ![](assets/surface-email-select-subdomain.png)

   所有位於美國的收件者都會收到使用該國家/地區所選子網域的訊息，這表示所有相關的URL （例如映象頁面、追蹤URL或取消訂閱連結）都會根據該子網域填入。

1. 視需要設定其他動態子網域。 您最多可以新增50個專案。

   ![](assets/surface-email-add-dynamic-subdomain.png)

   <!--Select the [IP pool](../configuration/ip-pools.md) to associate with the surface. [Learn more](email-settings.md#subdomains-and-ip-pools)-->

1. 定義所有其他專案 [電子郵件設定](email-settings.md) 和 [提交](../configuration/channel-surfaces.md#create-channel-surface) 您的表面。

將一或多個動態子網域新增至曲面後，系統會根據此曲面的已解析動態子網域填入下列專案：

* 所有URL （資源URL、映象頁面URL和追蹤URL）

* 此 [取消訂閱URL](email-settings.md#list-unsubscribe)

* 此 **來自電子郵件** 和 **錯誤電子郵件** 尾碼

>[!NOTE]
>
>如果您設定動態子網域，然後停用 **[!UICONTROL 動態子網域]** 選項，則會移除所有動態值。 選取子網域並提交表面，變更即可生效。

## 個人化您的頁首 {#personalize-header}

您也可以針對曲面中定義的所有標頭引數使用個人化。

例如，如果您有多個品牌，您可以建立單一介面，並對電子郵件標題使用個人化值。 這可讓您確保從不同品牌傳送的所有電子郵件都會傳送給每位客戶，而且正確無誤 **從** 名稱和電子郵件。 同樣地，當您的收件者點選 **回覆** 電子郵件使用者端軟體中的按鈕，您希望 **回覆** 名稱和電子郵件對應於正確使用者的正確品牌。

若要針對曲面標頭引數使用個人化變數，請遵循下列步驟。

>[!NOTE]
>
>您可以全部個人化 **[!UICONTROL 標頭引數]** 欄位，但 **[!UICONTROL 錯誤電子郵件前置詞]** 欄位。


1. 依照您通常的作法定義標頭引數。 [了解作法](email-settings.md#email-header)

1. 對於每個欄位，選取編輯圖示。

   ![](assets/surface-email-personalize-header.png)

1. 此 [運算式編輯器](../personalization/personalization-build-expressions.md) 隨即開啟。 依照需要定義條件，然後儲存變更。

   例如，設定條件，例如每位收件者都會收到來自其品牌代表的電子郵件。

   >[!NOTE]
   >
   >您只能選取 **[!UICONTROL 設定檔屬性]** 和 **[!UICONTROL 輔助函式]**.

1. 針對您想要新增個人化的每個引數，重複上述步驟。

>[!NOTE]
>
>如果您在曲面中新增一或多個動態子網域， **來自電子郵件** 和 **錯誤電子郵件** 將會根據解析的填入尾碼 [動態子網域](#dynamic-subdomains).

<!--
## Use personalized URL tracking {#personalize-url-tracking}

To use personalized URL tracking prameters, follow the steps below.

1. Select the profile attribute of your choice from the expression editor.

1. Repeat the steps above for each tracking parameter you want to personalize.

Now when the email is sent out, this parameter will be automatically appended to the end of the URL. You can then capture this parameter in web analytics tools or in performance reports.
-->

## 檢視表面詳細資料 {#view-surface-details}

在促銷活動或介面中使用具有個人化設定的介面時，您可以直接在促銷活動或介面中顯示介面細節。 請遵循下列步驟。

1. 建立電子郵件 [行銷活動](../campaigns/create-campaign.md) 或 [歷程](../building-journeys/journey-gs.md).

1. 選取 **[!UICONTROL 編輯內容]** 按鈕。

1. 按一下 **[!UICONTROL 檢視表面詳細資料]** 按鈕。

   ![](assets/campaign-view-surface-details.png)

1. 此 **[!UICONTROL 傳遞設定]** 視窗隨即顯示。 您可以檢視所有曲面設定，包括動態子網域和個人化的標頭引數。

   >[!NOTE]
   >
   >此畫面上的所有資訊都是唯讀的。

1. 選取 **[!UICONTROL 展開]** 以顯示動態子網域的詳細資訊。

   ![](assets/campaign-delivery-settings-subdomain-expand.png)
