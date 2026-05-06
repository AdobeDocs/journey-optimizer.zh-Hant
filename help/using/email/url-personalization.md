---
solution: Journey Optimizer
product: journey optimizer
title: 個人化電子郵件中的URL
description: 瞭解以動態方式產生URL，同時保持追蹤可靠的最佳實務和限制
feature: Email Design, Monitoring
topic: Content Management
role: User
level: Intermediate, Experienced
keywords: url，連結，個人化，追蹤，編碼，大括弧
source-git-commit: 36fad8d6c200118210794249fa12263ae70e5422
workflow-type: tm+mt
source-wordcount: '760'
ht-degree: 1%

---

# 個人化電子郵件中的URL {#url-personalization}

個人化URL可協助您透過[!DNL Journey Optimizer]電子郵件訊息傳遞內容體驗，例如產生收件者特定連結或附加動態引數。

收件者會根據設定檔屬性，將收件者帶往網站的特定頁面或個人化的微網站。

## 個人化URL {#personalize-url}

若要個人化URL，請遵循下列步驟。

1. 在電子郵件Designer中，選取內容中的元素，並使用內容工具列[插入連結](message-tracking.md#insert-links)。

   >[!IMPORTANT]
   >
   >Personalization僅適用於&#x200B;**[!UICONTROL 外部連結]**、**[!UICONTROL 取消訂閱連結]**&#x200B;和&#x200B;**[!DNL Opt-Out]**。 請務必選取適當的連結型別。

1. 選取個人化圖示。

   ![](assets/message-tracking-insert-link-perso.png)

1. 使用個人化編輯器新增您想要個人化URL的設定檔屬性。

1. 儲存您的變更。

以下是一些個人化URL的範例：

* `https://www.adobe.com/users/{{profile.person.name.lastName}}`
* `https://www.adobe.com/users?uid={{profile.person.name.firstName}}`
* `https://www.adobe.com/usera?uid={{context.journey.technicalProperties.journeyUID}}`
* `https://www.adobe.com/users?uid={{profile.person.crmid}}&token={{context.token}}`

>[!NOTE]
>
>在個人化編輯器中編輯個人化URL時，基於安全考量，會停用協助程式功能和對象成員資格。
>
>url內使用的個人化權杖不支援空格。

若要獲得可靠的演算和追蹤，請遵循下列[最佳實務和護欄](#best-practices)。

## 個人化完整/基本URL {#personalize-complete-base-url}

Journey Optimizer也支援個人化&#x200B;**整個** URL或URL的&#x200B;**基本網域**，例如：

```html
<a href="{{profile.social.link}}" />
<a href="{{profile.social.baseUrl}}/profile" />
<a href="https://{{profile.social.baseUrl}}/profile" />
```

>[!IMPORTANT]
>
>若要啟用完整或基本URL個人化，請聯絡Adobe並提供您接受的網域清單。 這有助於防止不安全的重新導向。

## 個人化URL追蹤引數 {#personalize-url-tracking-parameters}

[URL追蹤](url-tracking.md)是在頻道設定層級管理，並套用至訊息內容中包含的所有URL。 您也可以為電子郵件Designer中的個別連結個人化URL追蹤引數。 這可讓您將收件者特有的引數附加至單一連結（例如，將識別碼傳遞至網頁分析工具）。

若要這麼做，[插入連結](message-tracking.md#insert-links)、選取個人化圖示、新增URL追蹤引數，並從[個人化編輯器](../personalization/personalization-build-expressions.md)中選取您選擇的設定檔屬性。

![](assets/message-tracking-perso-parameter.png)

針對您要新增此追蹤引數的每個連結，重複上述步驟。

現在，當電子郵件寄出時，此引數會自動附加至URL的結尾。 接著，您就可以在網站分析工具或效能報表中擷取此引數。

>[!NOTE]
>
>若要驗證最終URL，您可以[傳送校樣](../content-management/proofs.md)，並在收到校樣後按一下電子郵件內容中的連結。 URL應顯示追蹤引數。 例如︰<https://luma.enablementadobe.com/content/luma/us/en.html?utm_contact=profile.userAccount.contactDetails.homePhone.number>

## 最佳作法和護欄 {#best-practices}

若要保持連結有效、可點按且可追蹤，請遵循下列最佳實務和護欄。

### 動態URL的大括弧 {#use-braces}

插入包含個人化的URL時，請對URL的動態部分使用三個大括弧(`{{{ ... }}}`)。 這可以防止逸出變更特殊字元（例如`/`和`+`），並有助於避免URL損毀、重新導向錯誤或追蹤問題。

其範例如下：

```html
<a href="https://example.com/path/{{{profile.person.customSlug}}}?ref={{{context.system.source.id}}}">View details</a>
```

>[!IMPORTANT]
>
>使用原始輸出(`{{{ ... }}}`)表示值會依原樣插入。 請僅將其用於您信任且預計可在URL中執行的值（例如，您產生或驗證上游的值）。

### 正確的URL追蹤 {#enable-url-tracking}

* 使用個人化來產生URL時，請確定每個收件者的解析值都以`http`/`https`開頭。 否則，可能不會套用追蹤，且連結可能不會如預期般運作。

* 請勿直接在個人化編輯器的URL欄位中使用動態邏輯，例如`let`、`each`或`if`陳述式。 基於安全考量已停用這些功能。

* 如果您的案例涉及產生個人化URL的複雜邏輯，請避免將該邏輯直接放入個人化編輯器的URL欄位中。 請改為使用：
   * 在HTML內容中，在URL欄位上方或附近新增必要的邏輯和陳述式。
   * 分別產生和儲存個人化屬性，然後在電子郵件內容中參考這些屬性。

### URL編碼和長度 {#encoding}

* URI語法規則([RFC 3986 standard](https://datatracker.ietf.org/doc/html/rfc3986){target="_blank"})適用於電子郵件內容中的所有URL。 不過，個人化URL更有可能發生編碼問題，因為收件者特定的值可能會引入保留字元（例如在查詢引數中）。 因此，請確定您的動態值為URL編碼（尤其是空格、`&`、`#`、`%`和`+`），並避免使用`+`作為查詢值。

* 瀏覽器、郵件使用者端或下游系統可能會截斷或拒絕過長的URL。 例如，當執行階段個人化繁重時，映象頁面URL可能會大幅增加。 將個人化裝載維持在較小規模，並避免將大型物件內嵌至URL。

### 建議的驗證步驟 {#validation}

在啟用歷程或行銷活動之前，請遵循以下建議：

* 傳送[校訂](../content-management/proofs.md)並按一下連結，以確認解析的URL以`http`/`https`開頭，並保留預期結構。
* 如果附加追蹤引數，請確認最終URL包含這些引數（透過設定層級URL追蹤或每個連結追蹤引數）。

