---
solution: Journey Optimizer
product: journey optimizer
title: 外部資料來源
description: 了解如何設定外部資料來源
feature: Data Sources
topic: Administration
role: Admin
level: Intermediate
exl-id: f3cdc01a-9f1c-498b-b330-1feb1ba358af
source-git-commit: f6db4f7cbb1951c009fa7915f340da96eea74120
workflow-type: tm+mt
source-wordcount: '1365'
ht-degree: 0%

---

# 外部資料來源 {#external-data-sources}

>[!CONTEXTUALHELP]
>id="ajo_journey_data_source_custom"
>title="外部資料來源"
>abstract="外部資料來源可讓您定義與協力廠商系統的連線，例如如果您使用飯店訂房系統來檢查人員是否已註冊客房。 與內建的Adobe Experience Platform資料來源不同，您可以視需要建立盡量多的外部資料來源。"

外部資料來源可讓您定義與協力廠商系統的連線，例如如果您使用飯店訂房系統來檢查人員是否已註冊客房。 與內建的Adobe Experience Platform資料來源不同，您可以視需要建立盡量多的外部資料來源。

>[!NOTE]
>
>使用外部系統時的護欄列在 [本頁](../configuration/external-systems.md).

支援使用POST或GET，以及傳回JSON的REST API。 支援API金鑰、基本和自訂驗證模式。

讓我們以一個氣象API服務為例，我想使用它來根據即時氣象資料來自訂歷程的行為。

以下是API呼叫的兩個範例：

* _https://api.adobeweather.org/weather?city=London,uk&amp;appid=1234_
* _https://api.adobeweather.org/weather?lat=35&amp;lon=139&amp;appid=1234_

