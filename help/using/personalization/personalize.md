---
title: 在 Journey Optimizer 中個人化內容
description: 開始使用個人化
feature: 個性化
topic: 個性化
role: Data Engineer
level: Beginner
source-git-commit: adb915a2013d1d1bf17ed5efb7ac4eb9c655c501
workflow-type: tm+mt
source-wordcount: '663'
ht-degree: 11%

---

# 開始使用個人化{#add-personalization}

探索[!DNL Adobe Journey Optimizer]個人化功能，運用您擁有的關於他/她的資料和資訊，讓您的訊息適應每個特定收件者。 這可以是他的名字，他的興趣，他住的地方，他買的東西，等等。

[!DNL :arrow_forward:] [了解如何個人化這些影片中的訊息](#video-perso)

[!DNL Journey Optimizer] 使用以 **** Handlebars為基礎的inlinesimple個人化語法，可讓您以雙大括弧{{}}括住的&#x200B;**內容建立運算式**。您可以在相同的內容或欄位中新增多個運算式，不受限制。 進一步了解[個人化語法](personalization-syntax.md)。

根據由 Adobe Experience Platform 定義的 **XDM 個人設定檔**&#x200B;方案管理的設定檔資料進行個人化。 有關詳細資訊，請參閱 [Adobe Experience Platform 資料模型 (XDM) 文件](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hant)。

>[!CAUTION]
>**XDM個別設定檔**&#x200B;結構是唯一可用來個人化[!DNL Journey Optimizer]中內容的結構。

**範例：**

* `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}`

* `Hello {{profile.person.name.fullName}}`

處理訊息（電子郵件和推播）時，Journey Optimizer會以Experience Cloud平台資料庫中包含的資料取代運算式： `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}`變成&quot;Hello John Doe&quot;。


## 個人化內容{#personalization-areas}

[!DNL Journey Optimizer]傳遞的訊息的內容和顯示可以幾種不同的方式進行個人化。

在具有編輯器圖示的每個欄位中，您可以開啟個人化編輯器（也稱為運算式編輯器）並定義個人化。

![](assets/perso_icon.png)

### 個人化您的電子郵件

建立電子郵件時，您可以在訊息的&#x200B;**電子郵件主旨**&#x200B;欄位中新增個人化。

![](assets/perso_subject.png)

在電子郵件設計工具中，您可以個人化內容：

* 在&#x200B;**message**&#x200B;中：按一下文字區塊內，按一下內容工具列中的&#x200B;**個人化**&#x200B;圖示，然後選取「插入個人化&#x200B;**」欄位。**&#x200B;如需電子郵件設計工具介面的詳細資訊，請參閱此[區段](../design-emails.md)。

   ![](assets/perso_insert.png)

* 對於&#x200B;**link**:選取文字區塊內的某些文字或影像，按一下內容工具列中的「插入連結&#x200B;**」圖示。**&#x200B;在視窗中，您可以按一下&#x200B;**新增個人化**&#x200B;圖示來新增個人化區塊。

   ![](assets/perso_link.png)

在這兩種情況下，您都可存取個人化編輯器。

![](assets/perso_ee.png)


### 個人化您的推播通知

您也可以在下列欄位中個人化您的&#x200B;**推播通知**:

* **標題**
* **主體**
* **自訂音效**
* **徽章**
* **自訂資料**

![](assets/perso_push.png)

進一步了解[此區段](../push-gs.md)中的推播通知設定。

## 使用運算式編輯器

運算式編輯器是[!DNL Journey Optimizer]中個人化的中心。

它適用於您需要定義電子郵件、推送和選件之類個人化的每個內容。

在運算式編輯器介面中，您將選取、排列、自訂及驗證所有資料，以針對您的內容建立自訂個人化。

![](assets/perso_ee1.png)

畫面左側會顯示網域選取器，供您選取個人化來源。 可用來源包括：

* **設定檔** :列出與Adobe Experience Platform資料模型(XDM)檔案中所述之設 [定檔架構相關聯的所有參考](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html)。
* **區段成員資格** :會列出在Adobe Experience Platform區段服務中建立的所有區段。[此處](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=en)提供分段的詳細資訊。
* **選件** :列出與特定版位相關聯的所有優惠方案。選取版位，然後在內容中插入優惠方案。 如需如何管理優惠方案的完整檔案，請參閱[此區段](../deliver-personalized-offers.md)。
* **內容** :在歷 **** 程中使用「訊息」活動時，此功能表中會提供內容歷程欄位。進一步了解[本節](personalization-use-case.md)。
* **輔助功能** :列出所有可用於對資料執行操作的輔助功能，如計算、資料格式或轉換、條件，以及在個人化環境中處理這些功能。進一步了解[本節](functions/functions.md)。

選取時，參考會新增到編輯器中。

>[!NOTE]
>
>「+」圖示旁的資訊圖示會開啟工具提示，提供每個變數的詳細資訊。

在下列範例中，運算式編輯器可讓您選取生日為今天的設定檔，然後透過插入與當天相對應的特定選件來完成自訂。

![](assets/perso_ee2.png)

## 作法影片{#video-perso}

了解如何使用歷程中的情境事件資訊來個人化訊息。

>[!VIDEO](https://video.tv.adobe.com/v/334165?quality=12)

了解如何使用歷程中的情境事件資訊來個人化訊息。

>[!VIDEO](https://video.tv.adobe.com/v/334078?quality=12)
