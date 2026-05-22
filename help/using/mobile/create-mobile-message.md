---
solution: Journey Optimizer
product: journey optimizer
title: 建立行動裝置訊息
description: 瞭解如何在Journey Optimizer中建立行動訊息
feature: SMS
topic: Content Management
role: User
level: Beginner
exl-id: 1f88626a-b491-4b36-8e3f-57f2b7567dd0
TQID: https://experienceleague.adobe.com/xgPlWorA3lsIF8ZBPHdg2UAK8cLKUsJO-2ONc7ZG8AU
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d556b755-390a-43f0-be32-a08cf6236126
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
subfeature_v2:
  - id: e5329d1b-e590-4e24-a3fb-ef3fe0f2c721
  - id: fa683eda-48de-4558-af32-2673edcd44fe
  - id: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 0201927f8d9260e8ba1d0db7014d6a7b30d09062
workflow-type: tm+mt
source-wordcount: 748
ht-degree: 2%

---

# 建立行動裝置訊息 {#create-sms}

>[!CONTEXTUALHELP]
>id="ajo_message_sms"
>title="建立行動裝置訊息"
>abstract="若要建立行動訊息，請在歷程或行銷活動中新增SMS動作，並開始使用個人化編輯器進行個人化。"

>[!AVAILABILITY]
>
>RCS不是HIPAA就緒服務，且不得用於收集、儲存或處理貴組織可能獲准在Journey Optimizer中處理的任何敏感個人資料，包括允許的健康資料，例如個人健康資訊。

您可以使用Adobe Journey Optimizer設計和傳送文字(SMS)、豐富通訊(RCS)和多媒體(MMS)訊息。 您首先需要在歷程或行銷活動中新增行動訊息動作，然後定義行動訊息的內容，如下所述。 Adobe Journey Optimizer也提供在傳送前測試行動訊息的功能，讓您可檢查轉譯、個人化屬性和所有其他設定。

