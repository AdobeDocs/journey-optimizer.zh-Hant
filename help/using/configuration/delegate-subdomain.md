---
solution: Journey Optimizer
product: journey optimizer
title: 委派子網域
description: 瞭解如何委派您的子網域。
feature: Subdomains, Deliverability
topic: Administration
role: Admin
level: Experienced
keywords: 子網域、委派、網域、DNS
exl-id: 8021f66e-7725-475b-8722-e6f8d74c9023
source-git-commit: bfb9e797757a96b1e39736f532ee9308f87bb71f
workflow-type: tm+mt
source-wordcount: '1816'
ht-degree: 21%

---

# 委派子網域 {#delegate-subdomain}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomainname"
>title="子網域委派"
>abstract="Journey Optimizer 可讓您將子網域委派給 Adobe。您可以將子網域完全委派給 Adobe，這是建議的方法。您還可以使用 CNAME 建立子網域以指向 Adobe 的特定記錄，但這種方法需要您自行維護和管理 DNS 記錄。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/delegate-subdomains/about-subdomain-delegation.html?lang=zh-Hant#subdomain-delegation-methods" text="子網域設定方法"

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomainname_header"
>title="子網域委派"
>abstract="若要開始傳送電子郵件，您需要將您的子網域委派給 Adobe。完成後，將為您設定 DNS 記錄、收件匣、寄件者、回覆地址和退回地址。"

網域名稱委派是一種方法，可讓網域名稱的所有者（技術上稱為DNS區域）將其細分（技術上稱為DNS區域下的細分）委派給另一個實體。 基本上，身為客戶，如果您處理&quot;example.com&quot;區域，您可以將子網區&quot;marketing.example.com&quot;委派給Adobe。 進一步瞭解 [子網域委派](about-subdomain-delegation.md)

>[!NOTE]
>
>根據預設， [!DNL Journey Optimizer] 可讓您委派最多10個子網域。 不過，根據您的授權合約，您最多可以委派100個子網域。 請聯絡您的Adobe聯絡人，以進一步瞭解您有權使用的子網域數量。

您可以完全委派子網域，或使用CNAME建立子網域以指向Adobe特定記錄。