呼叫由主要URL(_https://api.adobeweather.org/weather_)、兩個參數集（「city」代表城市，「lat/long」代表經緯度）和API金鑰(appid)。

以下是建立和設定新外部資料來源的主要步驟：

1. 從資料來源清單中，按一下 **[!UICONTROL Create Data Source]** 建立新外部資料來源。

   ![](assets/journey25.png)

   這會開啟畫面右側的資料來源設定窗格。

   ![](assets/journey26.png)

1. 輸入資料源的名稱。

   >[!NOTE]
   >
   >請勿使用空格或特殊字元。 請勿使用超過30個字元。

1. 新增說明至您的資料來源。 此步驟為選用。
1. 新增外部服務的URL。 在我們的範例中： _https://api.adobeweather.org/weather_.

   >[!CAUTION]
   >
   >基於安全考量，我們強烈建議使用HTTPS。 另請注意，我們不允許使用非公開的Adobe位址和IP位址。

   ![](assets/journey27.png)

1. 根據外部服務配置配置身份驗證： **[!UICONTROL No authentication]**, **[!UICONTROL Basic]**, **[!UICONTROL Custom]** 或 **[!UICONTROL API key]**. 如需自訂驗證模式的詳細資訊，請參閱 [本節](../datasource/external-data-sources.md#custom-authentication-mode). 在我們的範例中，我們選取：

   * **[!UICONTROL Type]**:&quot;API金鑰&quot;
   * **[!UICONTROL Name]**:&quot;appid&quot;（這是API金鑰參數名稱）
   * **[!UICONTROL Value]**:&quot;1234&quot;（這是我們API金鑰的值）
   * **[!UICONTROL Location]**:&quot;Query parameter&quot;（API金鑰位於URL中）

   ![](assets/journey28.png)

1. 按一下「 」，為每個API參數集新增欄位群組 **[!UICONTROL Add a New Field Group]**. 請勿在欄位群組名稱中使用空格或特殊字元。 在我們的範例中，我們需要建立兩個欄位群組，每個群組各一個參數集（city及long/lat）。

對於&quot;long/lat&quot;參數集，我們會建立包含下列資訊的欄位群組：

* **[!UICONTROL Used in]**:顯示使用欄位群組的歷程數。 您可以按一下 **[!UICONTROL View journeys]** 圖示以顯示使用此欄位群組的歷程清單。
* **[!UICONTROL Method]**:選擇POST或GET方法。 在本例中，我們選取GET方法。
* **[!UICONTROL Dynamic Values]**:在本例中，輸入以逗號分隔的不同參數，即&quot;long,lat&quot;。 由於參數值視執行內容而定，因此會在歷程中定義。 [深入了解](../building-journeys/expression/expressionadvanced.md)
* **[!UICONTROL Response Payload]**:按一下內部 **[!UICONTROL Payload]** 欄位，並貼上呼叫傳回之有效負載的範例。 例如，我們使用了氣象API網站上找到的裝載。 驗證欄位類型是否正確。 每次呼叫API時，系統都會擷取裝載範例中包含的所有欄位。 請注意，您可以按一下 **[!UICONTROL Paste a new payload]** 如果您想要變更目前傳遞的裝載。
* **[!UICONTROL Sent Payload]**:此欄位不會出現在範例中。 只有選取POST方法時才可用。 貼上將傳送至協力廠商系統的裝載。

若是GET呼叫所需的參數，請在 **[!UICONTROL Dynamic Values]** 欄位，且這些欄位會在呼叫結束時自動新增。 若是POST呼叫，您需要：

* 列出呼叫時要傳遞的參數，位於 **[!UICONTROL Dynamic Values]** 欄位(在以下範例中：&quot;identifier&quot;)。
* 在已傳送裝載的正文中，也使用完全相同的語法來指定它們。 若要這麼做，您需要新增：&quot;param&quot;:&quot;name of your parameter&quot;(在以下範例中：&quot;identifier&quot;)。 請遵循下列語法：

   ```
   {"id":{"param":"identifier"}}
   ```

![](assets/journey29.png)

按一下 **[!UICONTROL Save]**.

資料來源現在已設定完畢，且可供您在歷程中使用，例如在您的條件中，或個人化電子郵件。 如果溫度高於30°C，您可以決定傳送特定通訊。

## 自訂驗證模式{#custom-authentication-mode}

>[!CONTEXTUALHELP]
>id="jo_authentication_payload"
>title="關於自訂驗證"
>abstract="自訂驗證模式會用於複雜驗證，以呼叫OAuth2等API封裝通訊協定。 動作執行是兩步驟程式。 首先，會執行端點呼叫以產生存取權杖。 接著，存取權杖會插入到動作的HTTP要求中。"

此驗證模式會用於複雜驗證，常用來呼叫OAuth2等API封裝通訊協定，以擷取要插入到動作之實際HTTP要求中的存取權杖。

設定自訂驗證時，您可以按一下下方的按鈕，以檢查自訂驗證裝載是否已正確設定。

![](assets/journey29-bis.png)

如果測試成功，按鈕會變成綠色。

![](assets/journey29-ter.png)

透過此驗證，動作執行是兩步驟程式：

1. 呼叫端點以產生存取權杖。
1. 以正確的方式插入存取權杖，以呼叫REST API。

此驗證分為兩部分。

要呼叫以產生存取權杖之端點的定義：

* 端點：用於產生端點的URL
* 端點上HTTP要求的方法（GET或POST）
* 標題：需要時，要插入做為此呼叫標題的機碼值組
* 內文：說明方法為POST時呼叫的正文。 我們支援有限的內文結構，定義於bodyParams（機碼 — 值組）中。 bodyType說明呼叫內內文的格式和編碼：
   * &#39;form&#39;:這表示內容類型將會是application/x-www-form-urlencoded（字元集UTF-8），而金鑰值配對將會序列化為：key1=value1&amp;key2=value2&amp;...
   * &#39;json&#39;:這表示內容類型將會是application/json（字元集UTF-8），而機碼值配對將會序列化為JSON物件，如下所示： _{ &quot;key1&quot;:&quot;value1&quot;, &quot;key2&quot;:&quot;value2&quot;, ...}_

存取權杖插入動作之HTTP要求中必須方式的定義：

* authorizationType:定義如何將產生的存取權杖插入動作的HTTP呼叫中。 可能的值為：

   * 承載者：指出存取權杖必須插入到授權標題中，例如： _授權：承載 &lt;access token=&quot;&quot;>_
   * 標題：指出存取權杖必須插入為標題，而標題名稱是由屬性tokenTarget定義。 例如，若tokenTarget為myHeader，則存取權杖會插入為標題，如下所示： _myHeader: &lt;access token=&quot;&quot;>_
   * queryParam:指出存取權杖必須插入為queryParam，而查詢參數名稱由屬性tokenTarget定義。 例如，若tokenTarget是myQueryParam，則動作呼叫的URL將會是： _&lt;url>?myQueryParam=&lt;access token=&quot;&quot;>_

* tokenInResponse:指出如何從驗證呼叫中擷取存取權杖。 此屬性可以是：
   * &#39;response&#39;:表示HTTP回應是存取權杖
   * json中的選取器（假設回應是json，則不支援XML等其他格式）。 此選取器的格式為 _json://&lt;path to=&quot;&quot; the=&quot;&quot; access=&quot;&quot; token=&quot;&quot; property=&quot;&quot;>_. 例如，如果呼叫的回應是： _{ &quot;access_token&quot;:&quot;theToken&quot;、&quot;timestamp&quot;:12323445656 }_,tokenInResponse將會是： _json://access_token_

此驗證的格式為：

```
{
    "type": "customAuthorization",
    "authorizationType": "<value in 'bearer', 'header' or 'queryParam'>",
    (optional, mandatory if authorizationType is 'header' or 'queryParam') "tokenTarget": "<name of the header or queryParam if the authorizationType is 'header' or 'queryParam'>",
    "endpoint": "<URL of the authentication endpoint>",
    "method": "<HTTP method to call the authentication endpoint, in 'GET' or 'POST'>",
    (optional) "headers": {
        "<header name>": "<header value>",
        ...
    },
    (optional, mandatory if method is 'POST') "body": {
        "bodyType": "<'form'or 'json'>,
        "bodyParams": {
            "param1": value1,
            ...

        }
    },
    "tokenInResponse": "<'response' or json selector in format 'json://<field path to access token>'"
}
```

您可以變更自訂驗證資料來源之權杖的快取期間。 以下是自訂驗證裝載的範例。 快取持續時間在「cacheDuration」參數中定義。 它會指定快取中產生代號的保留期間。 單位可以是毫秒、秒、分鐘、小時、天、月、年。

```
"authentication": {
    "type":"customAuthorization",
    "authorizationType":"Bearer",
    "endpoint":"http://localhost:${port}/epsilon/oauth2/access_token",
    "method":"POST",
    "headers": {
        "Authorization":"Basic EncodeBase64(${epsilonClientId}:${epsilonClientSecret})"
        },
    "body": {
        "bodyType":"form",
        "bodyParams": {
             "scope":"cn mail givenname uid employeeNumber",
             "grant_type":"password",
             "username":"${epsilonUserName}",
             "password":"${epsilonUserPassword}"
             }
        },
    "tokenInResponse":"json://access_token",
    "cacheDuration":
             { "duration":5, "timeUnit":"seconds" }
    }
```

>[!NOTE]
>
>快取持續時間有助於避免對驗證端點發出太多呼叫。 在服務中快取驗證權杖保留，沒有持續性。 如果服務重新啟動，則會以乾淨的快取開始。 預設的快取持續時間為1小時。 在自訂驗證裝載中，可借由指定其他保留期間來調整。