根據業界標準及法規，所有SMS/RCS/MMS行銷訊息都必須包含讓收件者輕鬆取消訂閱的方式。 要執行此操作，簡訊收件者可以使用選擇加入和選擇退出關鍵字進行回覆。 [瞭解如何管理選擇退出](../privacy/opt-out.md#opt-out-decision-management)

## 新增行動裝置訊息 {#create-sms-journey-campaign}

瀏覽下列標籤，瞭解如何在行銷活動或歷程中新增行動訊息。

>[!BEGINTABS]

>[!TAB 新增行動訊息至歷程]

1. 開啟您的歷程，然後從浮動視窗的&#x200B;**[!UICONTROL 動作]**&#x200B;區段拖放&#x200B;**[!UICONTROL 動作]**&#x200B;活動。 深入瞭解[動作活動](../building-journeys/journey-action.md)。

   >[!IMPORTANT]
   >
   >舊版原生管道活動（電子郵件、推播、簡訊、應用程式內、網頁、程式碼型體驗和內容卡）自2026年3月版本起即已淘汰。 使用這些活動的現有歷程仍可繼續運作，不會有任何變更，無需移轉。

1. 選取&#x200B;**[!UICONTROL 行動訊息]**&#x200B;作為動作型別，然後按一下&#x200B;**[!UICONTROL 新增]**。

   ![](assets/sms_create_1.png)

1. 輸入&#x200B;**[!UICONTROL 標籤]**&#x200B;以識別您在歷程畫布中的動作。

1. 按一下&#x200B;**[!UICONTROL 設定動作]**&#x200B;按鈕。

1. 您被導向到&#x200B;**[!UICONTROL 動作]**&#x200B;標籤。 從那裡，選取或建立要使用的行動訊息設定。 [了解更多](mobile-configuration.md)

   ![](assets/sms_create_2.png)

1. 此外，您可以選取&#x200B;**[!UICONTROL 商業規則]**&#x200B;下拉式清單中的規則集，將上限規則套用至行動訊息動作。 [進一步了解](../conflict-prioritization/channel-capping.md)

1. 選取&#x200B;**[!UICONTROL 編輯內容]**&#x200B;按鈕，並視需要建立您的內容。 [了解更多](design-mobile.md)

1. 返回歷程畫布。 如有必要，請拖放其他動作或事件以完成您的歷程流程。 [了解更多](../building-journeys/about-journey-activities.md)

有關如何建立、設定和發佈歷程的詳細資訊，請參閱[此頁面](../building-journeys/journey-gs.md)。

>[!TAB 新增行動裝置訊息至行銷活動]

1. 存取&#x200B;**[!UICONTROL 促銷活動]**&#x200B;功能表，然後按一下&#x200B;**[!UICONTROL 建立促銷活動]**。

1. 選取您要執行的行銷活動型別

   * **已排程 — 行銷**：立即或在指定日期執行行銷活動。 已排程的行銷活動旨在傳送行銷訊息。 可從使用者介面設定及執行。

   * **API觸發 — 行銷/異動**：使用API呼叫執行行銷活動。 API觸發的行銷活動旨在傳送行銷或交易式訊息，也就是在個人執行動作後傳送的訊息：密碼重設、購物車購買等。

1. 從&#x200B;**[!UICONTROL 屬性]**&#x200B;區段，編輯行銷活動的&#x200B;**[!UICONTROL 標題]**&#x200B;和&#x200B;**[!UICONTROL 描述]**。

1. 從&#x200B;**[!UICONTROL 動作]**&#x200B;索引標籤，按一下&#x200B;**[!UICONTROL 新增動作]**&#x200B;並選擇&#x200B;**[!UICONTROL 行動訊息]**。 然後，選取或建立新組態。

   在[此頁面](mobile-configuration.md)上進一步瞭解行動訊息設定。

   ![](assets/sms_create_3.png)

1. 按一下&#x200B;**[!UICONTROL 建立實驗]**&#x200B;以開始設定您的內容實驗，並建立處理以測量其效能，並為您的目標對象識別最佳選項。 [了解更多](../content-management/content-experiment.md)

1. 在&#x200B;**[!UICONTROL 動作追蹤]**&#x200B;區段中，指定是否要追蹤行動訊息中連結的點按次數。

1. 在「**[!UICONTROL 對象]**」標籤中，按一下「**[!UICONTROL 選取對象]**」按鈕，從可用的Adobe Experience Platform對象清單定義要定位的對象。 [了解更多資訊](../audience/about-audiences.md)。

1. 在&#x200B;**[!UICONTROL 身分識別名稱空間]**&#x200B;欄位中，選擇要使用的名稱空間，以識別所選對象中的個人。 [了解更多](../event/about-creating.md#select-the-namespace)。

1. 從&#x200B;**[!UICONTROL 排程]**&#x200B;索引標籤，您可以將行銷活動設計成在特定日期或循環頻率執行。 在[本節](../campaigns/campaign-schedule.md#action-campaign-schedule)中瞭解如何設定行銷活動的&#x200B;**[!UICONTROL 排程]**。

1. 從&#x200B;**[!UICONTROL 動作觸發程式]**&#x200B;功能表，選擇行動訊息的&#x200B;**[!UICONTROL 頻率]**：

   * 一次
   * 每日
   * 每週
   * Month

您現在可以從&#x200B;**[!UICONTROL 編輯內容]**&#x200B;按鈕開始設計行動訊息的內容，如下所述。 [了解更多](design-mobile.md)

如需如何建立、設定和啟動行銷活動的詳細資訊，請參閱[此頁面](../campaigns/get-started-with-campaigns.md)。

>[!ENDTABS]

**相關主題**

* [設計行動裝置訊息](design-mobile.md)
* [在行銷活動中新增訊息](../campaigns/create-campaign.md)
* [預覽、測試及傳送您的行動裝置訊息](send-mobile-message.md)
* [設定行動訊息頻道](mobile-configuration.md)
* [行動訊息報表](../reports/journey-global-report-cja-sms.md)

