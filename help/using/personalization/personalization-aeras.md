---
title: Journey Optimizer中的個人化內容
description: 了解您可以新增個人化的內容
source-git-commit: 741fe2b614e3ded57c4a7ecd9b7333bdd99ab359
workflow-type: tm+mt
source-wordcount: '446'
ht-degree: 2%

---

# 個人化內容和工具{#personalization-areas}

![](../assets/do-not-localize/badge.png)

Journey Optimizer傳送的訊息內容和顯示可透過數種不同方式個人化。

與編輯器圖示相關聯的所有欄位都可以開啟個人化編輯器並接收個人化內容。

![](assets/perso_icon.png)

## 個人化您的電子郵件

建立電子郵件時，您可以在訊息的&#x200B;**電子郵件主旨**&#x200B;欄位中新增個人化。

![](assets/perso_subject.png)

在電子郵件設計工具中，您可以個人化內容：

* 在&#x200B;**message**&#x200B;中：按一下文字區塊內，按一下內容工具列中的&#x200B;**個人化**&#x200B;圖示，然後選取「插入個人化&#x200B;**」欄位。**&#x200B;如需電子郵件設計工具介面的詳細資訊，請參閱此[區段](../design-emails.md)。

   ![](assets/perso_insert.png)

* 對於&#x200B;**link**:選取文字區塊內的某些文字或影像，按一下內容工具列中的「插入連結&#x200B;**」圖示。**&#x200B;在視窗中，您可以按一下&#x200B;**新增個人化**&#x200B;圖示來新增個人化區塊。

   ![](assets/perso_link.png)

## 個人化推播通知

您也可以在下列欄位中個人化您的&#x200B;**推播通知**:

* **標題**
* **主體**
* **自訂音效**
* **徽章**
* **自訂資料**

![](assets/perso_push.png)

進一步了解[此區段](../create-push.md)中的推播通知設定。

## 使用運算式編輯器

運算式編輯器是Journey Optimizer中個人化的中心。

它適用於您需要定義電子郵件、推送和選件之類個人化的每個內容。

在運算式編輯器介面中，您將選取、排列、自訂及驗證所有資料，以針對您的內容建立自訂個人化。

![](assets/perso_ee1.png)

畫面左側會顯示網域選取器，供您選取個人化來源。

* **設定檔** :列出與Adobe Experience Platform資料模型(XDM)檔案中所述之設 [定檔架構相關聯的所有參考](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hant)。
* **區段成員資格** :會列出在Adobe Experience Platform區段服務中建立的所有區段。有關可用區段的詳細資訊，請前往[這裡](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=en)
* **選件** :列出與特定版位相關聯的所有優惠方案。選取版位，然後在內容中插入優惠方案。 如需如何管理優惠方案的完整檔案，請參閱[此區段](../deliver-personalized-offers.md)
* **內容** :在歷 **** 程中使用「訊息」活動時，此功能表中會提供內容歷程欄位。請參閱[此區段](personalization-use-case.md)
* **輔助功能** :列出所有可用於對資料執行操作的輔助功能，如計算、資料格式或轉換、條件，以及在個人化環境中處理這些功能。[了解更多](functions/functions.md)



選取時，參考會新增到編輯器中。

>[!NOTE]
>
>「+」圖示旁的資訊圖示會開啟工具提示，提供每個變數的詳細資訊。

在下列範例中，運算式編輯器可讓您選取生日為今天的設定檔，然後透過插入與當天相對應的特定選件來完成自訂。

![](assets/perso_ee2.png)




