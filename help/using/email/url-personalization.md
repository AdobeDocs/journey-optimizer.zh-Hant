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
source-git-commit: 91b9ce5398bd62ff1969374be6e5c9f720fb4e31
workflow-type: tm+mt
source-wordcount: '402'
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

<!--
## Best practices and guardrails {#best-practices}

To keep links valid, clickable, and trackable, follow the best practices and guardrails below.

### Braces for dynamic URLs {#use-braces}

When inserting a URL that contains personalization, use three curly braces (`{{{ ... }}}`) for the dynamic portion of the URL. This prevents escaping from altering special characters (for example `/` and `+`) and helps avoid broken URLs, incorrect redirects, or tracking issues.

Here is an example:

```html
<a href="https://example.com/path/{{{profile.person.customSlug}}}?ref={{{context.system.source.id}}}">View details</a>
```

>[!IMPORTANT]
>
>Using raw output (`{{{ ... }}}`) means the value is inserted as-is. Only use it with values you trust and that are intended to be URL-safe (for example, values you generate or validate upstream).

### Correct URL tracking {#enable-url-tracking}

* When using personalization to generate the URL, ensure the resolved value starts with `http`/`https` for every recipient. Otherwise, tracking may not be applied and the link may not behave as expected.

* Do not use dynamic logic such as `let`, `each`, or `if` statements directly in the personalization editor's URL field. These are disabled for security reasons.

* If your scenario involves complex logic to generate personalized URLs, avoid placing that logic directly in the personalization editor's URL field. Instead:
    * Add the necessary logic and statements in the HTML content above or near the URL field.
    * Generate and store personalized attributes separately, then reference them in your email content.

### URL encoding and length {#encoding}

* URI syntax rules ([RFC 3986 standard](https://datatracker.ietf.org/doc/html/rfc3986){target="_blank"}) apply to all URLs in your email content. However, personalized URLs are more likely to surface encoding issues because recipient-specific values can introduce reserved characters (for example in query parameters). Therefore, ensure your dynamic values are URL-encoded (especially spaces, `&`, `#`, `%`, and `+`) and avoid using `+` for query values.

* Very long URLs can be truncated or rejected by browsers, mail clients, or downstream systems. For example, mirror page URLs can grow significantly when runtime personalization is heavy. Keep personalized payloads small and avoid embedding large objects into URLs.

### Recommended validation steps {#validation}

Before activating a journey or campaign, follow the recommendations below:

* Send a [proof](../content-management/proofs.md) and click links to confirm the resolved URL starts with `http`/`https` and keeps the expected structure.
* If tracking parameters are appended, confirm the final URL includes them (either via configuration-level URL tracking or per-link tracking parameters).
-->
