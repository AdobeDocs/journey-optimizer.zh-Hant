---
title: 快速入門
description: 了解如何開始使用產品建議庫 API，使用決策引擎執行主要作業。
feature: Decision Management, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 773bee50-849f-4b07-9423-67de5279ad28
source-git-commit: 30fed481bb02fd25f1833e76ae94330aa51d153b
workflow-type: ht
source-wordcount: '382'
ht-degree: 100%

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

➡️ [了解更多此影片中的決策管理元件相關資訊](#video)

## 先決條件 {#prerequisites}

本指南需要您深入了解下列 Adobe Experience Platform 元件：

* [[!DNL Experience Data Model (XDM) System]](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hant){target="_blank"}：[!DNL Experience Platform] 據以組織客戶體驗資料的標準化框架。
   * [結構構成的基本概念](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=zh-Hant){target="_blank"}：了解 XDM 結構的基本建置區塊。
* [決策管理](../../../using/offers/get-started/starting-offer-decisioning.md)：說明用於一般 Decisioning，特別是決策管理之概念和元件。說明在客戶體驗期間用於選取最佳選項的策略。
* [[!DNL Profile Query Language (PQL)]](https://experienceleague.adobe.com/docs/experience-platform/segmentation/pql/overview.html?lang=zh-Hant){target="_blank"}：PQL是一種在 XDM 執行個體上編寫運算式的强大語言。PQL 用於定義決策規則。

## 讀取範例 API 呼叫 {#reading-sample-api-calls}

本指南提供範例 API 呼叫，示範如何格式化您的請求。 這些包括路徑、必要的標頭和正確格式化的請求承載。 此外，也提供 API 回應中傳回的範例 JSON。 如需文件中用於範例 API 呼叫的慣例相關資訊，請參閱 [!DNL Experience Platform] 疑難排解指南中的[如何讀取範例 API 呼叫](https://experienceleague.adobe.com/docs/experience-platform/landing/troubleshooting.html?lang=zh-Hant#how-do-i-format-an-api-request){target="_blank"}一節。

## 收集所需標頭的值 {#gather-values-for-required-headers}

為了對 [!DNL Adobe Experience Platform] API 進行呼叫，您必須先完成[驗證教學課程](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-authentication.html?lang=zh-Hant){target="_blank"}。完成驗證教學課程會提供所有 [!DNL Experience Platform] API 呼叫中每個必要標頭的值，如下所示：

* `Authorization: Bearer {ACCESS_TOKEN}`
* `x-api-key: {API_KEY}`
* `x-gw-ims-org-id: {IMS_ORG}`
* `x-sandbox-name: {SANDBOX_NAME}`

所有包含承載 (POST、PUT、PATCH) 的請求都需有額外的標頭：

* `Content-Type: application/json`

>[!NOTE]
>
>系統會根據指派的產品輪廓強制執行權限檢查。只有關聯產品輪廓中授與的權限才能決定可透過 API 存取或管理的資源。

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

