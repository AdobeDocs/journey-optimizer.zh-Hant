---
solution: Journey Optimizer
product: journey optimizer
title: 關於 Adobe Experience Platform 客群
description: 了解如何使用 Adobe Experience Platform 客群
feature: Audiences, Profiles
topic: Content Management
role: User
level: Beginner
exl-id: 78b95ccd-bc28-46cd-937a-f68e3f34cc1e
source-git-commit: 24d66f146ea3ed0e89a3b928b805bc53a70a8895
workflow-type: tm+mt
source-wordcount: '753'
ht-degree: 14%

---

# [!DNL Journey Optimizer]中的對象啟用 {#segments-in-journey-optimizer}

您可以在行銷活動和歷程中選取使用區段定義、自訂上傳、組合工作流程或同盟對象組合產生的任何對象。

## 護欄與限制 {#guardrails}

* **Healthcare Shield或Privacy and Security Shield** — 目前Healthcare Shield或Privacy and Security Shield無法使用對象構成中的對象和屬性。 [瞭解如何在 [!DNL Journey Optimizer]](../audience/about-audiences.md#enrichment)中使用對象擴充屬性

* **自訂上傳與同盟對象構成** — 對於自訂上傳與同盟對象構成對象，請注意下列護欄：

   * **預覽和校訂支援：**&#x200B;目前，使用CSV上傳或同盟對象構成所建立的對象不支援預覽和校訂。 在規劃行銷活動時，請記住這一點。

   * **鎖定新設定檔：**&#x200B;當記錄與整合設定檔服務設定檔之間找不到相符專案時，會建立新的空白設定檔。 此設定檔連結至儲存在Data Lake中的擴充屬性。 因為這個新的設定檔是空的，所以通常在[!DNL Journey Optimizer]中使用的目標欄位（例如personalEmail.address、mobilePhone.number）是空的。 因此，這些欄位無法用於目標定位。

     若要解決此問題，您可以在通道設定中將「執行欄位」（或「執行地址」，視通道而定）指定為「identityMap」。 這可確保在建立受眾時選擇作為身分的屬性將是在[!DNL Journey Optimizer]中用於定位的屬性。

   * **啟用的記錄與身分拼接：**&#x200B;對象中的每個記錄都已啟動，包括任何重複專案。 在下次統一設定檔服務設定檔匯出期間，這些記錄會進行身分拼接。 因此，啟用的記錄數可能與身分拼接後的設定檔數不同。

## 對象啟用延遲 {#activation}

內嵌完成之後，對象就可以在[!DNL Journey Optimizer]中使用。 雖然這通常在一小時內完成，但可能會有所變動。 從構成中產生的對象應在發佈後24小時內可用。

對於批次分段工作產生的對象，啟用可能會因批次擷取變數而延遲。 對於每日排程的讀取對象歷程，您可以在歷程屬性中定義時間範圍，以確保在歷程執行之前有新的對象資料可用。

如果區段工作未在定義的時間範圍內完成，將略過歷程直到其下一次發生。 [瞭解如何排程讀取對象歷程](../building-journeys/read-audience.md)

## 在[!DNL Journey Optimizer]中鎖定對象

您可以在 **[!DNL Journey Optimizer]** 中以不同方式善用客群：

* 選擇&#x200B;**行銷活動**&#x200B;的客群，將訊息傳送給屬於所選客群的所有個人。 [了解如何定義行銷活動的客群](../campaigns/create-campaign.md#define-the-audience-audience)。

* 在歷程中使用&#x200B;**讀取對象**&#x200B;協調活動，讓對象中的所有個人進入歷程並接收歷程中包含的訊息。 假設您有「銀級客戶」客群。 利用此活動，您可以讓所有銀級客戶進入歷程。 接著，您就可以傳送一系列個人化訊息給他們。 [了解如何設定讀取客群活動](../building-journeys/read-audience.md#configuring-segment-trigger-activity)。

  對於使用受眾構成或自訂上傳的受眾的歷程，設定檔屬性與在歷程輸入時的最後一次批次評估一樣新。 不過，在&#x200B;**等待**&#x200B;活動後，歷程會重新整理來自整合設定檔服務(UPS)的設定檔屬性，擷取最新可用的資料，這表示歷程執行期間可能會變更設定檔屬性。 [進一步瞭解等待活動後重新整理設定檔](../building-journeys/wait-activity.md#profile-refresh)

* 在歷程中使用&#x200B;**條件**&#x200B;活動，以根據客群成員資格建置條件。 [了解如何在條件中使用客群](../building-journeys/condition-activity.md#using-a-segment)。

* 在歷程中使用&#x200B;**對象資格**&#x200B;事件活動，以根據Adobe Experience Platform對象進入和退出，讓個人進入歷程或是在歷程中前進。 例如，您可以讓所有新的銀級客戶進入歷程，並向其傳送訊息。 [瞭解如何設定對象資格活動](../building-journeys/audience-qualification-events.md)。

  >[!NOTE]
  >
  >由於使用構成工作流程、自訂上傳或同盟對象構成所建立的對象批次性質，您無法在「對象資格」活動中鎖定這些對象。 此活動中只能運用使用區段定義建立的對象。

## 啟用[!DNL Journey Optimizer]中不支援的對象型別

只有在Audience Portal中建立的對象，才能在[!DNL Journey Optimizer]歷程與行銷活動中直接鎖定目標。 [進一步瞭解可用的對象型別](../audience/about-audiences.md#types)。

如果您需要定位非支援對象(例如Customer Journey Analytics對象)的設定檔，則需要將其包裝在對象入口網站的新區段定義中。 [區段產生器檔案](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/segment-builder#adding-audiences){target="_blank"}提供了如何在區段定義中新增對象的詳細資訊

完成後，請等待區段評估完成，以便用於您的歷程和行銷活動。
