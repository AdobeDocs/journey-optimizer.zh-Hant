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
source-git-commit: c082d9329949fd8dc68929e3934daf2d9dfdbd46
workflow-type: tm+mt
source-wordcount: '612'
ht-degree: 0%

---

# 設定電子郵件動態子網域 {#surface-personalization}

建立電子郵件介面時，為了增加彈性並控制電子郵件設定， [!DNL Journey Optimizer] 可讓您定義子網域、標題和URL追蹤引數的個人化值。

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

若要定義動態子網域，請遵循下列步驟。

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

   所有在美國的收件者都會收到使用該國家/地區所選子網域的訊息，這表示所有相關的URL （例如映象頁面、追蹤URL或取消訂閱連結）都會根據該子網域填入。

1. 視需要設定其他動態子網域。 您最多可以新增50個專案。

   ![](assets/surface-email-add-dynamic-subdomain.png)

1. 選取 [IP集區](../configuration/ip-pools.md) 以與曲面相關聯。 [了解更多](email-settings.md#subdomains-and-ip-pools)

將一或多個動態子網域新增至曲面後，系統會根據此曲面的已解析動態子網域填入下列專案：

* 所有URL （資源URL、映象頁面URL和追蹤URL）

* 此 [取消訂閱URL](email-settings.md#list-unsubscribe)

* 此 **來自電子郵件** 和 **錯誤電子郵件** 尾碼

## 個人化您的標題(#personalize-header)

您也可以針對曲面中定義的所有標頭引數使用個人化。

例如，如果您有多個品牌，您可以建立單一介面，並對電子郵件標題使用個人化值。 這可讓您確保從不同品牌傳送的所有電子郵件都會傳送給每位客戶，而且正確無誤 **從** 名稱和電子郵件。 同樣地，當您的收件者點選 **回覆** 電子郵件使用者端軟體中的按鈕，您希望 **回覆** 名稱和電子郵件對應於正確使用者的正確品牌。

若要針對曲面標頭引數使用個人化變數，請遵循下列步驟。

1. 依照您通常的作法定義標頭引數。 [了解作法](email-settings.md#email-header)

1. 對於每個欄位，選取編輯圖示。

   ![](assets/surface-email-personalize-header.png)

1. 此 [運算式編輯器](../personalization/personalization-build-expressions.md) 隨即開啟。 依照需要定義條件，然後儲存變更。<!--In this example, set a condition such as -->

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

select the profile attribute of your choice from the expression editor.

1. Repeat the steps above for each tracking parameter you want to personalize.

Now when the email is sent out, this parameter will be automatically appended to the end of the URL. You can then capture this parameter in web analytics tools or in performance reports.
-->