>[!CAUTION]
>
>建議使用完全子網域委派方法。 深入瞭解兩者之間的差異 [子網域設定方法](about-subdomain-delegation.md#subdomain-delegation-methods).
>
>子網域設定在所有環境中都是通用的。 因此，對子網域所做的任何修改也會影響生產沙箱。

## 完全子網域委派 {#full-subdomain-delegation}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_dns"
>title="產生相符的 DNS 記錄"
>abstract="若要將新的子網域完全委派給 Adobe，您需要將 Journey Optimizer 介面中顯示的 Adobe 名稱伺服器資訊複製貼上您的網域託管解決方案中，以產生相符的 DNS 記錄。若要使用 CNAME 委派子網域，您還需要複製貼上 SSL CDN URL 驗證記錄。一旦檢查成功，子網域就準備好可用於傳遞訊息了。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/delegate-subdomains/delegate-subdomain.html?lang=zh-Hant#cname-subdomain-delegation" text="CNAME 子網域委派"

[!DNL Journey Optimizer] 可讓您直接從產品介面將子網域完全委派給Adobe。 藉由這樣做，Adobe將能夠控制並維護傳遞、演算及追蹤電子郵件行銷活動所需的DNS的各個層面，以受管理的方式傳遞訊息。

您可以仰賴Adobe來維護所需的DNS基礎架構，以符合電子郵件行銷傳送網域的產業標準傳遞能力要求，同時繼續維護和控制內部電子郵件網域的DNS。

若要將新子網域完全委派給Adobe，請執行以下步驟：

1. 存取 **[!UICONTROL 管理]** > **[!UICONTROL 頻道]** > **[!UICONTROL 子網域]** 功能表，然後按一下 **[!UICONTROL 設定子網域]**.

   ![](assets/subdomain-delegate.png)

1. 選取 **[!UICONTROL 已完全委派]** 從 **[!UICONTROL 設定方法]** 區段。

   ![](assets/subdomain-method-full.png)

1. 指定要委派的子網域名稱。

   ![](assets/subdomain-name.png)

   >[!CAUTION]
   >
   >不允許將無效的子網域委派給Adobe。 請務必輸入貴組織所擁有的有效子網域，例如marketing.yourcompany.com。

   <!--Capital letters are not allowed in subdomains. TBC by PM-->

1. 要放置在 DNS 伺服器顯示中的記錄清單。 逐一複製這些記錄，或下載 CSV 檔案，然後導覽至您的網域託管解決方案，以產生相符的 DNS 記錄。

1. 請確定所有DNS記錄都已產生至您的網域託管解決方案。 如果所有專案都已正確設定，請勾選「我確認……」方塊。

   ![](assets/subdomain-submit.png)

1. 設定DMARC記錄。 如果子網域有現有的DMARC記錄，而且它是由擷取的 [!DNL Journey Optimizer]，您可使用相同的值，或視需要加以變更。 如果您未新增任何值，則會使用預設值。 [了解更多](dmarc-record.md)

   ![](assets/dmarc-record-found.png)

1. 按一下&#x200B;**[!UICONTROL 提交]**。

   >[!NOTE]
   >
   >您可以建立記錄，並在稍後使用提交子網域設定。 **[!UICONTROL 另存為草稿]** 按鈕。 然後，您就可以從子網域清單中開啟子網域委派，以繼續子網域委派。

1. 子網域會顯示在含有「 」的清單中 **[!UICONTROL 處理中]** 狀態。 如需子網域狀態的詳細資訊，請參閱 [本節](about-subdomain-delegation.md#access-delegated-subdomains).

   ![](assets/subdomain-processing.png)

   您必須先等到Adobe執行所需的檢查（最多可能需要3小時），才能使用該子網域傳送訊息。 請參閱[此章節](#subdomain-validation)深入瞭解。

   >[!NOTE]
   >
   >任何遺失的記錄（代表尚未在您的託管解決方案上建立的記錄）都會列出。

1. 檢查成功後，子網域會取得 **[!UICONTROL 成功]** 狀態。 已準備好用於傳遞訊息。

   >[!NOTE]
   >
   >子網域將標籤為 **[!UICONTROL 已失敗]** 如果您無法在託管解決方案上建立驗證記錄。

一旦將子網域委派給中的Adobe [!DNL Journey Optimizer]，PTR記錄會自動建立並與此子網域相關聯。 [了解更多](ptr-records.md)

>[!CAUTION]
>
>目前不支援平行執行子網域 [!DNL Journey Optimizer]. 如果您嘗試提交子網域以進行委派，當另一個子網域具有 **[!UICONTROL 處理中]** 狀態，您會收到錯誤訊息。

## CNAME 子網域設定 {#cname-subdomain-delegation}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_dns_cname"
>title="產生相符的 DNS 和驗證記錄"
>abstract="若要使用 CNAME 委派子網域，您需要將 Journey Optimizer 介面中顯示的 Adobe 名稱伺服器資訊和 SSL CDN URL 驗證記錄複製貼上您的託管平台。一旦檢查成功，子網域就準備好可用於傳遞訊息了。"

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_cdn_cname"
>title="複製驗證記錄"
>abstract="Adobe 會產生驗證記錄。您需要在您的託管平台上建立相對應的記錄，以進行 CDN URL 驗證。"

如果您有網域特定的限制原則，並且您希望Adobe只擁有對DNS的部份控制權，您可以選擇在您這邊執行所有DNS相關的活動。

CNAME子網域設定可讓您建立子網域，並使用CNAME指向Adobe特定記錄。 使用此設定，您和 Adobe 都有責任維護 DNS，針對電子郵件的傳送、轉譯和追蹤設定環境。

>[!CAUTION]
>
>如果貴組織的原則限制完整的子網域委派方法，則建議使用CNAME方法。 此方法需要您自行維護和管理DNS記錄。 Adobe將無法協助變更、維護或管理透過CNAME方法設定的子網域的DNS。

➡️ [在本影片中瞭解如何使用CNAME建立子網域以指向Adobe特定記錄](#video)

若要使用CNAME設定子網域，請遵循下列步驟：

1. 存取 **[!UICONTROL 管理]** > **[!UICONTROL 頻道]** > **[!UICONTROL 子網域]** 功能表，然後按一下 **[!UICONTROL 設定子網域]**.

1. 選取 **[!UICONTROL CNAME設定]** 方法。

   ![](assets/subdomain-method-cname.png)

1. 指定要委派的子網域名稱。

   >[!CAUTION]
   >
   >不允許將無效的子網域委派給Adobe。 請務必輸入貴組織所擁有的有效子網域，例如marketing.yourcompany.com。

   <!--Capital letters are not allowed in subdomains. TBC by PM-->

1. 要放置在 DNS 伺服器顯示中的記錄清單。 逐一複製這些記錄，或下載 CSV 檔案，然後導覽至您的網域託管解決方案，以產生相符的 DNS 記錄。

1. 請確定所有DNS記錄都已產生至您的網域託管解決方案。 如果所有專案都已正確設定，請勾選「我確認……」方塊。

   ![](assets/subdomain-create-dns-confirm.png)

1. 設定DMARC記錄。 如果子網域有現有的DMARC記錄，而且它是由擷取的 [!DNL Journey Optimizer]，您可使用相同的值，或視需要加以變更。 如果您未新增任何值，則會使用預設值。 [了解更多](dmarc-record.md)

   ![](assets/dmarc-record-found.png)

1. 按一下&#x200B;**[!UICONTROL 繼續]**。

   >[!NOTE]
   >
   >您稍後可以使用 **[!UICONTROL 另存為草稿]** 按鈕。 然後，您就可以在此階段繼續子網域委派，方法是從子網域清單中開啟該子網域。

1. 等候，直到Adobe驗證在您的託管解決方案上產生記錄時沒有發生錯誤。 此程式最多可能需要2分鐘。

   >[!NOTE]
   >
   >任何遺失的記錄（代表尚未在您的託管解決方案上建立的記錄）都會列出。

1. Adobe會產生SSL CDN URL驗證記錄。 將此驗證記錄複製到您的代管平台。 如果您已在代管解決方案上正確建立此記錄，請勾選「我確認……」方塊，然後按一下 **[!UICONTROL 提交]**.

   <!--![](assets/subdomain-cdn-url-validation.png)-->

1. 提交CNAME子網域委派後，子網域會顯示在清單中，並包含 **[!UICONTROL 處理中]** 狀態。 如需子網域狀態的詳細資訊，請參閱 [本節](about-subdomain-delegation.md#access-delegated-subdomains).

   ![](assets/subdomain-cname-processing.png)

   您必須等待Adobe執行所需檢查（通常需要2至3小時），才能使用該子網域傳送訊息。 請參閱[此章節](#subdomain-validation)深入瞭解。

1. 檢查成功後<!--i.e Adobe validates the record you created and installs it-->，子網域會取得 **[!UICONTROL 成功]** 狀態。 已準備好用於傳遞訊息。

   >[!NOTE]
   >
   >子網域將標籤為 **[!UICONTROL 已失敗]** 如果您無法在託管解決方案上建立驗證記錄。

在驗證記錄並安裝憑證時，Adobe會自動建立CNAME子網域的PTR記錄。 [了解更多](ptr-records.md)

>[!CAUTION]
>
>目前不支援平行執行子網域 [!DNL Journey Optimizer]. 如果您嘗試提交子網域以進行委派，當另一個子網域具有 **[!UICONTROL 處理中]** 狀態，您會收到錯誤訊息。

## 子網域驗證 {#subdomain-validation}

將執行以下檢查和動作，直到驗證子網域並可用於傳送訊息為止。

>[!NOTE]
>
>這些步驟由Adobe執行，最多可能需要3小時。

1. **預先驗證**：Adobe會檢查子網域是否已委派給AdobeDNS （NS記錄、SOA記錄、區域設定、所有權記錄）。 如果預先驗證步驟失敗，則會傳回錯誤及相應原因，否則Adobe會進行下一個步驟。

1. **設定網域的DNS**：

   * **MX記錄**：郵件交換記錄 — 處理傳送到子網域的傳入電子郵件的郵件伺服器記錄。
   * **SPF記錄**：寄件者原則架構記錄 — 列出可從子網域傳送電子郵件的郵件伺服器IP。
   * **DKIM記錄**：DomainKeys Identified Mail標準記錄 — 使用公開私密金鑰加密來驗證郵件以避免詐騙。
   * **A**：預設IP對應。
   * **CNAME**：正式名稱或CNAME記錄是一種DNS記錄，將別名對應到真實或正式網域名稱。

1. **建立追蹤和映象URL**：如果網域為email.example.com，追蹤/映象網域將為data.email.example.com。 安裝SSL憑證即可確保安全性。

1. **布建CDN CloudFront**：如果尚未設定CDN，則Adobe會將其布建為您組織的ID。

1. **建立CDN網域**：如果網域為email.example.com，則CDN網域將為cdn.email.example.com。

1. **建立並附加CDN SSL憑證**：Adobe會為CDN網域建立CDN憑證，並將憑證附加至CDN網域。

1. **建立轉送DNS**：如果您所委派的第一個子網域，Adobe會建立轉送DNS，而這是PTR記錄的建立所需，每個IP各一個。

1. **建立PTR記錄**：ISP需要PTR記錄（也稱為反向DNS記錄），才能將電子郵件標示為垃圾郵件。 Gmail也建議每個IP都有PTR記錄。 Adobe只會在您第一次委派子網域時建立PTR記錄，每個IP各一個，所有IP都指向該子網域。 例如，如果IP為 *192.1.2.1* 而子網域為 *email.example.com*，PTR記錄會是： *192.1.2.1 PTR r1.email.example.com*. 您之後可以更新PTR記錄，以指向新的委派網域。 [深入瞭解PTR記錄](ptr-records.md)

## 操作說明影片{#video}

瞭解如何使用 CNAME 建立子網域以指向 Adobe 特定記錄。

>[!VIDEO](https://video.tv.adobe.com/v/339484?quality=12)
