---
solution: Journey Optimizer
product: journey optimizer
title: ' [!DNL Journey Optimizer]中的子網域委派'
description: 瞭解如何委派您的子網域
feature: Subdomains
topic: Administration
role: Admin
level: Experienced
keywords: 子網域，最佳化工具，委派
exl-id: 1b5ca4db-44d9-49e2-ab39-a1abba223ec7
source-git-commit: 1746efa82611d232b5af07b271739417b4e36e8c
workflow-type: tm+mt
source-wordcount: '982'
ht-degree: 28%

---

# [!DNL Journey Optimizer] 中的子網域委派 {#subdomain-delegation}

>[!CONTEXTUALHELP]
>id="ajo_admin_delegated_subdomains"
>title="您委派的子網域會顯示在這裡。"
>abstract="委派您的第一個子網域。委派完成後，PTR 記錄就會建立且電子郵件管道將啟用。"

建立電子郵件促銷活動的子網域可讓品牌將各種型別的流量（例如行銷與企業）隔離到特定的IP集區和特定網域，進而加快IP預熱程式並改善整體的可遞送性。

如果您共用網域，且網域遭到封鎖或新增至拒絕清單，可能會影響您的公司郵件傳送。 不過，您電子郵件行銷通訊專屬網域上的信譽問題或封鎖將只會影響該電子郵件流程。 使用您的主網域作為寄件者或多個郵件串流的「寄件者」地址也會破壞電子郵件驗證，導致您的郵件遭到封鎖或放入垃圾郵件資料夾。

>[!CAUTION]
>
>您無法使用相同的傳送網域從[!DNL Adobe Journey Optimizer]和其他產品（例如[!DNL Adobe Campaign]或[!DNL Adobe Marketo Engage]）傳送訊息。

## 為什麼要設定子網域？ {#why-set-up-subdomains}

子網域是您網域的分割槽，可用來隔離您的名稱或各類流量，例如交易訊息和行銷通訊。

讓我們以「mybrand.com」網域為例，這是個用來傳送交易和行銷通訊的網域。在此情況下，您可以決定設定兩個子網域：

* 「Info.mybrand.com」子網域用來進行交易通訊（購買確認函、密碼重設等等）；
* 「marketing.mybrand.com」子網域則用來傳送電子郵件給潛在客戶。

您可以藉此維護網域和其他子網域的信譽。舉例來說，如果「marketing.mybrand.com」子網域因傳遞能力不佳，而被網際網路服務提供者新增至封鎖清單，如此就能防止整個「mybrand.com」網域和「info.mybrand.com」子網域被新增至封鎖清單。

實作解決方案時，對外向元件會有需求：包括設定要追蹤的連結和網頁、顯示映象頁面等。

雖然這些需求是透過Adobe和客戶託管的元件進行管理，但包含電子郵件收件者可檢視的URL。 為避免具有指出基礎技術解決方案或託管提供者的URL，可以設定子網域以讓此對電子郵件的收件者透明。

**了解更多**

* 瞭解如何直接從介面[委派您的子網域](delegate-subdomain.md)
* 瞭解如何[將Google TXT記錄](google-txt.md)新增至您的子網域，以確保將電子郵件成功傳送至Gmail地址
* 瞭解如何[存取為您的子網域產生的PTR記錄](ptr-records.md)，以便透過傳送郵件伺服器來驗證這些記錄

## 子網域設定方法 {#subdomain-delegation-methods}

子網域設定可讓您設定網域的子區段（技術上稱為「DNS區域」），以便與Adobe Campaign搭配使用。

可用的設定方法如下。

### 將子網域完全委派給Adobe （建議） {#full-subdomain-delegation}

[!DNL Journey Optimizer]可讓您直接從產品介面將子網域完全委派給Adobe。 藉由這樣做，Adobe將能夠控制並維護傳遞、演算及追蹤電子郵件行銷活動所需的DNS的各個層面，以受管理的方式傳遞訊息。

