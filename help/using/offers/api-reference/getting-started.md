---
title: 快速入門
description: 了解如何開始使用產品建議庫 API，使用決策引擎執行主要作業。
feature: Decision Management, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 773bee50-849f-4b07-9423-67de5279ad28
source-git-commit: b6fd60b23b1a744ceb80a97fb092065b36847a41
workflow-type: tm+mt
source-wordcount: '352'
ht-degree: 76%

---

# 決策管理 API 開發人員指南 {#decision-management-api-developer-guide}

>[!CONTEXTUALHELP]
>id="od_api_support"
>title="新的決策管理 API"
>abstract="現已推出用於建立和管理決策管理物件的新 API。舊版 API 將支援至 2024 年 3 月 27 日為止。"

>[!CONTEXTUALHELP]
>id="ajo_decisioning_api_support"
>title="新的決策管理 API"
>abstract="現已推出用於建立和管理決策管理物件的新 API。舊版 API 將支援至 2024 年 3 月 27 日為止。"

本開發人員指南提供了協助您開始使用 [!DNL Offer Library] API 的步驟。 接著，本指南會提供範例 API 呼叫，用於使用決策引擎執行主要作業。

➡️ [在此影片中進一步了解決定管理的元件](#video)

## 先決條件 {#prerequisites}

本指南需要您深入了解下列 Adobe Experience Platform 元件：

* [[!DNL Experience Data Model (XDM) System]](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hant){target="_blank"}： [!DNL Experience Platform]用來組織客戶體驗資料的標準化架構。
   * [結構描述組合的基本概念](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=zh-Hant){target="_blank"}：瞭解XDM結構描述的基本建置區塊。
* [決策管理](../../../using/offers/get-started/starting-offer-decisioning.md)：說明用於一般 Decisioning，特別是決策管理之概念和元件。說明在客戶體驗期間用於選取最佳選項的策略。
* [[!DNL Profile Query Language (PQL)]](https://experienceleague.adobe.com/docs/experience-platform/segmentation/pql/overview.html?lang=zh-Hant){target="_blank"}： PQL是一種強大的語言，可透過XDM執行個體寫入運算式。 PQL 用於定義決策規則。

## 讀取範例 API 呼叫 {#reading-sample-api-calls}

本指南提供範例 API 呼叫，示範如何格式化您的請求。 這些包括路徑、必要的標頭和正確格式化的請求承載。 此外，也提供 API 回應中傳回的範例 JSON。 如需檔案中所使用範例API呼叫慣例的詳細資訊，請參閱[疑難排解指南中](https://experienceleague.adobe.com/docs/experience-platform/landing/troubleshooting.html?lang=zh-Hant#how-do-i-format-an-api-request){target="_blank"}如何讀取範例API呼叫[!DNL Experience Platform]一節。

## 收集所需標頭的值 {#gather-values-for-required-headers}

若要呼叫[!DNL Adobe Experience Platform] API，您必須先完成[驗證教學課程](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-authentication.html?lang=zh-Hant){target="_blank"}。 完成驗證教學課程會提供所有 [!DNL Experience Platform] API 呼叫中每個必要標頭的值，如下所示：

* `Authorization: Bearer {ACCESS_TOKEN}`
* `x-api-key: {API_KEY}`
* `x-gw-ims-org-id: {IMS_ORG}`
* `x-sandbox-name: {SANDBOX_NAME}`

所有包含承載 (POST、PUT、PATCH) 的請求都需有額外的標頭：

* `Content-Type: application/json`

## 後續步驟 {#next-steps}

本文件說明對 [!DNL Offer Library] API 進行呼叫所需的先決條件知識。您現在可以繼續進行本開發人員指南中提供的範例呼叫，並遵循其指示進行作業。
<!--
>[!NOTE]
>
> The In-app messaging channel in Adobe Journey Optimizer uses decision management objects. If your organization uses the in-app messaging channel, then API list requests for objects will include objects created by the in-app messaging service and can be ignored for decision management use cases. Objects created for in-app messages will have `createdBy = "Mobile_Sheliak"`.
-->

<!-- ## How-to video {#video}

The following video is intended to support your understanding of the components of Decision Management.

>[!VIDEO](https://video.tv.adobe.com/v/329919?quality=12) -->

