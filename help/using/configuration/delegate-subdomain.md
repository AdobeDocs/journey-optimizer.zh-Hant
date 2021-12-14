---
title: 委派子網域
description: 了解如何委派子網域
page-status-flag: never-activated
uuid: null
contentOwner: null
products: null
audience: administrators
content-type: reference
topic-tags: null
discoiquuid: null
internal: n
snippet: y
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 8021f66e-7725-475b-8722-e6f8d74c9023
source-git-commit: c548852b976100935271afafd5267fd7f32a9b50
workflow-type: tm+mt
source-wordcount: '1396'
ht-degree: 6%

---

# 委派子網域

域名委派是一種允許域名所有者的方法(技術上：DNS區域)，以委派DNS區域(技術上：其下的DNS區域，可稱為子區域)，傳至其他實體。 基本上，身為客戶，如果您處理「example.com」區域，您可以委派子區域「marketing.example.com」給Adobe。

透過委派子網域以搭配使用 [!DNL Journey Optimizer]，客戶可仰賴Adobe來維護所需的DNS基礎架構，以符合其電子郵件行銷傳送網域的業界標準傳遞能力需求，同時持續維護和控制其內部電子郵件網域的DNS。

## 完全子網域委派 {#full-subdomain-delegation}

[!DNL Journey Optimizer] 可讓您直接從產品介面完全委派子網域以Adobe。 如此一來，Adobe便能控制並維護傳送、呈現及追蹤電子郵件行銷活動所需的DNS的所有層面，以托管服務的形式傳送訊息。

>[!NOTE]
>
>依預設， [!DNL Journey Optimizer] 授權合約可讓您委派最多10個子網域。 如果您想要增加此限制，請聯絡您的Adobe連絡人。

若要委派新子網域，請遵循下列步驟：

1. 存取 **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Subdomains]** ，然後按一下 **[!UICONTROL Set up subdomain]**.

   ![](../assets/subdomain-delegate.png)

1. 選擇 **[!UICONTROL Fully delegated]** 從 **[!UICONTROL Set up method]** 區段。

   ![](../assets/subdomain-method-full.png)

1. 指定要委派的子網域名稱。

   ![](../assets/subdomain-name.png)

   >[!CAUTION]
   >
   >不允許將無效的子網域委派至Adobe。 請務必輸入貴組織擁有的有效子網域，例如marketing.yourcompany.com。
   >
   >請注意，目前不支援電子郵件.marketing.yourcompany.com等多層級子網域。

1. 要放置在 DNS 伺服器顯示中的記錄清單。 逐一複製這些記錄，或下載 CSV 檔案，然後導覽至您的網域託管解決方案，以產生相符的 DNS 記錄。

1. 請確定所有DNS記錄都已產生至您的網域托管解決方案。 如果所有項目皆已正確設定，請核取「I confirm...」方塊，然後按一下 **[!UICONTROL Submit]**.

   ![](../assets/subdomain-submit.png)

   >[!NOTE]
   >
   >您稍後可以使用 **[!UICONTROL Save as draft]** 按鈕。 然後，您就可以從子網域清單中開啟子網域委派，以繼續進行子網域委派。

1. 提交完整的子網域委派後，子網域會顯示在清單中，並搭配 **[!UICONTROL Processing]** 狀態。 如需子網域狀態的詳細資訊，請參閱 [本節](access-subdomains.md).

   ![](../assets/subdomain-processing.png)

   在能夠使用該子網域來傳送訊息之前，您需要等到Adobe執行所需的檢查，最多需要3小時。 深入了解 [本節](#subdomain-validation).

   >[!NOTE]
   >
   >任何遺失的記錄（亦即尚未在您的托管解決方案上建立的記錄）都會列出。

1. 檢查成功後，子網域會取得 **[!UICONTROL Success]** 狀態。 它已準備好用於傳送訊息。

   >[!NOTE]
   >
   >子網域將標示為 **[!UICONTROL Failed]** 如果您未在托管解決方案上建立驗證記錄。

   <!-- later on, users will be notified in Pulse -->

將子網域委派至Adobe後， [!DNL Journey Optimizer]，則會自動建立PTR記錄並與此子域關聯。 [了解更多](ptr-records.md)

>[!CAUTION]
>
>中目前不支援並行執行子網域 [!DNL Journey Optimizer]. 如果您嘗試在另一個子網域具有 **[!UICONTROL Processing]** 狀態，您會收到錯誤訊息。

## CNAME子網域委派 {#cname-subdomain-delegation}

如果您有特定於域的限制策略，並且希望Adobe只對DNS有部分控制，則可以選擇在您的一方執行所有與DNS相關的活動。

CNAME子網域委派可讓您建立子網域，並使用CNAME指向Adobe特定記錄。 使用此設定，您和Adobe都有責任維護DNS，以便設定傳送、轉譯和追蹤電子郵件的環境。

>[!CAUTION]
>
>如果貴組織的原則限制完整的子網域委派方法，則建議使用此方法。 此方法需要您自行維護和管理DNS記錄。 Adobe將無法協助變更、維護或管理透過CNAME方法設定之子網域的DNS。

若要使用CNAME委派子網域，請遵循下列步驟：

1. 存取 **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Subdomains]** ，然後按一下 **[!UICONTROL Set up subdomain]**.

