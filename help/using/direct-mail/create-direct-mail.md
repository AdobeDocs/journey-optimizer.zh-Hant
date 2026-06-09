---
solution: Journey Optimizer
product: journey optimizer
title: 建立新的直接郵件訊息
description: 瞭解如何在 Journey Optimizer 建立直接郵件訊息
feature: Direct Mail
topic: Content Management
role: User
level: Beginner
keywords: 直接郵件, 訊息, 行銷活動
exl-id: 6b438268-d983-4ab8-9276-c4b7de74e6bd
TQID: https://experienceleague.adobe.com/vn-PhvuksTX-ALADGGwGlvtp7-dTgjFVsIVvucAjLa8
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2:
  - id: f8d2e9f0-69c9-40cd-890f-71336c8dfff7
  - id: cb1f1586-9fb4-4de2-8332-02cebb88d42d
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: a4e4f5ca5c3eb9dbfb5691cb5de420009ed7e5a5
workflow-type: tm+mt
source-wordcount: 1132
ht-degree: 16%

---

# 建立新的直接郵件訊息 {#create-direct}

>[!CONTEXTUALHELP]
>id="ajo_direct_mail"
>title="直接郵件建立"
>abstract="在排程的行銷活動和歷程中建立直接郵件訊息，並設計直接郵件提供者向您客戶傳送郵件所需的摘取檔案。"

>[!CONTEXTUALHELP]
>id="ajo_journey_direct_mail"
>title="結束活動"
>abstract="直接郵件是離線管道，可讓您個人化和產生第三方直接郵件提供者傳送郵件給客戶所需的擷取檔案。"

若要建立直接郵件訊息，請建立排程的行銷活動或歷程，並設定解壓縮檔案。 直接郵件提供者需要此檔案，才能將郵件傳送給您的客戶。

