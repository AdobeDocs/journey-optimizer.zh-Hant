---
title: Journey Optimizer的個人化背景
description: 瞭解您可以在哪些內容中新增個人化
translation-type: tm+mt
source-git-commit: 568b37f0bbcb663cf7062f26b90d57d89452e862
workflow-type: tm+mt
source-wordcount: '407'
ht-degree: 2%

---

# 個人化區域{#personalization-areas}

![](../assets/do-not-localize/badge.png)

Journey Optimizer傳遞的資訊內容和顯示可以通過幾種不同的方式實現個性化。

所有與編輯器表徵圖關聯的欄位都可以開啟個性化編輯器並接收個性化內容。

![](assets/perso_icon.png)

## 個人化您的電子郵件

在建立電子郵件渠道訊息期間，**電子郵件主旨**&#x200B;欄位可個人化。

![](assets/perso_subject.png)

在電子郵件設計人員中，您可以個人化內容：

* 在&#x200B;**message**&#x200B;中：在文字區塊內按一下，按一下內容相關工具列中的「個人化&#x200B;****」圖示，然後選取「插入個人化&#x200B;**」欄位。**&#x200B;有關「電子郵件設計器」介面的詳細資訊，請參閱[部分](../design-emails.md)。

   ![](assets/perso_insert.png)

* 對於&#x200B;**link**:在文字區塊中選取某些文字或影像，按一下內容相關工具列中的「插入連結」(**Insert)連結**&#x200B;圖示。 在窗口中，可以通過按一下&#x200B;**添加個性化**&#x200B;表徵圖添加個性化塊。

   ![](assets/perso_link.png)

## 個人化推播通知

在&#x200B;**推播頻道**&#x200B;中，個人化可讓您微調您的推播通知。

您可以在下列欄位中新增個人化：

* **標題**
* **身體**
* **自訂音效**
* **標章**
* **自訂資料**

![](assets/perso_push.png)

有關推播通知配置的完整文檔，請參閱[本節](../configure-push.md)。


## 使用運算式編輯器

表情編輯是Journey Optimizer個人化的核心。

它適用於您需要定義個人化（例如電子郵件、推播和優惠）的每個環境。

在運算式編輯器介面中，您將選取、排列、自訂和驗證所有資料，為您的內容建立自訂的個人化。

![](assets/perso_ee1.png)

畫面的左側會顯示網域選擇器，供您選取個人化來源。

* **設定檔** :列出與Adobe Experience Platform資料模型(XDM)文檔中描述的 [配置檔案模式相關的所有引用](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hant)。
* **區段會籍** :列出在「Adobe Experience Platform區段」服務中建立的所有區段。有關區段的詳細資訊[此處](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=en)
* **選件** :列出與特定位置相關的所有選件。選取位置，然後將選件插入內容中。 有關如何管理選件的完整說明檔案，請參閱[本節](https://experienceleague.adobe.com/docs/customer-journey-management/using/create-messages/deliver-personalized-offers.html?lang=en#about-offer-decisioning)

在選取時，參考會新增至編輯器中。

>[!NOTE]
>
>「+」圖示旁的資訊圖示會開啟工具提示，提供每個變數的詳細資訊。

在下列範例中，運算式編輯器可讓您選取今天有生日的描述檔，然後插入與當天對應的特定選件以完成自訂。

![](assets/perso_ee2.png)




