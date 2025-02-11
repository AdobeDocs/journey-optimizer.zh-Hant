---
solution: Journey Optimizer
product: journey optimizer
title: 將內建頻道動作新增至歷程
description: 瞭解如何將內建頻道動作新增到歷程
feature: Journeys, Activities, Channels Activity
topic: Content Management
role: User
level: Intermediate
keywords: 歷程，訊息，推播，簡訊，電子郵件，應用程式內，網頁，內容卡，程式碼型體驗
exl-id: 4db07a9e-c3dd-4873-8bd9-ac34c860694c
source-git-commit: 994eac32591f4ca352d310bc06057bd20ea03886
workflow-type: tm+mt
source-wordcount: '431'
ht-degree: 27%

---

# 使用內建頻道動作 {#add-a-message-in-a-journey}

>[!CONTEXTUALHELP]
>id="ajo_message_activity"
>title="內建頻道動作"
>abstract="Journey Optimizer 內建頻道動作功能。您只需在您的歷程中新增傳出 (電子郵件、簡訊 (SMS/MMS)、推播) 或傳入 (應用程式內、網頁版、基於程式碼的體驗、內容卡片) 活動，並定義設定和內容。然後會在歷程的內容中執行和傳送。"

[!DNL Journey Optimizer]隨附內建頻道動作功能。 您只需在您的歷程中新增傳出 (電子郵件、簡訊 (SMS/MMS)、推播) 或傳入 (應用程式內、網頁版、基於程式碼的體驗、內容卡片) 活動，並定義設定和內容。然後會在歷程的內容中執行和傳送。

>[!NOTE]
>
>您也可以設定傳送訊息給您的特定動作。 [了解更多](#recommendation)

若要將內建頻道動作新增至歷程，請遵循下列步驟。

1. 以[事件](general-events.md)或[讀取對象](read-audience.md)活動來開始您的歷程。

1. 從調色盤的&#x200B;**動作**&#x200B;區段，拖放外寄（**電子郵件**、**推播**、**簡訊**）或內送（**應用程式內**、**網頁**、**程式碼型體驗**、**內容卡**）活動至畫布。

   ![](assets/journey-web-activity.png)

1. 設定您的活動。

   * 瞭解建立訊息內容的詳細步驟，如下所示：

     <table style="table-layout:fixed">
      <tr style="border: 0;">
      <td>
      <a href="../email/create-email.md">
      <img alt="銷售機會" src="../assets/do-not-localize/email.jpg">
      </a>
      <div><a href="../email/create-email.md"><strong>建立電子郵件</strong>
      </div>
      <p>
      </td>
      <td>
      <a href="../push/create-push.md">
      <img alt="不頻繁" src="../assets/do-not-localize/push.jpg">
      </a>
      <div>
      <a href="../push/create-push.md"><strong>建立推播通知<strong></a>
      </div>
      <p>
      </td>
      <td>
      <a href="../sms/create-sms.md">
      <img alt="驗證" src="../assets/do-not-localize/sms.jpg">
      </a>
      <div>
      <a href="../sms/create-sms.md"><strong>建立文字訊息（簡訊/多媒體簡訊）</strong></a>
      </div>
      <p>
      </td>
      </tr>
      </table>

   * 瞭解建立傳入動作的詳細步驟，如下所示：

     <table style="table-layout:fixed">
      <tr style="border: 0;">
      <td>
      <a href="../in-app/create-in-app.md">
      <img alt="銷售機會" src="../assets/do-not-localize/in-app.jpg">
      </a>
      <div><a href="../in-app/create-in-app.md"><strong>建立應用程式內訊息</strong>
      </div>
      <p>
      </td>
      <td>
      <a href="../web/create-web.md">
      <img alt="銷售機會" src="../assets/do-not-localize/web-create.jpg">
      </a>
      <div><a href="../web/create-web.md"><strong>建立網站體驗</strong>
      </div>
      <p>
      </td>
      <td>
      <a href="../content-card/create-content-card.md">
      <img alt="銷售機會" src="../assets/do-not-localize/sms-config.jpg">
      </a>
      <div><a href="../content-card/create-content-card.md"><strong>建立內容卡片</strong>
      </div>
      <p>
      </td>
      <td>
      <a href="../code-based/create-code-based.md">
      <img alt="不頻繁" src="../assets/do-not-localize/web-design.jpg">
      </a>
      <div>
      <a href="../code-based/create-code-based.md"><strong>建立程式碼型體驗<strong></a>
      </div>
      <p>
      </td>
      </tr>
      </table>

     >[!NOTE]
     >
     >每個傳入訊息活動都隨附3天&#x200B;**等待**&#x200B;活動。 [了解更多](../building-journeys/wait-activity.md#auto-wait-node)

## 建議 {#recommendation}

[!DNL Journey Optimizer]隨附內建訊息功能。 不過，自訂動作可讓您設定協力廠商系統的連線，以傳送訊息或API呼叫。

* 如果您使用協力廠商系統來傳送訊息，則可建立自訂動作。 [了解更多](../action/action.md)

* 如果您正在使用Campaign和Journey Optimizer，請參閱下列區段：

   * [[!DNL Journey Optimizer]和Campaign v7/v8](../action/acc-action.md)
   * [[!DNL Journey Optimizer]與Campaign Standard](../action/acs-action.md)

## 更新即時內容{#update-live-content}

您可以在即時歷程中更新內建頻道動作的內容。

若要這麼做，請開啟您的即時歷程、選取頻道活動並按一下&#x200B;**編輯內容**。

![](assets/add-a-message2.png)

但是，您無法變更個人化中使用的屬性，無論是設定檔屬性或內容資料（來自事件或歷程屬性）。

如果您修改內容資料，將會顯示下列錯誤訊息： ERR_AUTHORING_JOURNEYVERSION_201

如果您修改設定檔屬性，將會顯示下列錯誤訊息：ERR_AUTHORING_JOURNEYVERSION_202

請注意，針對應用程式內活動，可以在歷程上線時對內容進行任何變更，但無法修改應用程式內觸發器。
