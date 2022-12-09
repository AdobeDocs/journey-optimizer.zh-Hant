---
solution: Journey Optimizer
product: journey optimizer
title: 關於運算式編輯器
description: 了解如何使用運算式編輯器。
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
exl-id: 1ac2a376-a3a8-41ae-9b04-37886697f0fc
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '330'
ht-degree: 0%

---

# 關於運算式編輯器 {#build-personalization-expressions}

>[!CONTEXTUALHELP]
>id="ajo_perso_editor"
>title="關於運算式編輯器"
>abstract="運算式編輯器可讓您選取、排列、自訂和驗證所有資料，以針對您的內容建立自訂的個人化。"

運算式編輯器是 [!DNL Journey Optimizer]. 它適用於您需要定義電子郵件、推送和選件之類個人化的每個內容。

在運算式編輯器介面中，您將選取、排列、自訂及驗證所有資料，以針對您的內容建立自訂個人化。

![](assets/perso_ee1.png)

畫面左側會顯示網域選取器，供您選取個人化來源。

![](assets/perso_ee3.png)

可用來源包括：

* **[!UICONTROL Profile attributes]** :列出與配置檔案架構相關的所有引用，如 [Adobe Experience Platform Data Model(XDM)檔案](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html){target=&quot;_blank&quot;}。
* **[!UICONTROL Segment memberships]** :會列出在Adobe Experience Platform劃分服務中建立的所有區段。 可用區段的詳細資訊 [此處](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html){target=&quot;_blank&quot;}。
* **[!UICONTROL Offer decisions]** :列出與特定版位相關聯的所有優惠方案。 選取版位，然後在內容中插入優惠方案。 如需如何管理優惠方案的完整檔案，請參閱 [本節](../email/add-offers-email.md).
* **[!UICONTROL Contextual attributes]** :在歷程中使用管道動作活動（電子郵件、推播、簡訊）時，您可透過此功能表取得內容歷程欄位。 深入了解 [本節](personalization-use-case.md).
* **[!UICONTROL Helper functions]** :列出所有可用於對資料執行操作的輔助功能，如計算、資料格式或轉換、條件，以及在個人化環境中處理這些功能。 深入了解 [本節](functions/functions.md).

按一下+按鈕，將屬性新增至編輯器。

>[!NOTE]
>
>「+」圖示旁的橢圓功能表可讓您取得每個變數的詳細資訊，並將最常使用的屬性新增至 [收藏夾](personalization-favorites.md).

![](assets/attribute-details.png)

在下列範例中，運算式編輯器可讓您選取生日為今天的設定檔，然後透過插入與當天相對應的特定選件來完成自訂。

![](assets/perso_ee2.png)

當您的個人化運算式準備就緒後，您必須由運算式編輯器驗證。 深入了解 [本節](personalization-validation.md).
