---
title: 開始使用Journey Optimizer的身份
description: 瞭解如何管理Adobe Journey Optimizer的身份
feature: Profiles
role: User
level: Beginner
exl-id: 90e892e9-33c2-4da5-be1d-496b42572897
source-git-commit: dee8dbac067dac851af02d87a3dece1ba2b29376
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 9%

---

# 開始使用標識 {#identities-gs}

標識是實體（通常是個人）唯一的資料。 諸如登錄ID、ECID或會員ID等標識稱為已知標識。

個人識別資訊(PII)（例如電子郵件地址和電話號碼）可直接識別客戶。 因此， PII用於跨系統匹配客戶的多個身份。

在 [!DNL Adobe Journey Optimizer]。 **身份** 將消費者連結到設備和通道，結果是 [身份圖](#id-graph)。 連結的身份圖用於根據您所有業務接觸點之間的交互來個性化體驗。

![](assets/identities-home.png)

瞭解有關 **身份服務** 在 [本文檔](https://experienceleague.adobe.com/docs/experience-platform/identity/home.html?lang=zh-Hant){target=&quot;_blank&quot;}。

## 標識命名空間 {#identity-namespaces}

****&#x200B;身分識別命名空間是 Identity Service 的元件，用途是作為身分識別相關內容的指標。例如，它們將 `name@email.com` 電子郵件地址或 `443522` 作為數字CRM ID。 使用標識命名空間需要瞭解涉及的各種Adobe Experience Platform服務。 開始使用命名空間之前，請查看以下服務的文檔：

瞭解有關 **標識命名空間** 在 [本文檔](https://experienceleague.adobe.com/docs/experience-platform/identity/namespaces.html?lang=zh-Hant){target=&quot;_blank&quot;}。

## 標識圖{#id-graph}

的 **標識圖** 是一張特定客戶不同身份之間關係的地圖，它為您提供了客戶如何通過不同渠道與您的品牌進行交互的直觀表示。 所有客戶身份圖由Adobe Experience Platform身份服務部門根據客戶活動近即時進行集體管理和更新。

中的標識圖形查看器 [!DNL Adobe Journey Optimizer] 用戶介面使您能夠直觀地顯示並更好地瞭解哪些客戶身份是通過什麼方式拼接在一起的。 查看器允許您拖動圖形的不同部分並與之交互，從而允許您檢查複雜的身份關係、更高效地調試，並受益於資訊利用方式提高的透明度。

瞭解有關 **標識圖** 在 [本文檔](https://experienceleague.adobe.com/docs/experience-platform/identity/ui/identity-graph-viewer.html){target=&quot;_blank&quot;}。
