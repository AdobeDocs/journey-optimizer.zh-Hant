---
title: 快速入門
description: 瞭解如何開始使用優惠資料庫API，使用決策引擎執行關鍵作業。
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 773bee50-849f-4b07-9423-67de5279ad28
source-git-commit: 805f7bdc921c53f63367041afbb6198d0ec05ad8
workflow-type: tm+mt
source-wordcount: '349'
ht-degree: 7%

---

# Decision Management API開發人員指南 {#decision-management-api-developer-guide}

本開發人員指南提供步驟，協助您開始使用 [!DNL Offer Library] API。 接著，指南會提供範例API呼叫，說明如何使用決策引擎執行重要作業。

➡️ [在此影片中進一步了解決定管理的元件](#video)

## 先決條件 {#prerequisites}

本指南需要您深入瞭解下列Adobe Experience Platform元件：

* [[!DNL Experience Data Model (XDM) System]](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hant){target="_blank"}：作為依據的標準化架構 [!DNL Experience Platform] 組織客戶體驗資料。
   * [結構描述組合基本概念](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=zh-Hant){target="_blank"}：瞭解XDM結構描述的基本建置組塊。
* [決定管理](../../../using/offers/get-started/starting-offer-decisioning.md)：說明用於一般體驗決策（尤其是決策管理）的概念和元件。 說明用於選擇在客戶體驗期間呈現的最佳選項的策略。
* [[!DNL Profile Query Language (PQL)]](https://experienceleague.adobe.com/docs/experience-platform/segmentation/pql/overview.html){target="_blank"}：PQL是一種強大的語言，可透過XDM執行個體寫入運算式。 PQL可用來定義決定規則。

## 讀取範例API呼叫 {#reading-sample-api-calls}

本指南提供範例API呼叫，示範如何格式化您的請求。 這些包括路徑、必要的標題和正確格式化的請求裝載。 此外，也提供API回應中傳回的範例JSON。 如需檔案中用於範例API呼叫的慣例相關資訊，請參閱以下章節： [如何讀取範例API呼叫](https://experienceleague.adobe.com/docs/experience-platform/landing/troubleshooting.html#how-do-i-format-an-api-request){target="_blank"} 在 [!DNL Experience Platform] 疑難排解指南。

## 收集所需標題的值 {#gather-values-for-required-headers}

為了呼叫 [!DNL Adobe Experience Platform] API，您必須先完成 [驗證教學課程](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-authentication.html){target="_blank"}. 完成驗證教學課程會提供所有中每個必要標題的值 [!DNL Experience Platform] API呼叫，如下所示：

* `Authorization: Bearer {ACCESS_TOKEN}`
* `x-api-key: {API_KEY}`
* `x-gw-ims-org-id: {IMS_ORG}`
* `x-sandbox-name: {SANDBOX_NAME}`

包含裝載(POST、PUT、PATCH)的所有請求都需要額外的標頭：

* `Content-Type: application/json`

## 後續步驟 {#next-steps}

本檔案說明呼叫「 」所需的先決條件知識 [!DNL Offer Library] API。 您現在可以繼續參閱本開發人員指南中提供的範例呼叫，並遵循其指示。
<!--
>[!NOTE]
>
> The In-app messaging channel in Adobe Journey Optimizer uses decision management objects. If your organization uses the in-app messaging channel, then API list requests for objects will include objects created by the in-app messaging service and can be ignored for decision management use cases. Objects created for in-app messages will have `createdBy = “Mobile_Sheliak”`.
-->

## 操作說明影片 {#video}

以下影片旨在協助您了解決定管理的元件。

>[!VIDEO](https://video.tv.adobe.com/v/329919?quality=12)

