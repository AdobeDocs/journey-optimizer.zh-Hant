---
title: 子域委派 [!DNL Journey Optimizer]
description: 瞭解如何委派子域
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 1b5ca4db-44d9-49e2-ab39-a1abba223ec7
source-git-commit: 5596c851b70cc38cd117793d492a15fd4ce175ef
workflow-type: tm+mt
source-wordcount: '714'
ht-degree: 32%

---

# 子域委派 [!DNL Journey Optimizer] {#subdomain-delegation}

為電子郵件活動建立子域使品牌能夠將不同類型的通信（例如，營銷與公司）隔離到特定的IP池中，並與特定的域隔離，這將加快IP升溫過程並提高整體交付能力。 如果您共用一個域，並且該域被阻止或添加到拒絕清單中，它可能會影響您的公司郵件傳遞。 但是，特定於您的電子郵件營銷通信的域上的聲譽問題或阻止只會影響電子郵件流。 將主域用作多個郵件流的發件人地址或「發件人」地址也可能會中斷電子郵件身份驗證，導致您的郵件被阻止或放置在垃圾郵件資料夾中。

>[!NOTE]
>
>不能使用同一發送域從 [!DNL Adobe Journey Optimizer] 和其他產品，比如 [!DNL Adobe Campaign] 或 [!DNL Adobe Marketo Engage]。

## 為什麼要設定子網域？ {#why-setting-up-subdomains}

子域是域的一個分區，可用於隔離您的品牌或各種類型的通信量，例如事務性消息和營銷通信。

讓我們以「mybrand.com」網域為例，這是個用來傳送交易和行銷通訊的網域。在此情況下，您可以決定設定兩個子網域：

* 「Info.mybrand.com」子網域用來進行交易通訊（購買確認函、密碼重設等等）；
* 「marketing.mybrand.com」子網域則用來傳送電子郵件給潛在客戶。

您可以藉此維護網域和其他子網域的信譽。舉例來說，如果「marketing.mybrand.com」子網域因傳遞能力不佳，而被網際網路服務提供者新增至封鎖清單，如此就能防止整個「mybrand.com」網域和「info.mybrand.com」子網域被新增至封鎖清單。

實施解決方案時，需要面向外部的元件：包括設定要跟蹤的連結和網頁、顯示鏡像頁等。

雖然這些要求是通過由Adobe和客戶托管的元件進行管理的，但它們包括URL，這些URL可由電子郵件的收件人看到。 為了避免具有指示底層技術解決方案或托管提供商的URL，可以設定子域以使此對電子郵件的收件人透明。

**了解更多**

* 瞭解如何 [委派子域](delegate-subdomain.md) 直接從介面
* 瞭解如何 [添加GoogleTXT記錄](google-txt.md) 確保將電子郵件成功傳遞到Gmail地址
* 瞭解如何 [訪問PTR記錄](ptr-records.md) 為子域生成，允許通過發送郵件伺服器來驗證

## 子域配置方法 {#subdomain-delegation-methods}

子域配置允許您配置域的子部分（技術上是「DNS區域」），以便與Adobe Campaign配合使用。 可用的設定方法有：

* **將子網域完全委派給 Adobe**（建議）：子網域已完全委派給 Adobe。Adobe能夠控制和維護傳遞、呈現和跟蹤消息所需的DNS的所有方面。 [瞭解有關完整子域委派的詳細資訊](delegate-subdomain.md#full-subdomain-delegation)

* **CNAME的使用**:建立子域並使用CNAME指向特定於Adobe的記錄。 使用此設定，您和Adobe共用維護DNS的責任。 [瞭解有關CNAME子域委派的詳細資訊](delegate-subdomain.md#cname-subdomain-delegation)

>[!CAUTION]
>
>Full子域委派是首選方法。
>
>如果組織的策略限制了完整的子域委派方法，則建議使用CNAMEs方法。 此方法要求您自行維護和管理DNS記錄。 Adobe將無法幫助更改、維護或管理通過CNAME方法配置的子域的DNS。

下表提供這些方法的運作方式摘要，以及所需投入的精力：

| 配置方法 | 運作方式 | 所需投入的精力 |
|---|---|---|
| **完全委派** | 建立子網域和命名空間記錄。Adobe 便會設定 Adobe Campaign 所需的所有 DNS 記錄。<br/><br/>在此設定中，Adobe 會完全負責管理子網域和所有 DNS 記錄。 | 低 |
| **CNAME，自訂方法** | 建立子網域和命名空間記錄。Adobe 便會提供要放置在 DNS 伺服器中的記錄，並在 Adobe Campaign DNS 伺服器中設定對應的值。<br/><br/>在此設定中，您和 Adobe 都有責任維護 DNS。 | 高 |

有關域配置的其他資訊，請參見 [本文檔](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/product-specific-resources/campaign/ac-domain-name-setup.html)。

如果您對子域配置方法有任何疑問，請聯繫Adobe，或最終聯繫客戶服務部門以請求提供性咨詢。