1. 選取 **[!UICONTROL CNAME set up]** 方法。

   ![](../assets/subdomain-method-cname.png)

   <!--The steps to specify the name of the subdomain to delegate and to generate the DNS records into your domain hosting solution are the same as for full subdomain delegation. See **steps 3 to 5** of the [Full subdomain delegation](#full-subdomain-delegation) section.)-->

1. 指定要委派的子網域名稱。

   >[!CAUTION]
   >
   >不允許將無效的子網域委派至Adobe。 請務必輸入貴組織擁有的有效子網域，例如marketing.yourcompany.com。
   >
   >請注意，目前不支援電子郵件.marketing.yourcompany.com等多層級子網域。

1. 要放置在 DNS 伺服器顯示中的記錄清單。 逐一複製這些記錄，或下載 CSV 檔案，然後導覽至您的網域託管解決方案，以產生相符的 DNS 記錄。

1. 請確定所有DNS記錄都已產生至您的網域托管解決方案。 如果所有項目皆已正確設定，請核取「I confirm...」方塊。

   ![](../assets/subdomain-create-dns-confirm.png)

   >[!NOTE]
   >
   >您稍後可以使用 **[!UICONTROL Save as draft]** 按鈕。 然後，您就可以從子網域清單開啟子網域委派，借此繼續此階段。

1. 等到Adobe驗證這些記錄是否已產生，且托管解決方案未發生錯誤。 此程式最多需要2分鐘。

   >[!NOTE]
   >
   >任何遺失的記錄（亦即尚未在您的托管解決方案上建立的記錄）都會列出。

1. Adobe會產生SSL CDN URL驗證記錄。 將此驗證記錄複製到您的托管平台。 如果您已在托管解決方案上正確建立此記錄，請核取方塊「I confirm...」，然後按一下 **[!UICONTROL Submit]**.

   ![](../assets/subdomain-cdn-url-validation.png)

   >[!NOTE]
   >
   >您也可以建立驗證記錄，並稍後使用 **[!UICONTROL Save as draft]** 按鈕。 然後，您就可以從子網域清單中開啟子網域委派，以繼續進行子網域委派。

1. 提交CNAME子網域委派後，子網域會顯示在清單中，並搭配 **[!UICONTROL Processing]** 狀態。 如需子網域狀態的詳細資訊，請參閱 [本節](access-subdomains.md).

   在能夠使用該子網域來傳送訊息之前，您需要等到Adobe執行所需檢查，這通常需要2到3小時。 深入了解 [本節](#subdomain-validation).

1. 檢查成功後<!--i.e Adobe validates the record you created and installs it-->，子網域會取得 **[!UICONTROL Success]** 狀態。 它已準備好用於傳送訊息。

   >[!NOTE]
   >
   >子網域將標示為 **[!UICONTROL Failed]** 如果您未在托管解決方案上建立驗證記錄。

在驗證記錄並安裝證書時，Adobe會自動為CNAME子域建立PTR記錄。 [了解更多](ptr-records.md)

>[!CAUTION]
>
>中目前不支援並行執行子網域 [!DNL Journey Optimizer]. 如果您嘗試在另一個子網域具有 **[!UICONTROL Processing]** 狀態，您會收到錯誤訊息。

## 子網域驗證 {#subdomain-validation}

將執行下列檢查和動作，直到子網域經過驗證，且可用於傳送訊息為止。

>[!NOTE]
>
>這些步驟由Adobe執行，最多需要3小時。

1. **預先驗證**:Adobe檢查子域是否已委派給AdobeDNS（NS記錄、SOA記錄、區域設定、所有權記錄）。 如果預先驗證步驟失敗，會傳回錯誤並出現對應的原因，否則Adobe會繼續執行下一個步驟。

1. **配置域的DNS**:

   * **MX記錄**:Mail eXchange記錄 — 處理髮送到子網域的傳入電子郵件的郵件伺服器記錄。
   * **SPF記錄**:發件人策略框架記錄 — 列出可從子域發送電子郵件的郵件伺服器的IP。
   * **DKIM記錄**:DomainKeys Indified Mail標準記錄 — 使用公私密鑰加密來驗證郵件以避免欺騙。
   * **A**:預設IP對應。
   * **CNAME**:規範名稱或CNAME記錄是一種DNS記錄，可將別名映射為真或規範網域名稱。

1. **建立追蹤和鏡像URL**:如果網域為email.example.com，則tracking/mirror網域將為data.email.example.com。 安裝SSL憑證可加以保護。

1. **布建CDN CloudFront**:如果尚未設定CDN，請Adobe為匯入設定CDN。

1. **建立CDN網域**:如果網域為email.example.com，則CDN網域將為cdn.email.example.com。

1. **建立並附加CDN SSL憑證**:Adobe會為CDN網域建立CDN憑證，並將憑證附加至CDN網域。

1. **建立轉發DNS**:如果這是要委派的第一個子域，則Adobe將建立建立PTR記錄所需的轉發DNS — 每個IP各一個。

1. **建立PTR記錄**:ISP需要PTR記錄（也稱為反向DNS記錄），以便它們不會將電子郵件標籤為垃圾郵件。 Gmail還建議為每個IP包含PTR記錄。 Adobe僅在您首次委派子網域時（每個IP各一個），即指向該子網域的所有IP時，才會建立PTR記錄。 例如，如果 *192.1.2.1* 而子網域為 *email.example.com*,PTR記錄將是： *192.1.2.1 PTR r1.email.example.com*. 之後，您可以更新PTR記錄以指向新的委派域。 [了解有關PTR記錄的更多資訊](ptr-records.md)