<!--The subdomain is fully delegated to Adobe. Adobe is able to control and maintain all aspects of DNS that are required for delivering, rendering and tracking messages.-->

您可以仰賴Adobe維護所需的DNS基礎架構，以符合電子郵件行銷傳送網域的產業標準傳遞能力要求，同時繼續維護及控制內部電子郵件網域的DNS。

>[!IMPORTANT]
>
>建議使用完全子網域委派方法。

在[本節](delegate-subdomain.md#set-up-subdomain)中瞭解如何將子網域完全委派給Adobe。

### 使用 CNAME 設定子網域 {#cname-subdomain-setup}

如果您有網域特定的限制原則，並且您希望Adobe只擁有對DNS的部份控制權，您可以選擇在自己這邊執行所有DNS相關的活動。

CNAME子網域設定可讓您建立子網域，並使用CNAME指向Adobe特定記錄。 使用此設定，您和 Adobe 都有責任維護 DNS，針對電子郵件的傳送、轉譯和追蹤設定環境。

>[!CAUTION]
>
>如果貴組織的原則限制完整的子網域委派方法，則建議使用CNAME方法。 此方法需要您自行維護和管理DNS記錄。
>
>Adobe將無法協助變更、維護或管理透過CNAME方法設定的子網域的DNS。

在[本節](delegate-subdomain.md#cname-subdomain-setup)中瞭解如何使用CNAME建立子網域以指向Adobe特定記錄。

### 使用自訂子網域 {#custom-subdomain-delegation}

自訂委派方法可讓您完全擁有控制及維護傳遞、轉譯及追蹤訊息所需的DNS各方面功能。

在此情況下，您將完全擁有和管理我們自己的子網域，並對此程式產生之憑證擁有完全控制權。

瞭解如何在[本節](delegate-custom-subdomain.md)中設定自訂網域。

## 比較設定方法

下表提供這些方法的運作方式摘要，以及所需投入的精力：
<!--
| Configuration method | How it works | Level of effort |
|---|---|---|
| **Full delegation** | Create the subdomain and namespace record. Adobe will then configure all DNS records required for Adobe Campaign.<br/><br/>In this setup, Adobe is fully responsible for managing the subdomain and all the DNS records. | Low |
| **CNAME method** |  Create the subdomain and namespace record. Adobe will then provide the records to be placed in your DNS servers and will configure the corresponding values in Adobe Campaign DNS servers.<br/><br/>In this setup, both you and Adobe share responsibility for maintaining DNS. | High |-->


| 設定方法 | 運作方式 | 所需投入的精力 |
|---|---|---|
| **完全委派** | 建立子網域和命名空間記錄。Adobe 便會設定 Adobe Campaign 所需的所有 DNS 記錄。<br/><br/>在此設定中，Adobe 會完全負責管理子網域和所有 DNS 記錄。 | 低 |
| **CNAME方法** | 建立子網域和命名空間記錄。Adobe 便會提供要放置在 DNS 伺服器中的記錄，並在 Adobe Campaign DNS 伺服器中設定對應的值。<br/><br/>在此設定中，您和 Adobe 都有責任維護 DNS。 | 高 |
| **自訂委派方法** | 建立子網域和名稱空間記錄 — Adobe接著會提供要放置在DNS伺服器中的記錄。 上傳從憑證授權單位取得的SSL憑證，並透過驗證網域所有權並報告電子郵件地址來完成回饋回圈步驟。<br/><br/>在此設定中，您完全有責任維護DNS。 | 非常高 |

如需網域設定的其他資訊，請參閱[此文件](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/product-specific-resources/campaign/ac-domain-name-setup.html?lang=zh-Hant){target="_blank"}。

如果您對子網域設定方法有任何疑問，請聯絡Adobe，或聯絡客戶服務以請求傳遞能力諮詢。