>[!IMPORTANT]
>
>在建立直接郵件訊息之前，請確定您已設定：
>
>1. [檔案路由組態](../direct-mail/direct-mail-configuration.md#file-routing-configuration)，指定應該上傳及儲存解壓縮檔案的伺服器，
>1. 將參考檔案路由設定的[直接郵件設定](../direct-mail/direct-mail-configuration.md#direct-mail-surface)。

## 新增直接郵件訊息 {#create-dm-campaign}

瀏覽下列標籤，瞭解如何在行銷活動或歷程中新增直接郵件訊息。

>[!BEGINTABS]

>[!TAB 新增直接郵件訊息至歷程]

1. 開啟您的歷程，然後從浮動視窗的&#x200B;**動作**&#x200B;區段拖放&#x200B;**[!UICONTROL 直接郵件]**&#x200B;活動。

1. 提供訊息的基本資訊（標籤、說明、類別），然後選擇要使用的訊息設定。 根據預設，**[!UICONTROL 組態]**&#x200B;欄位會預先填入使用者用於該頻道的最後一個組態。 如需如何設定歷程的詳細資訊，請參閱[此頁面](../building-journeys/journey-gs.md)。

1. 設定要傳送給直接郵件提供者的擷取檔案。 若要這麼做，請按一下&#x200B;**[!UICONTROL 編輯內容]**&#x200B;按鈕。

   ![從動作調色盤新增至歷程的直接郵件活動](assets/direct-mail-add-journey.png)

1. 調整解壓縮檔案屬性，例如檔案名稱或要顯示的欄。 如需如何設定解壓縮檔案屬性的詳細資訊，請參閱本節： [建立直接郵件訊息](../direct-mail/create-direct-mail.md#extraction-file)。

   ![直接郵件歷程活動的擷取檔案內容編輯器](assets/direct-mail-journey-content.png)

1. 定義擷取檔案的內容後，請使用&#x200B;**[!UICONTROL 模擬內容]**&#x200B;預覽該內容。 [瞭解如何預覽和測試內容](../content-management/preview-test.md)

   ![模擬直接郵件擷取檔案的內容預覽](assets/direct-mail-simulate.png){width="800" align="center"}

當您的擷取檔案準備就緒時，請完成[歷程](../building-journeys/journey-gs.md)的設定以傳送它。

>[!TAB 新增直接郵件訊息至行銷活動]

1. 存取&#x200B;**[!UICONTROL 促銷活動]**&#x200B;功能表，然後按一下&#x200B;**[!UICONTROL 建立促銷活動]**。

1. 選取&#x200B;**已排程 — 行銷**&#x200B;行銷活動型別。

1. 在&#x200B;**[!UICONTROL 屬性]**&#x200B;區段中，編輯行銷活動的&#x200B;**[!UICONTROL 標題]**&#x200B;和&#x200B;**[!UICONTROL 描述]**。

1. 若要定義您的目標對象，請按一下&#x200B;**[!UICONTROL 選取對象]**&#x200B;按鈕，然後從可用的Adobe Experience Platform對象中選擇。 [了解更多](../audience/about-audiences.md)。

   >[!IMPORTANT]
   >
   >目前，受眾選擇限製為3百萬個設定檔。 如有要求，您可向Adobe代表解除此限制。

1. 在&#x200B;**[!UICONTROL 身分識別名稱空間]**&#x200B;欄位中，選取適當的名稱空間以識別所選對象中的個人。 [了解更多](../event/about-creating.md#select-the-namespace)。

1. 在&#x200B;**[!UICONTROL 動作]**&#x200B;區段中，選擇&#x200B;**[!UICONTROL 直接郵件]**。

1. 選取或建立要使用的&#x200B;**[!UICONTROL 直接郵件組態]**。 [瞭解如何建立直接郵件設定](direct-mail-configuration.md#direct-mail-surface)。

   ![在排程行銷活動中設定的直接郵件動作](assets/direct-mail-campaign.png){width="800" align="center"}

   >[!AVAILABILITY]
   >
   >直接郵件支援&#x200B;**保留**&#x200B;功能，但目前不支援&#x200B;**處理**。 [瞭解如何使用實驗](../content-management/get-started-experiment.md)

1. 行銷活動可以排程為特定日期，或設定為定期重複。 在[本節](../campaigns/campaign-schedule.md)中瞭解如何設定行銷活動的&#x200B;**[!UICONTROL 排程]**。

您現在可以開始設定擷取檔案，以傳送給直接郵件提供者。

>[!ENDTABS]

## 設定摘取檔案 {#extraction-file}

>[!CONTEXTUALHELP]
>id="ajo_direct_mail_data_fields"
>title="資料欄位"
>abstract="依直接郵件提供者之要求，新增並設定在摘取檔案中要顯示的欄位和資訊，才能把郵件寄送給你的客戶。 你可以新增最多 50 欄。"

>[!CONTEXTUALHELP]
>id="ajo_direct_mail_formatting"
>title="摘取檔案格式"
>abstract="使用個人化編輯器指定每個欄位的標籤以及要顯示的資訊。<br/><br/> 您可以透過「<b>排序方式</b>」選項，使用選定的欄位做為摘取檔案的欄排序依據。"

直接郵件供應商需要擷取檔案，才能傳送郵件給您的客戶。 若要定義解壓縮檔案組態，請執行下列步驟：

1. 在行銷活動或歷程設定畫面中，按一下&#x200B;**[!UICONTROL 編輯內容]**&#x200B;按鈕以設定擷取檔案內容。

1. 若要新增決定原則至您的直接郵件訊息，請在&#x200B;**[!UICONTROL 資料欄位]**&#x200B;區段中選取欄，並使用![](../experience-decisioning/assets/do-no-localize/editor-icon.svg)圖示開啟個人化編輯器。 瀏覽至&#x200B;**[!UICONTROL 決定原則]**&#x200B;功能表以建立和插入決定原則。 然後，您就可以在擷取檔案中，將決策專案屬性當做欄資料使用。

   >[!AVAILABILITY]
   >
   >直接郵件中的Experience決策是一項新功能。 以前，直接郵件擷取檔案無法使用決策引擎；您現在可以新增決策原則，並在匯出中包含決策專案屬性作為欄資料。

   [瞭解如何在直接郵件中新增決定原則](../experience-decisioning/create-decision-policy.md#add)。 如需批次決定工作流程和範例（個人化的直接郵件或匯出到下游系統），請參閱直接郵件中的[批次決定](../experience-decisioning/batch-decisioning-direct-mail.md)。

1. 調整解壓縮檔案屬性：

   1. 在&#x200B;**[!UICONTROL 檔案名稱]**&#x200B;欄位中，指定解壓縮檔案的名稱。

      >[!NOTE]
      >
      >依預設，檔案會寫入伺服器上的根目錄中。 **[!UICONTROL Filename]**&#x200B;欄位也接受格式「/your/path/here/Filename.csv」，其中指定的路徑是所選伺服器上的目標目錄。<!--TBC if for SFTP and Azure only, or for all servers including S3-->

   1. 如果要將自動時間戳記新增到指定的檔案名稱，請選擇性地啟用&#x200B;**[!UICONTROL 附加時間戳記以匯出檔案名稱]**&#x200B;選項。

   1. 有時候，您可能需要在解壓縮檔案的開頭或結尾新增資訊。 若要這麼做，請使用&#x200B;**[!UICONTROL 附註]**&#x200B;欄位，然後指定是否要以頁首或頁尾形式包含附註。

      ![擷取檔案內容，包括檔案名稱、時間戳記、頁首或頁尾備註](assets/direct-mail-properties.png){width="800" align="center"}

1. 設定要在擷取檔案中顯示的欄和資訊：

   1. 按一下「**[!UICONTROL 新增]**」按鈕以建立新欄。

   1. **[!UICONTROL 格式]**&#x200B;窗格會顯示在右側，讓您設定選取的欄。 指定資料行的&#x200B;**[!UICONTROL 標籤]**。

   1. 在&#x200B;**[!UICONTROL 資料]**&#x200B;欄位中，使用[個人化編輯器](../personalization/personalization-build-expressions.md)選取要顯示的設定檔屬性。

   1. 若要使用欄來排序擷取檔案，請選取該欄並開啟&#x200B;**[!UICONTROL 排序依據]**&#x200B;選項。 **[!UICONTROL 排序依據]**&#x200B;圖示會顯示在&#x200B;**[!UICONTROL 資料欄位]**&#x200B;區段中資料行的標籤旁。

      ![直接郵件擷取檔案編輯器中的資料欄位和欄格式](assets/direct-mail-content.png){width="800" align="center"}

   1. 重複這些步驟，視需要為解壓縮檔案新增任意數目的欄。 請注意，您最多可以新增50欄。

      若要變更欄的位置，請將其拖放至&#x200B;**[!UICONTROL 資料欄位]**&#x200B;區段中的所需位置。 若要刪除欄，請選取該欄，然後按一下&#x200B;**[!UICONTROL 格式]**&#x200B;窗格中的&#x200B;**[!UICONTROL 移除]**&#x200B;按鈕。

您現在可以測試直接郵件訊息，並將其傳送給您的對象。 [瞭解如何測試和傳送直接郵件訊息](test-send-direct-mail.md)

## 相關主題 {#related-topics}

* [開始使用直接郵件](get-started-direct-mail.md)
* [設定直接郵件頻道](direct-mail-configuration.md)
* [測試並傳送直接郵件](test-send-direct-mail.md)
* [預覽和測試內容](../content-management/preview-test.md)

如需直接郵件的常見問題，請參閱[開始使用直接郵件](get-started-direct-mail.md)。
