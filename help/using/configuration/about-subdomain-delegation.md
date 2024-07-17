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
source-git-commit: f8d62a702824bcfca4221c857acf1d1294427543
workflow-type: tm+mt
source-wordcount: '916'
ht-degree: 30%

---

# [!DNL Journey Optimizer] 中的子網域委派 {#subdomain-delegation}

>[!CONTEXTUALHELP]
>id="ajo_admin_delegated_subdomains"
>title="您委派的子網域會顯示在這裡。"
>abstract="委派您的第一個子網域。委派完成後，PTR 記錄就會建立且電子郵件管道將啟用。"

建立電子郵件促銷活動的子網域可讓品牌將各種型別的流量（例如行銷與企業）隔離到特定的IP集區和特定網域，進而加快IP預熱程式並改善整體的可遞送性。

如果您共用網域，且網域遭到封鎖或新增至拒絕清單，可能會影響您的公司郵件傳送。 不過，您電子郵件行銷通訊專屬網域上的信譽問題或封鎖將只會影響該電子郵件流程。 使用您的主網域作為寄件者或多個郵件串流的「寄件者」地址也會破壞電子郵件驗證，導致您的郵件遭到封鎖或放入垃圾郵件資料夾。

>[!NOTE]
>
>您無法使用相同的傳送網域從[!DNL Adobe Journey Optimizer]和其他產品（例如[!DNL Adobe Campaign]或[!DNL Adobe Marketo Engage]）傳送訊息。

## 為什麼要設定子網域？ {#why-set-up-subdomains}

子網域是您網域的分割槽，可用來隔離您的名稱或各類流量，例如交易訊息和行銷通訊。

讓我們以「mybrand.com」網域為例，這是個用來傳送交易和行銷通訊的網域。在此情況下，您可以決定設定兩個子網域：

* 「Info.mybrand.com」子網域用來進行交易通訊（購買確認函、密碼重設等等）；
* 「marketing.mybrand.com」子網域則用來傳送電子郵件給潛在客戶。

您可以藉此維護網域和其他子網域的信譽。舉例來說，如果「marketing.mybrand.com」子網域因傳遞能力不佳，而被網際網路服務提供者新增至封鎖清單，如此就能防止整個「mybrand.com」網域和「info.mybrand.com」子網域被新增至封鎖清單。

實作解決方案時，對外向元件會有需求：包括設定要追蹤的連結和網頁、顯示映象頁面等。

雖然這些需求是透過Adobe和客戶託管的元件來管理，但它們包含電子郵件收件者可以看到的URL。 為避免具有指出基礎技術解決方案或託管提供者的URL，可以設定子網域以讓此對電子郵件的收件者透明。

**了解更多**

* 瞭解如何直接從介面[委派您的子網域](delegate-subdomain.md)
* 瞭解如何[將Google TXT記錄](google-txt.md)新增至您的子網域，以確保將電子郵件成功傳送至Gmail地址
* 瞭解如何[存取為您的子網域產生的PTR記錄](ptr-records.md)，以便透過傳送郵件伺服器來驗證這些記錄

## 子網域設定方法 {#subdomain-delegation-methods}

子網域設定可讓您設定網域的子區段（技術上稱為「DNS區域」），以便與Adobe Campaign搭配使用。 可用的設定方法有：

* **將子網域完全委派給Adobe** （建議）：子網域已完全委派給Adobe。 Adobe能夠控制並維護傳遞、轉譯及追蹤訊息所需的DNS的各個層面。 [深入瞭解完整子網域委派](delegate-subdomain.md#full-subdomain-delegation)

* **使用 CNAME**：建立子網域並使用 CNAME 以指向 Adobe 特定記錄。 使用此設定，您和Adobe都有責任維護DNS。 [深入瞭解CNAME子網域委派](delegate-subdomain.md#cname-subdomain-delegation)

>[!CAUTION]
>
>* 建議使用完全子網域委派方法。
>
>* 如果貴組織的原則限制完整的子網域委派方法，則建議使用CNAME方法。 此方法需要您自行維護和管理DNS記錄。 Adobe將無法協助變更、維護或管理透過CNAME方法設定的子網域的DNS。

下表提供這些方法的運作方式摘要，以及所需投入的精力：

| 設定方法 | 運作方式 | 所需投入的精力 |
|---|---|---|
| **完全委派** | 建立子網域和命名空間記錄。Adobe 便會設定 Adobe Campaign 所需的所有 DNS 記錄。<br/><br/>在此設定中，Adobe 會完全負責管理子網域和所有 DNS 記錄。 | 低 |
| **CNAME，自訂方法** | 建立子網域和命名空間記錄。Adobe 便會提供要放置在 DNS 伺服器中的記錄，並在 Adobe Campaign DNS 伺服器中設定對應的值。<br/><br/>在此設定中，您和 Adobe 都有責任維護 DNS。 | 高 |

如需網域設定的其他資訊，請參閱[此文件](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/product-specific-resources/campaign/ac-domain-name-setup.html?lang=zh-Hant)。

如果您對子網域設定方法有任何疑問，請聯絡Adobe，或最終聯絡客戶服務以要求獲得傳遞能力諮詢。

## 存取委派的子網域 {#access-delegated-subdomains}

所有委派的子網域會顯示在&#x200B;**[!UICONTROL 管理]** > **[!UICONTROL 管道]** > **[!UICONTROL 子網域]**&#x200B;功能表中。 篩選器可協助您調整清單（委派日期、使用者或狀態）。

![](assets/subdomain-list.png)

**[!UICONTROL 狀態]**&#x200B;欄提供子網域委派程式的資訊：

* **[!UICONTROL 草稿]**：子網域委派已儲存為草稿。 按一下子網域名稱以繼續委派程式，
* **[!UICONTROL 正在處理]**：子網域正在執行數個組態檢查，然後才能使用，
* **[!UICONTROL 成功]**：子網域已成功通過檢查，且可用於傳遞訊息，
* **[!UICONTROL 失敗]**：提交子網域委派後，一或多個檢查失敗。

若要存取狀態為&#x200B;**[!UICONTROL 成功]**&#x200B;之子網域的詳細資訊，請從清單中開啟該子網域。

![](assets/subdomain-delegated.png)

您可以：

* 擷取委派過程中設定的子網域名稱（唯讀），以及產生的URL （資源、映象頁面、追蹤URL），

* 將Google網站驗證TXT記錄新增至您的子網域，以確保其已驗證(請參閱[將Google TXT記錄新增至子網域](google-txt.md))。


>[!CAUTION]
>
>子網域設定在所有環境中都是通用的。 因此，對子網域所做的任何修改也會影響生產沙箱。
