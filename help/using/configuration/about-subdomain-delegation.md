---
title: 委派子網域
description: 了解如何委派子網域
internal: n
snippet: y
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 1b5ca4db-44d9-49e2-ab39-a1abba223ec7
source-git-commit: 203f8545200d4a6c20a748807e20ba7aba1ab5f3
workflow-type: tm+mt
source-wordcount: '637'
ht-degree: 36%

---

# 子網域委派於 [!DNL Journey Optimizer]

為電子郵件行銷活動建立子網域可讓品牌將各種類型的流量（行銷與公司等）隔離至特定IP池和特定網域，以加速IP準備程式並改善整體傳遞能力。 如果您共用某個域，該域被阻止或添加到拒絕清單中，則可能會影響公司郵件的傳送。 不過，您電子郵件行銷通訊專屬網域的信譽問題或區塊，只會影響電子郵件的流程。 將主域用作多個郵件流的發件人地址或「發件人」地址也可能會中斷電子郵件身份驗證，從而導致郵件被阻止或放在垃圾郵件資料夾中。

## 為什麼要設定子網域？ {#why-setting-up-subdomains}

子網域是您網域的分區，可用來隔離您的品牌或各種類型的流量，例如交易式訊息和行銷通訊。

讓我們以「mybrand.com」網域為例，這是個用來傳送交易和行銷通訊的網域。在此情況下，您可以決定設定兩個子網域：

* 「Info.mybrand.com」子網域用來進行交易通訊（購買確認函、密碼重設等等）；
* 「marketing.mybrand.com」子網域則用來傳送電子郵件給潛在客戶。

您可以藉此維護網域和其他子網域的信譽。舉例來說，如果「marketing.mybrand.com」子網域因傳遞能力不佳，而被網際網路服務提供者新增至封鎖清單，如此就能防止整個「mybrand.com」網域和「info.mybrand.com」子網域被新增至封鎖清單。

實施解決方案時，對外部元件有以下要求：包括設定要追蹤的連結和網頁、顯示鏡像頁面等。

雖然這些需求是透過Adobe和客戶托管的元件來管理，但其中包含URL，可供電子郵件的收件者看到。 為避免有指出基礎技術解決方案或托管提供者的URL，您可以設定子網域，讓這對電子郵件的收件者透明。

**了解更多**

* 了解如何 [委派子網域](delegate-subdomain.md) 直接從介面
* 了解如何 [新增Google TXT記錄](google-txt.md) 傳送至您的子網域，以確保電子郵件成功傳送至Gmail地址
* 了解如何 [訪問PTR記錄](ptr-records.md) 為您的子網域產生，可透過傳送郵件伺服器來驗證

## 子網域設定方法 {#subdomain-delegation-methods}

子網域設定可讓您設定網域的子區段（技術上稱為「DNS區域」），以便與Adobe Campaign搭配使用。 可用的設定方法有：

* **將子網域完全委派給 Adobe**（建議）：子網域已完全委派給 Adobe。Adobe能夠控制並維護傳遞、呈現和追蹤訊息所需的DNS的所有方面。 [深入了解完整子網域委派](delegate-subdomain.md#full-subdomain-delegation)

* **CNAME的使用**:建立子網域並使用CNAME指向Adobe特定記錄。 使用此設定，您和Adobe都有責任維護DNS。 [深入了解CNAME子網域委派](delegate-subdomain.md#cname-subdomain-delegation)

下表提供這些方法的運作方式摘要，以及所需投入的精力：

| 配置方法 | 運作方式 | 所需投入的精力 |
|---|---|---|
| **完全委派** | 建立子網域和命名空間記錄。Adobe 便會設定 Adobe Campaign 所需的所有 DNS 記錄。<br/><br/>在此設定中，Adobe 會完全負責管理子網域和所有 DNS 記錄。 | 低 |
| **CNAME，自訂方法** | 建立子網域和命名空間記錄。Adobe 便會提供要放置在 DNS 伺服器中的記錄，並在 Adobe Campaign DNS 伺服器中設定對應的值。<br/><br/>在此設定中，您和 Adobe 都有責任維護 DNS。 | 高 |

有關域配置的其他資訊，請參見 [本檔案](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/product-specific-resources/campaign/ac-domain-name-setup.html).

如果您對子網域設定方法有任何疑問，請聯絡Adobe，或最終聯絡客戶服務以要求傳遞能力諮詢。
