---
title: 開始使用Journey Optimizer中的身分識別
description: 了解如何在Adobe Journey Optimizer中管理身分
feature: 設定檔
role: User
level: Beginner
source-git-commit: b07970ff11f1ba7c4e6db30dc2eca1252a579ca4
workflow-type: tm+mt
source-wordcount: '349'
ht-degree: 6%

---

# 開始使用身分 {#identities-gs}

身分是實體（通常為個人）專屬的資料。 登入ID、ECID或忠誠度ID等身分識別，即為已知身分識別。

個人識別資訊(PII)，例如電子郵件地址和電話號碼，可直接識別客戶。 因此，PII可用來比對客戶跨系統的多重身分。

在[!DNL Adobe Journey Optimizer]中， **身分**&#x200B;連結跨裝置和通道的使用者，結果是[身分圖表](#id-graph)。 連結的身分圖表可依據您所有業務接觸點的互動，來個人化體驗。

![](assets/identities-home.png)

深入了解[本檔案](https://experienceleague.adobe.com/docs/experience-platform/identity/home.html){target=&quot;_blank&quot;}中的&#x200B;**Identity服務**。

## 身分識別命名空間

****&#x200B;身分識別命名空間是 Identity Service 的元件，用途是作為身分識別相關內容的指標。例如，它們會將`name@email.com`值區分為電子郵件地址，或將`443522`區分為數值CRM ID。 使用身分識別命名空間需要先了解所涉及的各種Adobe Experience Platform服務。 開始使用命名空間之前，請先檢閱以下服務的檔案：

深入了解&#x200B;**[本檔案](https://experienceleague.adobe.com/docs/experience-platform/identity/namespaces.html){target=&quot;_blank&quot;}中的身分識別命名空間**。

## 身分圖{#id-graph}

**身分圖表**&#x200B;是特定客戶不同身分之間關係的地圖，可以以視覺化呈現客戶如何透過不同管道與品牌互動。 所有客戶身分圖表均由Adobe Experience Platform Identity Service以近乎即時的方式共同管理和更新，以回應客戶活動。

[!DNL Adobe Journey Optimizer]使用者介面中的身分圖表檢視器可讓您視覺化，並更清楚了解哪些客戶身分識別會匯整在一起，以及以哪些方式匯整。 檢視器可讓您拖曳圖形的不同部分並加以互動，讓您檢查複雜的身分關係、更有效率地偵錯，並透過資訊的使用方式提高透明度而獲益。

深入了解[本檔案](https://experienceleague.adobe.com/docs/experience-platform/identity/ui/identity-graph-viewer.html){target=&quot;_blank&quot;}中的&#x200B;**身分圖**。

