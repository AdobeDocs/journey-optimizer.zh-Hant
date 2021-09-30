---
title: 快速啟動
description: Journey Optimizer 快速啟動
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 71ab7369-fd84-46eb-95d2-941bd887d565
source-git-commit: 9c1edc8d79c58fcf4f2048b9fe81cd31ea621777
workflow-type: tm+mt
source-wordcount: '519'
ht-degree: 35%

---

# 快速入門 {#cjm-quick-start}

## 啟動的重要步驟 {#cjm-key-steps}

藉助 [!DNL Adobe Journey Optimizer]，您可以匯入現有訊息內容或設計新內容、使用客戶設定檔資料個人化訊息、建立事件以觸發訊息、定義細分並調整對象、傳送多頻道訊息、建立並新增優惠，以及存取一套完整的報告與監視工具來評估訊息和客戶歷程的影響。

您可以根據您的組織定義數種使用者類型，並依其權限授予他們特定功能的存取權。

## 準備和配置您的環境

開始使用[!DNL Adobe Journey Optimizer]之前，需要執行幾個步驟來準備您的環境。

身為系統管理員，您需要&#x200B;**了解產品設定檔，並為沙箱管理和通道設定指派權限**。 您也需要設定沙箱，並針對可用的產品設定檔進行管理。
然後，您便能將團隊成員指派給產品設定檔，以及**設定通道設定**&#x200B;以傳送訊息。

如需詳細資訊，請參閱下列頁面：

* **設定使** 用者權限並授予團隊成員的存取權。[閱讀全文](../using/administration/permissions.md)

* **部署[!DNL Adobe Experience Manager Assets Essentials]** 以管理訊息中的資產和影像：需要存取的使 [!DNL Assets Essentials] 用者必須屬於Assets Essentials消費 **者使** 用者或/和Assets Essentials **使用者** 產品設定檔。[如需詳細資訊，請參閱Assets Essentials檔案](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/deploy-administer.html){target=&quot;_blank&quot;}

* **設定您的** 管道，並定義您的電子郵件和推播通知設定。[閱讀全文](../using/configuration/get-started-configuration.md)

* **定義預** 設集並設定品牌參數。[閱讀全文](../using/configuration/message-presets.md)

* **管理** 沙箱，將執行個體分割到個別的虛擬環境中。[閱讀全文](../using/administration/sandboxes.md)


## 準備資料並設定歷程

身為資料管理員，您需要&#x200B;**識別資料，並建立結構和資料集**，將資料匯入Adobe Experience Platform。

以下各節將詳細說明建立身分命名空間和為設定檔啟用的資料集、建立區段和測試設定檔的步驟：

* 了解如何在[Adobe Experience Platform檔案](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html?lang=zh-Hant){target=&quot;_blank&quot;}中預覽和建立&#x200B;**資料集**

* 了解如何在[Adobe Experience Platform檔案](https://experienceleague.adobe.com/docs/experience-platform/identity/namespaces.html#manage-namespaces){target=&quot;_blank&quot;}中建立&#x200B;**身分命名空間**

* 了解如何在[此頁面](../using/building-journeys/creating-test-profiles.md)中建立&#x200B;**測試設定檔**

* 深入了解[Adobe Experience Platform檔案](https://experienceleague.adobe.com/docs/experience-platform/ingestion/home.html?lang=zh-Hant){target=&quot;_blank&quot;}中的&#x200B;**資料擷取**

* 了解如何在[本頁面](../using/segment/about-segments.md)中定義對象&#x200B;**、建立區段、管理同意和隱私權**

此外，若要在歷程中傳送訊息，您必須設定&#x200B;**[!UICONTROL Data Sources]**、**[!UICONTROL Events]**&#x200B;及&#x200B;**[!UICONTROL Actions]**。 請參閱[本節](../using/configuration/about-data-sources-events-actions.md)以進一步瞭解

## 建立訊息、優惠方案和歷程

身為歷程慣例，請參閱下列章節，以設定您的第一個歷程、新增選件和資產，以及傳送訊息：

* **建立訊息**：存取訊息、設計或載入電子郵件和推播內容、新增個人化及預覽訊息。[閱讀全文](create-message.md)

* **上傳資產**：使用 Adobe Experience Manager Assets Essentials 來管理資產和影像。[閱讀全文](assets-essentials.md)

* **新增優惠**：使用 Journey Optimizer 決定管理在訊息中新增個人化優惠。[閱讀全文](../using/offers/get-started/starting-offer-decisioning.md)

* **建立歷程**：傳送訊息、運用情境式資料、調整對象、設計並執行多步驟使用案例。[閱讀全文](building-journeys/journey.md)

* **監控訊息和歷程**:控制訊息執行、檢查訊息與歷程報告、後續傳遞能力量度。[閱讀全文](message-monitoring.md)
