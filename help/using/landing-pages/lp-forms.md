---
solution: Journey Optimizer
product: journey optimizer
title: 建立並使用適用於您的登陸頁面的表單
description: 瞭解如何在Journey Optimizer中建立和使用表單以供登陸頁面
feature: Landing Pages
topic: Content Management
role: User
level: Beginner
keywords: 登入，登陸頁面，建立，頁面，表單
badge: label="有限可用性" type="Informative"
hidefromtoc: true
hide: true
source-git-commit: 67283fe92282ce23c97c29fa2c0ad78132cc184a
workflow-type: tm+mt
source-wordcount: '1137'
ht-degree: 2%

---

# 在您的登入頁面中使用表單 {#lp-forms}

>[!AVAILABILITY]
>
>此功能為「有限可用性」的狀態。請聯絡您的 Adobe 代表以取得存取權。

若要使用您的[!DNL Journey Optimizer]登陸頁面擷取設定檔資料並擴充[!DNL Experience Platform]資料集，您可以在登陸頁面中運用表單。

## 建立表單預設集 {#create-form-preset}

>[!CONTEXTUALHELP]
>id="ajo_lp_form_connection"
>title="選取要使用的端點"
>abstract="定義在提交表單時傳送資料的串流端點。"
>additional-url="https://experienceleague.adobe.com/en/docs/experience-platform/sources/ui-tutorials/create/streaming/http" text="建立HTTP API串流連線"

>[!CONTEXTUALHELP]
>id="ajo_lp_form_dataset"
>title="選取資料集"
>abstract="定義要儲存並反映表單回應的資料集。 您可以輸入以搜尋特定資料集，或從清單中選取它。"

建立表單前，您需要先建立專屬的預設集，您可在其中選取傳送表單提交資料的連線端點，以及儲存透過表單擷取之資料的資料集。

當資料登陸串流端點時，會與資料集資訊連結。 然後會使用產生的來源/目標連線和來源流程，將資料推送至資料集。

建立預設集時：

* 您可以使用不同的資料集和串流連線組合，設定多個預設集。
* 相同的資料集或串流連線可在多個預設集中重複使用。
* 每個串流連線都會自動產生資源，例如：
   * **Source連線** — 資料來源。
   * **目標連線** — 資料儲存或使用的位置。
   * **Source流程** — 將資料從來源連線移至[!DNL Experience Platform]、處理對應、轉換和驗證的管道。

>[!NOTE]
>
> 若要存取及編輯表單預設集，您必須擁有生產沙箱的&#x200B;**[!UICONTROL 管理表單預設集]**&#x200B;許可權。 在[本節](../administration/high-low-permissions.md#administration-permissions).<!--TBC-->中進一步瞭解許可權

1. 若要存取&#x200B;**[!UICONTROL 表單預設集]**&#x200B;詳細目錄，請從左側功能表選取&#x200B;**[!UICONTROL 管理]** > **[!UICONTROL 管道]** >**[!UICONTROL 表單設定]**。

1. 按一下&#x200B;**[!UICONTROL 建立表單預設集]**。

1. 更新名稱以更輕鬆地擷取它，並視需要新增說明。

   ![](assets/lp_create-form-preset.png){width=80%}

