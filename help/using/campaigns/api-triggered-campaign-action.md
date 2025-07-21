---
solution: Journey Optimizer
product: journey optimizer
title: 設定API觸發的行銷活動動作
description: 瞭解如何設定API觸發的行銷活動動作。
feature: Campaigns, API
topic: Content Management
role: Developer
level: Experienced
keywords: 行銷活動， API觸發， REST，最佳化工具，訊息
source-git-commit: 1bdba8c5c1a9238d351b159551f6d3924935b339
workflow-type: tm+mt
source-wordcount: '425'
ht-degree: 7%

---


# 設定API觸發的行銷活動動作 {#api-action}

使用&#x200B;**[!UICONTROL 動作]**&#x200B;索引標籤選取訊息的通道設定，並設定其他設定，例如追蹤、內容實驗或多語言內容。

1. **選擇頻道**。

   導覽至&#x200B;**[!UICONTROL 動作]**&#x200B;標籤，按一下&#x200B;**[!UICONTROL 新增動作]**&#x200B;按鈕並選取通訊通道。

   ![](assets/api-triggered-channel.png)

   >[!NOTE]
   >
   >可用的通道因您的授權模式及附加元件而異。
   >
   >針對API觸發的行銷活動，只有電子郵件、簡訊和推播通知通道可用。

1. **選取通道設定**

   設定是由[系統管理員](../start/path/administrator.md)所定義。 它包含所有用於傳送訊息的技術參數，如標頭參數、子網域、行動應用程式等等。[瞭解如何設定頻道設定](../configuration/channel-surfaces.md)

   ![](assets/create-campaign-action.png)

1. **建立內容實驗**

   使用&#x200B;**[!UICONTROL 內容實驗]**&#x200B;區段來定義多個傳遞處理，以測量哪個傳遞處理對目標對象執行得最好。 按一下&#x200B;**[!UICONTROL 建立實驗]**&#x200B;按鈕，然後依照本節詳述的步驟進行： [建立內容實驗](../content-management/content-experiment.md)。

1. **新增多語言內容**

   使用&#x200B;**[!UICONTROL 語言]**&#x200B;區段在您的行銷活動中以多種語言建立內容。 若要這麼做，請按一下&#x200B;**[!UICONTROL 新增語言]**&#x200B;按鈕，然後選取所需的&#x200B;**[!UICONTROL 語言設定]**。 本節提供如何設定及使用多語言功能的詳細資訊： [開始使用多語言內容](../content-management/multilingual-gs.md)

根據所選的通訊通道，有其他設定可供使用。 請展開下列各節以取得詳細資訊。

+++**套用上限規則** （電子郵件、推播、簡訊）

在&#x200B;**[!UICONTROL 商業規則]**&#x200B;下拉式清單中，選取要套用上限規則至行銷活動的規則集。 運用管道規則集，可讓您根據通訊型別設定頻率上限，以防止訊息相似的客戶超載。 [學習如何使用規則集](../conflict-prioritization/rule-sets.md)

+++

+++**追蹤參與** （電子郵件、簡訊）。

使用&#x200B;**[!UICONTROL 動作追蹤]**&#x200B;區段來追蹤收件者對您的電子郵件或簡訊傳遞的反應。 執行行銷活動後，即可從行銷活動報表存取追蹤結果。 [進一步瞭解行銷活動報告](../reports/campaign-global-report-cja.md)

+++

+++**啟用快速傳遞模式** （推播）。

快速傳送模式是[!DNL Journey Optimizer]附加元件，允許透過行銷活動以非常快的速度傳送大量推送訊息。 當您想要在行動電話上傳送緊急推播警報（例如傳送重大新聞給已安裝您新聞頻道應用程式的使用者）時，如果訊息傳送延遲對業務至關重要，則會使用快速傳送。 如需使用快速傳遞模式時效能的詳細資訊，請參閱[Adobe Journey Optimizer產品說明](https://helpx.adobe.com/tw/legal/product-descriptions/adobe-journey-optimizer.html)。

+++

## 後續步驟 {#next}

準備好行銷活動設定和內容後，您就可以設計其內容。 [了解更多](api-triggered-campaign-content.md)
