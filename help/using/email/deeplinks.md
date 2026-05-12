---
solution: Journey Optimizer
product: journey optimizer
title: 在電子郵件訊息中使用深層連結
description: 瞭解如何新增深層連結至電子郵件內容，以及如何在iOS和Android應用程式中實作深層連結處理。
feature: Email
topic: Content Management
role: User, Developer
level: Intermediate
keywords: 深層連結，深層連結，通用連結，應用程式連結，電子郵件
source-git-commit: 8efe5aaf0ebf24aa61decf40651c2ecc198ab0bc
workflow-type: tm+mt
source-wordcount: '1182'
ht-degree: 1%

---


# 在電子郵件中設定深層連結 {#email-deeplinks}

電子郵件中的深層連結，可協助您將收件者從電子郵件帶至行動應用程式中的特定畫面或內容片段。 它有助於引導人們直接使用預期的應用程式內體驗，而不需透過網頁瀏覽器或應用程式商店路由，讓歷程保持在相關性和品牌上。

若要新增深層連結至電子郵件，請確定[連結追蹤已啟用](message-tracking.md#enable-tracking)。 在電子郵件Designer中選取您要連結的元素（文字、按鈕或影像），按一下內容工具列中的&#x200B;**[!UICONTROL 插入連結]**，然後選擇&#x200B;**[!UICONTROL 深層連結]**&#x200B;以輸入深層連結URL。 [進一步瞭解插入連結](message-tracking.md#insert-links)

當您的收件者按一下深層連結時，就會直接導向至預期的應用程式內內容 — **前提是您已完成此頁面上詳述的設定步驟**，其中涵蓋：

* 如何在Journey Optimizer中設定電子郵件的深層連結
* 如何在行動應用程式中為iOS和Android實作深層連結處理

>[!NOTE]
>
>[!DNL Adobe Journey Optimizer]支援使用追蹤的URL (`/ee/v1/mclick/*`)對iOS和Android進行深層連結，以確保相容性和點選追蹤。

## Journey Optimizer中的設定 {#configuration}

若要在行動應用程式的電子郵件中使用深層連結，請完成下列設定步驟。

>[!NOTE]
>
>此區段適用於您使用&#x200B;**通用連結(iOS)**&#x200B;和&#x200B;**應用程式連結(Android)** （HTTPS型深層連結）的情況。

1. 在Journey Optimizer中，委派已啟用深層連結的子網域。 [了解更多](../configuration/delegate-subdomain.md)

1. 在您的子網域上託管iOS的AASA檔案和Android的assetLinks.json檔案。 請聯絡[Adobe客戶服務](https://helpx.adobe.com/tw/enterprise/admin-guide.html/enterprise/using/support-for-experience-cloud.ug.html){target="_blank"}或您的Adobe代表，並提供下列詳細資料：

   * 針對iOS (AASA)**&#x200B;**：
      * 委派的子網域
      * 應用程式套件組合ID
   * **若為Android (assetLinks.json)**：
      * 委派的子網域
      * 應用程式套件組合ID
      * SHA-256憑證指紋

>[!IMPORTANT]
>
>啟用[連結追蹤](message-tracking.md#enable-tracking)時，會套用透過Adobe電子郵件基礎結構的深層連結。 追蹤的深層連結點選使用`/ee/v1/mclick/*`下的URL，Adobe會託管並解析。
>
>對於&#x200B;**個未追蹤的**&#x200B;連結，不會透過Adobe系統重新寫入URL。 您必須在自己的網域和託管上設定通用連結或應用程式連結，讓這些連結可依預期開啟您的應用程式。

## 行動應用程式實施 {#mobile-implementation}

本節說明如何使用[!DNL Adobe Journey Optimizer]實作行動深層連結，以便在典型的&#x200B;**HTTPS**&#x200B;設定中（通用連結和應用程式連結），單一URL可以：

* 安裝應用程式時，在行動應用程式內開啟特定畫面，或
* 未安裝應用程式時開啟您的網站作為遞補。

當您的郵件啟用[連結追蹤](message-tracking.md#enable-tracking)時，[!DNL Journey Optimizer]會繼續追蹤這些點按，將它們納入報告中，而且如果您在郵件上執行這些點按，則可以在[內容實驗](../content-management/content-experiment.md)中使用它們。

本節提供深層連結的常見實作模式。 確切的設定取決於應用程式架構和路由架構。

### iOS （通用連結） {#ios-implementation}

1. 在Xcode中，透過&#x200B;**[!UICONTROL 簽署與功能]** > **[!UICONTROL +功能]** > **[!UICONTROL 關聯的網域]**&#x200B;來選取您的目標。
1. 為您委派的子網域新增專案，例如：

   ```text
   applinks:www.mybusiness.com
   applinks:data.email.mybusiness.com
   ```

1. 在應用程式中處理通用連結，並從回應標題取得原始連結。

   +++ 範例：iOS 13+搭配場景

   ```swift
   class SceneDelegate: UIResponder, UIWindowSceneDelegate {
   
       func scene(_ scene: UIScene,
                 continue userActivity: NSUserActivity) {
           guard userActivity.activityType == NSUserActivityTypeBrowsingWeb,
                 let incomingURL = userActivity.webpageURL else {
               return
           }
   
           handleUniversalLink(url: incomingURL)
       }
   
       private func handleUniversalLink(url: URL) {
           // Only handle AJO tracked mobile clicks
           guard url.host == "data.email.mybusiness.com",
                 url.path.hasPrefix("/ee/v1/mclick") else {
               // Could also handle direct www.mybusiness.com links here
               return
           }
   
           resolveTrackedUrlAndRoute(url)
       }
   
       private func resolveTrackedUrlAndRoute(_ trackedUrl: URL) {
           var request = URLRequest(url: trackedUrl)
           request.httpMethod = "GET"
   
           URLSession.shared.dataTask(with: request) { _, response, error in
               guard error == nil,
                     let httpResponse = response as? HTTPURLResponse,
                     let locationValue = httpResponse.allHeaderFields["Location"] as? String,
                     let finalUrl = URL(string: locationValue) else {
                   return
               }
   
               DispatchQueue.main.async {
                   self.routeToDestination(finalUrl)
               }
           }.resume()
       }
   
       private func routeToDestination(_ url: URL) {
           // Example: map URL paths to screens
           // https://www.mybusiness.com/dashboard/offers/coupons
           // → OffersViewController for Coupons
       }
   }
   ```

   +++

>[!IMPORTANT]
>
>應用程式必須在`mclick` URL上執行&#x200B;**GET**&#x200B;並讀取&#x200B;**`Location`**&#x200B;標題，然後根據&#x200B;**最終** URL路由。
>
>請勿僅在Safari中開啟`mclick` URL；這會破壞深層連結的目的。

### Android （應用程式連結） {#android-implementation}

1. 在您的Android應用程式中新增應用程式連結意圖篩選器。

   ```xml
   <activity
       android:name=".DeepLinkActivity"
       android:exported="true">
   
       <intent-filter android:autoVerify="true">
           <action android:name="android.intent.action.VIEW" />
           <category android:name="android.intent.category.DEFAULT" />
           <category android:name="android.intent.category.BROWSABLE" />
   
           <data
               android:scheme="https"
               android:host="data.email.mybusiness.com"
               android:pathPrefix="/ee/v1/mclick" />
       </intent-filter>
   
   </activity>
   ```

1. 實作深層連結處理常式。

   +++ 在Kotlin：

   ```kotlin
   class DeepLinkActivity : AppCompatActivity() {
   
       override fun onCreate(savedInstanceState: Bundle?) {
           super.onCreate(savedInstanceState)
   
           val trackedUri = intent?.data
           if (trackedUri == null ||
               trackedUri.host != "data.email.mybusiness.com" ||
               !trackedUri.path.orEmpty().startsWith("/ee/v1/mclick")) {
               finish()
               return
           }
   
           resolveTrackedUrlAndRoute(trackedUri)
       }
   
       private fun resolveTrackedUrlAndRoute(trackedUri: Uri) {
           lifecycleScope.launch(Dispatchers.IO) {
               try {
                   val finalUrl = followRedirect(trackedUri.toString())
                   withContext(Dispatchers.Main) {
                       routeToDestination(finalUrl)
                       finish()
                   }
               } catch (e: Exception) {
                   // Optionally log error, fallback to browser
                   finish()
               }
           }
       }
   
       private fun followRedirect(trackedUrl: String): Uri {
           val client = OkHttpClient.Builder()
               .followRedirects(false) // We want to read Location ourselves
               .build()
   
           val request = Request.Builder()
               .url(trackedUrl)
               .get()
               .build()
   
           client.newCall(request).execute().use { response ->
               val location = response.header("Location")
                   ?: throw IllegalStateException("Missing Location header")
               return Uri.parse(location)
           }
       }
   
       private fun routeToDestination(finalUri: Uri) {
           // Example: interpret https://www.mybusiness.com/dashboard/offers/coupons
           // and open the correct Activity / Fragment
       }
   }
   ```

   +++

>[!IMPORTANT]
>
>就像iOS一樣，應用程式必須呼叫`mclick` URL並使用&#x200B;**`Location`**&#x200B;標頭來決定最終目的地。
>
>使用`followRedirects(false)`來控制重新導向處理，並視需要準確地記錄分析。
>
>路由邏輯供應用程式專用；可定義從URL到畫面的清晰對應。

## 建議作法 {#deeplink-best-practices}

* **使用穩定路徑**：偏好可復原應用程式UI變更的路由（例如`/account/orders`而非`/tab/3/view/2`）。
* **將追蹤的路徑列入帳戶**：啟用連結追蹤時，點按的連結可能會使用追蹤的路徑模式（例如`/ee/v1/mclick/`）。 請確定您的路由器可在解析追蹤的連結後剖析最終URL。
* **讓引數維持可預測**：定義一致的引數配置（例如`?orderId=12345`）。
* **避免URL中的敏感資料**：請勿將機密或個人資料直接放入深層連結URL。
* **測試您的深層連結**：傳送校樣，然後按一下已安裝應用程式之裝置上的深層連結。
* **在真實裝置上進行驗證**：在實體裝置上進行驗證時，通用連結和追蹤連結解析行為會比在模擬器上更可靠。
* **驗證應用程式端路由**：如果深層連結未開啟預期的畫面，請驗證應用程式端路由和URL格式（主機/路徑/查詢和URL編碼）。
* **請記得應用程式初始化**：應用程式連結/通用連結行為在安裝及開啟應用程式至少一次後最為可靠。

## 疑難排解和常見問答( FAQ) {#troubleshooting-faq}

+++ 我點選深層連結時，應用程式未開啟。

* 驗證URL是否與您的應用程式註冊要處理的主機及路徑模式相符，包括在啟用連結追蹤時追蹤的點選路徑（例如`/ee/v1/mclick/`下的路徑）。
* 針對iOS通用連結和Android應用程式連結，請確認網域關聯(AASA / `assetlinks.json`)已正確設定且可供存取。
* 在真實裝置上進行測試（模擬器/模擬器對於連結關聯可能會有不同的行為）。

+++

+++ 應用程式隨即開啟，但未導覽至預期的畫面。

* 確認應用程式端路由器正確剖析URL路徑/查詢。
* 檢查URL編碼：保留的字元應使用URL編碼。
* 驗證引數名稱和值符合路由器的預期。

+++

+++ 如果未安裝應用程式，會發生什麼事？

* 如果您的網站可以提供相同的HTTPS URL，則連結會在應用程式未安裝時開啟網頁作為遞補（相應地設定您的網頁目的地和路由）。

+++

+++ 如何在引數中安全地包含特殊字元？

以URL編碼查詢引數值。 這可減少傳送和轉譯問題，並有助於防止應用程式發生剖析錯誤。

+++

+++ 我們應該如何測試端對端？

* 使用深層連結建立校訂，在iOS和Android裝置（已安裝或未安裝的情況）上按一下。
* 驗證：
   * 最終電子郵件連結值（主機/路徑/查詢）
   * 作業系統層級的關聯（如果使用通用連結/應用程式連結）
   * 應用程式內路由結果

+++

+++ 我有一個應用程式，但組織的子網域不同。 我是否應該要求為每個子網域建立AASA和assetLinks.json？

是。 如果您想要在每個委派的子網域上進行深層連結，請要求支援此功能的每個子網域的AASA和`assetlinks.json`設定。

+++

+++ 我設定的URL是否應該使用深層連結格式（例如`appname://path`）？

您可以使用自訂URL配置（例如`appname://path`），但建議的方法是通用連結或應用程式連結(`https://`)，符合此頁面設定與實作區段中的HTTPS設定。

+++

+++ URL上的UTM引數是否可在行動應用程式中用於分析？

可以。 當應用程式在`mclick` URL上執行GET時，您在[!DNL Journey Optimizer]中設定的UTM引數會包含在`Location`標頭中傳回的最終URL中，以便您將其用於應用程式內分析。

+++

+++ `/ee/v1/click/` URL的使用者體驗為何？

連結會在裝置的預設網頁瀏覽器中開啟（標準點選追蹤行為），而非透過本頁面所述的`mclick`流程以應用程式深層連結處理。

+++

