---
solution: Journey Optimizer
product: journey optimizer
title: 自訂上傳(CSV)和同盟對象構成
description: 瞭解使用自訂上傳(CSV)和同盟受眾構成受眾時的重要資訊和最佳實務。
feature: Audiences, Profiles
topic: Content Management
role: User
level: Beginner
mini-toc-levels: 1
source-git-commit: 26d311802236a1f9e8f6273c1291bcb54138aad2
workflow-type: tm+mt
source-wordcount: '415'
ht-degree: 6%

---

# 自訂上傳(CSV)和同盟對象構成 {#csv-fac}

## 關於自訂上傳和同盟對象構成 {#about}

除了區段定義和對象構成之外，[!DNL Journey Optimizer]可讓您從CSV檔案匯入對象，或運用資料倉儲中的資料，來產生和鎖定對象。

* **自訂上傳**：使用CSV檔案匯入對象。 在Adobe Experience Platform [Segmentation Service檔案](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/audience-portal#import-audience){target="_blank"}中瞭解如何匯入對象。

* **同盟對象構成**：直接從您現有的資料倉儲同盟資料集，以在一個系統中建立並擴充Adobe Experience Platform對象和屬性。 請閱讀[同盟對象構成](https://experienceleague.adobe.com/zh-hant/docs/federated-audience-composition/using/home)的指南。

  >[!AVAILABILITY]
  >
  >聯合客群組成目前僅開放給某些組織使用 (限量開放使用)。如需詳細資訊，請聯絡您的 Adobe 代表。

您可以在Journey Optimizer中鎖定這些對象，或在Adobe Experience Platform支援的任何目的地啟用他們

➡️[在影片中探索這些功能](#video)

## 必讀 {#must-read}

本節提供處理自訂上傳（CSV檔案）和同盟對象構成對象時，請牢記的重要資訊。

* **預覽和校訂支援：**&#x200B;目前，使用CSV上傳或同盟對象構成所建立的對象不支援預覽和校訂。 在規劃行銷活動時，請記住這一點。

* **啟用延遲：**&#x200B;受眾可在內嵌完成後立即在Journey Optimizer中使用。 雖然這通常在一小時內完成，但可能會有所變動。

* **啟用的記錄與身分拼接：**&#x200B;對象中的每個記錄都已啟動，包括任何重複專案。 在下次UPS設定檔匯出期間，這些記錄將進行身分拼接。 因此，啟用的記錄數可能與身分拼接後的設定檔數不同。

* **鎖定新設定檔：**&#x200B;當記錄和UPS設定檔之間找不到相符專案時，會建立新的空白設定檔。 此設定檔連結至儲存在Data Lake中的擴充屬性。 由於此新設定檔為空白，因此Journey Optimizer中通常使用的目標定位欄位（例如personalEmail.address、mobilePhone.number）為空白，因此無法用於目標定位。

  若要解決此問題，您可以在通道設定中將「執行欄位」（或「執行地址」，視通道而定）指定為「identityMap」。 這將確保在建立受眾時選擇作為身分的屬性將是用於在Journey Optimizer中定位的屬性。

## 作法影片 {#video}

瞭解如何將CSV格式的對象上傳至Adobe Experience Platform。

>[!VIDEO](https://video.tv.adobe.com/v/3421714?quality=12)

進一步瞭解同盟對象構成。

>[!VIDEO](https://video.tv.adobe.com/v/3432261?quality=12)
