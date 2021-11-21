---
title: 開始使用Journey Optimizer中的身分識別
description: 了解如何在Adobe Journey Optimizer中管理身分
feature: Profiles
role: User
level: Beginner
exl-id: 90e892e9-33c2-4da5-be1d-496b42572897
source-git-commit: 7138e1f031bd26caf9379c3ff19d79ac29442bc6
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 9%

---

# 開始使用身分 {#identities-gs}

身分是實體（通常為個人）專屬的資料。 登入ID、ECID或忠誠度ID等身分識別，即為已知身分識別。

個人識別資訊(PII)，例如電子郵件地址和電話號碼，可直接識別客戶。 因此，PII可用來比對客戶跨系統的多重身分。

在 [!DNL Adobe Journey Optimizer], **身分** 連結裝置和管道上的消費者，結果是 [身分圖](#id-graph). 連結的身分圖表可依據您所有業務接觸點的互動，來個人化體驗。

![](assets/identities-home.png)

深入了解 **Identity服務** in [本檔案](https://experienceleague.adobe.com/docs/experience-platform/identity/home.html?lang=zh-Hant){target=&quot;_blank&quot;}。

## 身分識別命名空間

****&#x200B;身分識別命名空間是 Identity Service 的元件，用途是作為身分識別相關內容的指標。例如，它們會區分 `name@email.com` 作為電子郵件地址或 `443522` 作為數值CRM ID。 使用身分識別命名空間需要先了解所涉及的各種Adobe Experience Platform服務。 開始使用命名空間之前，請先檢閱以下服務的檔案：

深入了解 **身分識別命名空間** in [本檔案](https://experienceleague.adobe.com/docs/experience-platform/identity/namespaces.html?lang=zh-Hant){target=&quot;_blank&quot;}。

## 身分圖{#id-graph}

此 **身分圖** 是特定客戶不同身分之間關係的地圖，以視覺化呈現客戶在不同管道間與品牌互動的方式。 所有客戶身分圖表均由Adobe Experience Platform Identity Service以近乎即時的方式共同管理和更新，以回應客戶活動。

中的身分圖表檢視器 [!DNL Adobe Journey Optimizer] 使用者介面可讓您視覺化並更清楚了解哪些客戶身分識別已匯整在一起，以及以哪些方式匯整。 檢視器可讓您拖曳圖形的不同部分並加以互動，讓您檢查複雜的身分關係、更有效率地偵錯，並透過資訊的使用方式提高透明度而獲益。

深入了解 **身分圖** in [本檔案](https://experienceleague.adobe.com/docs/experience-platform/identity/ui/identity-graph-viewer.html){target=&quot;_blank&quot;}。
