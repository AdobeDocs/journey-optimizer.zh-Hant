---
title: 關於表達式編輯器
description: 瞭解如何使用表達式編輯器。
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
source-git-commit: 50e12a28ed9f94133a9810a460172d34ad3a4593
workflow-type: tm+mt
source-wordcount: '315'
ht-degree: 1%

---

# 關於表達式編輯器 {#build-personalization-expressions}

表達式編輯器是個性化的核心 [!DNL Journey Optimizer]。 它適用於您需要定義個性化的每個上下文，如電子郵件、推送和提供。

在表達式編輯器介面中，您將選擇、排列、自定義和驗證所有資料，以便為您的內容建立自定義個性化。

![](assets/perso_ee1.png)

螢幕的左側部分顯示一個域選擇器，用於選擇個性化的源。

![](assets/perso_ee3.png)

可用源包括：

* **[!UICONTROL Profile attributes]** :列出與中所述的配置檔案架構關聯的所有引用 [Adobe Experience Platform資料模型(XDM)文檔](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hant){target=&quot;_blank&quot;}。
* **[!UICONTROL Segment memberships]** :列出在Adobe Experience Platform分段服務中建立的所有段。 有關分段的詳細資訊 [這裡](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html){target=&quot;_blank&quot;}。
* **[!UICONTROL Offer decisions]** :列出與特定位置關聯的所有優惠。 選擇位置，然後在內容中插入聘用。 有關如何管理優惠的完整文檔，請參閱 [此部分](../deliver-personalized-offers.md)。
* **[!UICONTROL Contextual attributes]** :當 **消息** 在行程中使用，上下文行程欄位可通過此菜單使用。 瞭解詳情 [此部分](personalization-use-case.md)。
* **[!UICONTROL Helper functions]** :列出可用於對資料執行操作（如計算、資料格式化或轉換、條件）的所有幫助程式函式，並在個性化的上下文中對它們進行操作。 瞭解詳情 [此部分](functions/functions.md)。

在選擇時，將在編輯器中添加引用。

>[!NOTE]
>
>「+」表徵圖旁的「資訊」表徵圖開啟工具提示，提供每個變數的詳細資訊。
>
>可以將最頻率使用的屬性添加到收藏夾。 瞭解詳情 [此部分](personalization-favorites.md)。

在以下示例中，表達式編輯器允許您選擇今天有生日的配置檔案，然後通過插入與當天對應的特定優惠來完成自定義。

![](assets/perso_ee2.png)

個性化表達式準備好後，需要通過表達式編輯器驗證。 瞭解詳情 [此部分](personalization-validation.md)。