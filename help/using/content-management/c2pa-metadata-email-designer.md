---
solution: Journey Optimizer
product: journey optimizer
title: 電子郵件和登陸頁面Designer中的C2PA中繼資料
description: 瞭解已附加至影像的C2PA中繼資料在Adobe Journey Optimizer中的電子郵件和登陸頁面設計工具中移動時會發生什麼事。
feature: Content Management
topic: Content Management, Artificial Intelligence
role: User
level: Beginner
source-git-commit: 47e95cbc3716e650492e9cda4a4fddbe61f56ffd
workflow-type: tm+mt
source-wordcount: '531'
ht-degree: 0%

---


# 電子郵件和登陸頁面Designer中的C2PA中繼資料 {#c2pa-email-landing-page-designer}

>[!BEGINSHADEBOX]

**在此頁面上：**&#x200B;瞭解C2PA中繼資料在Adobe Journey Optimizer中的電子郵件和登入頁面設計工具中移動時，已附加至影像的情形。

>[!ENDSHADEBOX]

>[!INFO]
>
>圍繞創作AI透明度的新法律不斷湧現，Adobe正在努力滿足各個司法轄區的適用要求。 C2PA中繼資料是Adobe用來符合這些法律要求的來源工具。

電子郵件和登入頁面設計工具本身不會產生或編輯影像。 它會參照在其他Adobe工具（例如「產生內容」、「Adobe Express」或「Firefly」）或合作夥伴模型中已使用產生AI產生或編輯的影像。 當您建置、發佈和傳送時，已附加至這些影像的C2PA中繼資料會保留且保持不變。

## 當您建置並傳送時，會保留C2PA中繼資料 {#c2pa-preserved}

下表總結了使用電子郵件和登入頁面設計工具建置和傳送內容的每個步驟中，C2PA中繼資料的情況。

| 動作 | 發生什麼情況 | 是否保留C2PA中繼資料？ | 範例 |
| --- | --- | --- | --- |
| **將影像插入範本** | 設計人員會為已在其他地方使用創作AI產生或編輯的影像新增參考，例如產生內容、Adobe Express、Firefly或合作夥伴模型。 影像檔案本身不會變更。 | 是，未變更 | Firefly產生的橫幅會插入電子郵件範本中。 |
| **調整大小、重新定位或新增替代文字** | 僅顯示範本HTML變更中的屬性。 不會重新編碼影像檔案。 | 是，未變更 | 影像會調整大小以符合行動版面以及指定的替代文字。 |
| **發佈** | 會發佈電子郵件或登入頁面，並儲存影像以供傳送。 | 是，未變更 | 行銷活動會發佈，其影像會儲存以供傳送。 |
| **傳送電子郵件或檢視登陸頁面** | 影像會傳送到收件者的收件匣或顯示在即時頁面上。 | 是，未變更 | 收件者開啟電子郵件並下載影像；認證仍符合原始憑證。 |

## 內容型別及其範圍 {#c2pa-content-types}

* **影像**：已涵蓋。 如上所示，插入、調整、發佈和傳送影像時，會保留已附加至影像的C2PA中繼資料。
* **視訊、音訊、文字**：不適用。 電子郵件和登入頁面設計工具不會使用產生AI來產生或編輯這些內容型別。

## 內容移動時發生什麼事 {#c2pa-content-moves}

C2PA中繼資料會透過Adobe Journey Optimizer中的電子郵件和登陸頁面設計工具，從您的編輯器透過儲存空間傳送到收件者的收件匣或即時頁面，與影像一起移動。 在以上任何步驟中，都不會建立、變更或移除認證。

如果影像未包含產生式AI C2PA中繼資料，因為該影像不是使用產生式AI產生或編輯的，則此處不會顯示認證。 這是預期中的情形，而非錯誤。

## 檢查認證 {#c2pa-checking-credential}

尚無法直接在電子郵件或登入頁面設計工具中檢查Content Credential。

## 其他資源

* [產生內容中的C2PA中繼資料](generative-c2pa-metadata.md)
* [Generative AI內容透明度](https://experienceleague.adobe.com/zh-hant/docs/cx-enterprise-ai/experience-cloud-ai/overview/content-transparency)