1. 選取&#x200B;**[!UICONTROL 串流連線]**&#x200B;以用於該表單。 這是串流端點，資料會在提交表單時傳送至此處。

   >[!NOTE]
   >
   >在[Experience Platform檔案](https://experienceleague.adobe.com/en/docs/experience-platform/sources/ui-tutorials/create/streaming/http){target="_blank"}中進一步瞭解如何建立串流來源連線。

1. 選取&#x200B;**[!UICONTROL 資料集]**&#x200B;以連結表單。 這是將儲存並反映表單回應的位置。 您可以輸入以搜尋特定資料集，或從清單中選取它。

   >[!NOTE]
   >
   >目前只有[!DNL Adobe Experience Platform]個資料集可供選取。 一次只能選取一個資料集。

1. 按一下&#x200B;**[!UICONTROL 發佈]**。 您的預設集現已準備就緒，可用於表單中。

## 存取及管理表單 {#access-forms}

若要存取表單清單，請從左側功能表選取&#x200B;**[!UICONTROL 內容管理]** > **[!UICONTROL Forms]**。

所有現有表單都會顯示。 您可以根據表單的狀態、建立或修改日期來篩選表單。

## 建立及設計表單 {#create-form}

>[!CONTEXTUALHELP]
>id="ajo_lp_form_preset"
>title="選取預設集"
>abstract="選擇預先定義的預設集，其中包含要使用的連線，以及表單預先定義的資料集。"
>additional-url="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/landing-pages/lp-forms#create-form-preset" text="建立表單預設集"

若要建立表單，請遵循下列步驟。

1. 從&#x200B;**[!UICONTROL Forms]**&#x200B;清單中，按一下&#x200B;**[!UICONTROL 建立表單]**。

1. 新增名稱。 您可以視需要新增說明。

   ![](assets/lp_create-form.png)

1. 選取&#x200B;**[!UICONTROL 預設集]**，其中包含要使用的連線以及表單的預先定義資料集。 [瞭解如何建立表單預設集](#create-form-preset)

1. 按一下&#x200B;**[!UICONTROL 建立]**。

   <!--![](assets/lp_create-form-filled.png){width=50%}-->

1. 表單設計工具隨即開啟。 新增[元件](../email/content-components.md#add-content-components)以建置您的表單內容。 您可以使用[Text](../email/content-components.md#text)元件和&#x200B;**[!UICONTROL Field]**&#x200B;元件。

1. 使用&#x200B;**[!UICONTROL 欄位]**&#x200B;元件，您可以根據選取的資料集結構描述選取屬性。

   >[!NOTE]
   >
   >若要將收集的資料與設定檔對應，請選取設定檔身分欄位。 若要識別屬性清單中的身分識別欄位，請尋找標示為&#x200B;**[!UICONTROL 必要]**.<!--Explain-->的欄位

   例如，您可以設定電子郵件和人員ID。 當使用者填寫這些欄位時，輸入的資訊會儲存到所選的資料集。

   ![](assets/lp_create-form-fields.png)

1. 您可以指定每個&#x200B;**[!UICONTROL 欄位詳細資料]**，例如指示、預設值、驗證訊息、最大長度等。

   ![](assets/lp_create-form-field-details.png)

1. 您可以使用&#x200B;**[!UICONTROL 樣式]**&#x200B;窗格，視需要調整表單的版面、樣式和維度。 [進一步瞭解樣式](../email/get-started-email-style.md)

1. 按一下&#x200B;**[!UICONTROL 儲存並關閉]**。

1. 設定感謝頁面。 [了解作法](#thank-you-page)

1. **[!UICONTROL 發佈]**&#x200B;表單，使其可在登陸頁面中選擇。

### 設定感謝頁面 {#thank-you-page}

>[!CONTEXTUALHELP]
>id="ajo_lp_forms_thankyou_page"
>title="感謝頁面"
>abstract="設定某人填寫或轉寄表單時所發生的情況。"

在&#x200B;**[!UICONTROL 感謝頁面]**&#x200B;區段中，設定使用者填寫表單時會發生什麼情況。

![](assets/lp_create-form-thank-you.png){width=70%}

設定下列其中一個動作：

* **[!UICONTROL 停留在頁面]** — 此選項可讓訪客在提交表單時停留在相同頁面。
* **[!UICONTROL 登陸頁面]** — 選取已發佈的[登陸頁面](create-lp.md)，使用者在提交表單後會重新導向該頁面。
* **[!UICONTROL 外部URL]** — 輸入您要作為後續頁面的完整URL。 使用者提交表單後，系統會將他們導向指定的URL。
* **[!UICONTROL 條件式重新導向]** — 設定規則，以根據表單回應動態顯示不同的後續動作。

  您可以為每個特定對象定義規則。 例如，您可以為美國居民顯示特定登陸頁面、為加拿大居民顯示另一個頁面，以此類推。 最後，針對未落入您定義之任何規則的使用者，設定預設動作。

  >[!NOTE]
  >
  >系統會依序讀取規則中定義的條件。

  ![](assets/lp_create-form-thank-you-conditional.png){width=40%}

## 在登入頁面中運用表單 {#leverage-form-in-lp}

您現在可以將此表單內嵌至登入頁面，以擷取與您在表單中定義的屬性對應的資料，並將其儲存至選取的資料集。 請遵循下列步驟。

1. 建立登入頁面。 [了解作法](create-lp.md#create-landing-page)

1. 選取&#x200B;**[!UICONTROL 資料擷取]**&#x200B;做為登陸頁面型別，然後按一下&#x200B;**[!UICONTROL 建立]**。

   ![](assets/lp_create-lp-data-capture.png){width=65%}

1. 設定主要頁面。 [了解作法](create-lp.md#configure-primary-page)

1. 開啟[登陸頁面設計工具](design-lp.md)。

1. 將&#x200B;**[!UICONTROL 結構元件]**&#x200B;拖放到您的內容中。 將&#x200B;**[!UICONTROL Form]**&#x200B;元件拖放到該結構中。

   >[!NOTE]
   >
   >登入頁面中只能選取已發佈的表單。

1. 在&#x200B;**[!UICONTROL 內嵌表單]**&#x200B;區段中，選取您建立的表單。

   ![](assets/lp_embed-form.png)

   >[!NOTE]
   >
   >您可以使用&#x200B;**[!UICONTROL 編輯表單]**&#x200B;按鈕更新選取的表單。 表單會在新標籤中開啟。 編輯表單內容的步驟與[此區段](#create-form)中說明的步驟相同。

1. 在&#x200B;**[!UICONTROL 後續追蹤型別]**&#x200B;區段中，設定使用者填寫表單時會發生什麼情況：

   * 選擇&#x200B;**[!UICONTROL 已定義的表單]**&#x200B;以選取內嵌表單中已定義的動作。 [了解更多](#thank-you-page)

   * 您也可以選取已發佈的[登陸頁面](create-lp.md)，使用者在提交表單後會重新導向該頁面。

   * 或者，將&#x200B;**[!UICONTROL 外部URL]**&#x200B;定義為後續頁面，當使用者提交表單時，會導向該頁面。

1. 儲存並測試您的登入頁面。 [了解作法](create-lp.md#test-landing-page)

一旦您的登入頁面已[發佈](create-lp.md#publish-landing-page)並用於歷程中，當使用者填寫表單時，輸入的資訊會擷取到選取的資料集中。

>[!NOTE]
>
>如果您取消發佈用於登入頁面的表單，編輯此表單並再次發佈，則登入頁面一律使用最新發佈的表單版本。
