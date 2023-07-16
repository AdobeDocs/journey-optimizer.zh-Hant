---
solution: Journey Optimizer
product: journey optimizer
title: 開始使用 Journey Optimizer 的身分
description: 了解如何在 Adobe Journey Optimizer 管理身分
feature: Profiles
role: User
level: Beginner
exl-id: 90e892e9-33c2-4da5-be1d-496b42572897
source-git-commit: 72bd00dedb943604b2fa85f7173cd967c3cbe5c4
workflow-type: ht
source-wordcount: '342'
ht-degree: 100%

---

# 開始使用身分 {#identities-gs}

身分是實體 (通常為個人) 專屬的資料。登入 ID、ECID 或會員 ID 等身分稱為已知身分。

電子郵件地址和電話號碼等個人身分資訊 (PII)，用於直接識別客戶。因此，PII 可用來比對跨系統的客戶多重身分。

在 [!DNL Adobe Journey Optimizer]，**身分**&#x200B;跨裝置和管道連結消費者，結果會是[識別圖](#id-graph)。 連結的身分圖表可依據您所有業務接觸點的互動，來個人化體驗。  

![](assets/identities-home.png)

深入了解&#x200B;**身分服務**，請參閱[本文件](https://experienceleague.adobe.com/docs/experience-platform/identity/home.html?lang=zh-Hant){target="_blank"}。

## 身分識別命名空間 {#identity-namespaces}

****&#x200B;身分識別命名空間是 Identity Service 的元件，用途是作為身分識別相關內容的指標。 例如，他們將 `name@email.com` 的值區分為電子郵件地址，或將值區分為 `443522` 作為數值 CRM ID。使用身分命名空間需先了解所涉及的各種 Adobe Experience Platform 服務。開始使用命名空間之前，請先檢閱下列服務文件：

請參閱[本文件](https://experienceleague.adobe.com/docs/experience-platform/identity/namespaces.html?lang=zh-Hant){target="_blank"}，深入了解&#x200B;**身分命名空間**。

## 識別圖{#id-graph}

此&#x200B;**識別圖**&#x200B;是特定客戶不同身分之間關係的地圖，以視覺化呈現客戶在不同管道間與品牌互動的方式。所有客戶識別圖均由 Adobe Experience Platform 身分服務以近乎即時的方式集中管理並更新，以回應客戶活動。

在 [!DNL Adobe Journey Optimizer] 使用者介面的識別圖檢視器，可讓您視覺化並更清楚了解哪些客戶身分已彙整在一起，以及以哪些方式彙整。 檢視器可讓您拖曳圖形的不同部分並加以互動，讓您檢查複雜的身分關係、更有效率地偵錯，並透過資訊的使用方式提高透明度而受益。

請參閱[本文件](https://experienceleague.adobe.com/docs/experience-platform/identity/ui/identity-graph-viewer.html?lang=zh-Hant){target="_blank"}，深入了解&#x200B;**識別圖**。
