---
solution: Journey Optimizer
product: journey optimizer
title: 欄位參考
description: 瞭解進階運算式中的欄位參考
feature: Journeys
role: Developer
level: Experienced
keywords: 歷程，欄位，運算式，事件
exl-id: 2348646a-b205-4b50-a08f-6625e92f44d7
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/G8ooc1R2PwL06V89EBs-jH8Lf43F6q5xj3I4Wl6hDHk
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1044
ht-degree: 1%

---

# 欄位參考 {#field-references}

欄位參考可附加至事件或欄位群組。 唯一有意義的資訊是欄位名稱及其路徑。

如果您在欄位中使用特殊字元，則必須使用雙引號或簡單引號。 以下是需要引號的情況：

* 欄位以數字字元開頭
* 欄位以「 — 」字元開頭
* 欄位包含&#x200B;_a_-_z_、_A_-_Z_、_0_-_9_、_、_-_以外的任何專案

例如，如果您的欄位是&#x200B;_3h_： _#{OpenWeather.weatherData.rain.&#39;3h&#39;} > 0_

```json
// event field
@event{<event name>.<XDM path to the field>}
@event{LobbyBeacon.endUserIDs._experience.emailid.id}

// field group
#{<data source name>.<field group name>.<path to the field>}
#{ExperiencePlatform.ProfileFieldGroup.profile.personalEmail.address}
```

在運算式中，事件欄位以「@」參照，資料來源欄位以「#」參照。

語法顏色是用來在視覺上區分事件欄位（綠色）與欄位群組（藍色）。

## 欄位參考的預設值 {#default-value}

預設值可與欄位名稱相關聯。 語法如下：

```json
// event field
@event{<event name>.<XDM path to the field>, defaultValue: <default value expression>}
@event{LobbyBeacon.endUserIDs._experience.emailid.id, defaultValue: "example@adobe.com"}
// field group
#{<data source name>.<field group name>.<path to the field>, defaultValue: <default value expression>}
#{ExperiencePlatform.ProfileFieldGroup.profile.personalEmail.address, defaultValue: "example@adobe.com"}
```

>[!NOTE]
>
>欄位型別和預設值必須相同。 例如，`@event{LobbyBeacon.endUserIDs._experience.emailid.id, defaultValue : 2}`無效，因為預設值是整數，而預期值應為字串。

範例:

```json
// for an event 'OrderEvent' having the following payload:
{
    "orderId": "12345"
}
 
expression example:
- @event{OrderEvent.orderId}                                    -> "12345"
- @event{OrderEvent.productId, defaultValue : "not specified" } -> "not specified" // default value, productId is not a field present in the payload
- @event{OrderEvent.productId}                                  -> null
 
 
// for an entity 'Profile' on datasource 'ACP' having fields person/lastName, with fetched data such as:
{
    "person": {
        "lastName":"Snow"
    },
    "emails": [
        { "email":"john.snow@winterfell.westeros" },
        { "email":"snow@thewall.westeros" }
    ]
}
 
expression examples:
- #{ACP.Profile.person.lastName}                 -> "Snow"
- #{ACP.Profile.emails.at(1).email}              -> "snow@thewall.westeros"
- #{ACP.Profile.person.age, defaultValue : -1}   -> -1 // default value, age is not a field present in the payload
- #{ACP.Profile.person.age}                      -> null
```

您可以將任何種類的運算式新增為預設值。 唯一的限制是運算式必須傳回預期的資料型別。 使用函式時，需要使用()封裝函式。

```
#{ExperiencePlatform.Subscriptions.profile.consents.marketing.any.time, defaultValue : (now())} 
== date("2022-02-10T00:00:00Z")
```

## 集合內欄位的參考

集合中定義的元素是使用特定函式`all`、`first`和`last`參考。 如需詳細資訊，請參閱[本頁面](../expression/collection-management-functions.md)。

範例：

```json
@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.all()
```

## 參照地圖中定義的欄位

### `entry`函式

為了擷取對應中的元素，我們使用具有給定索引鍵的專案函式。 例如，根據選取的名稱空間，定義事件的索引鍵時會使用它。 如需詳細資訊，請參閱[此頁面](../../event/about-creating.md#select-the-namespace)。

```json
@event{MyEvent.identityMap.entry('Email').first().id}
```

在此運算式中，我們會取得事件之「IdentityMap」欄位的「Email」索引鍵專案。 &#39;Email&#39;專案是集合，我們使用&#39;first()&#39;從其中取得第一個元素中的&#39;id&#39;。 如需詳細資訊，請參閱[此頁面](../expression/collection-management-functions.md)。

### `firstEntryKey`函式

若要擷取對映的第一個專案索引鍵，請使用`firstEntryKey`函式。

此範例顯示如何擷取特定清單中訂閱者的第一個電子郵件地址：

```json
#{ExperiencePlatform.Subscriptions.profile.consents.marketing.email.subscriptions.entry('daily-email').subscribers.firstEntryKey()}
```

在此範例中，訂閱清單名為`daily-email`。 電子郵件地址在`subscribers`對應中定義為金鑰，此對應連結至訂閱清單對應。

### `keys`函式

若要擷取對應的所有索引鍵，請使用`keys`函式。

此範例說明如何針對特定設定檔擷取與特定清單訂閱者相關聯的所有電子郵件地址：

```json
#{ExperiencePlatform.Subscriptions.profile.consents.marketing.email.subscriptions.entry('daily-mail').subscribers.keys()
```

## 資料來源的引數值（資料來源動態值）

如果您從外部資料來源選取欄位，需要呼叫引數，右側會出現新索引標籤，供您指定此引數。 請參閱[此頁面](../expression/expressionadvanced.md)。

對於更複雜的使用案例，如果您想將資料來源的引數納入主要運算式中，可以使用關鍵字&#x200B;_params_&#x200B;來定義其值。 即使來自另一個包含另一個引數的資料來源，引數也可以是任何有效的運算式。

>[!NOTE]
>
>當您在運算式中定義引數值時，右側的標籤會消失。

使用下列語法：

```json
#{<datasource>.<field group>.fieldName, params: {<params-1-name>: <params-1-value>, <params-2-name>: <params-2-value>}}
```

* **`<params-1-name>`**：資料來源中第一個引數的確切名稱。
* **`<params-1-value>`**：第一個引數的值。 可以是任何有效的運算式。

範例：

```json
#{Weather.main.temperature, params: {localisation: @event{Profile.address.localisation}}}
#{Weather.main.temperature, params: {localisation: #{GPSLocalisation.main.coordinates, params: {city: @event{Profile.address.city}}}}}
```

+++ AI知識參考

本節包含結構化知識，用於支援與本主題相關的解譯、擷取和問答。

如需完整瞭解，此資訊應結合本頁的檔案。 兩者皆非獨立來源；頁面說明功能，本節提供額外內容，以協助去除術語、意圖、適用性和限制條件的歧義。

* **TL；DR：**&#x200B;此頁面說明如何在歷程運算式中參考事件欄位和資料來源欄位群組，包括預設值語法、對應存取函式(`entry`、`firstEntryKey`、`keys`)，以及以`params`關鍵字傳遞的內嵌資料來源引數。

**意圖：**

* 使用`@event{eventName.fieldPath}`語法在運算式中參考事件欄位
* 使用`#{dataSourceName.fieldGroupName.fieldPath}`語法參考資料來源欄位群組
* 將遞補預設值指派給欄位參考，讓運算式不會傳回null
* 使用`entry()`函式，從身分對應或訂閱對應擷取特定專案
* 使用`keys()`函式從對應欄位擷取所有金鑰
* 使用`params`關鍵字將引數值傳遞至內嵌的外部資料來源

**字彙表：**

* **欄位參考**：運算式語法，指向事件裝載或資料來源欄位群組&#x200B;*（產品特定）*&#x200B;中的具名欄位
* **defaultValue**：附加至欄位參考的可選遞補運算式，當欄位不存在或為Null *（產品特定）*&#x200B;時傳回
* **entry(key)**：對應函式，可擷取與指定索引鍵&#x200B;*（產品特定）*&#x200B;相關聯的集合專案
* **firstEntryKey()**：傳回對應欄位&#x200B;*（產品特定）*&#x200B;的第一個索引鍵的對應函式
* **keys()**：傳回對應欄位&#x200B;*（產品特定）*&#x200B;之所有索引鍵的對應函式
* **params關鍵字**：在主運算式&#x200B;*（產品特定）*&#x200B;中指定外部資料來源欄位之引數值的內嵌語法

**護欄：**

* 包含特殊字元的欄位名稱（以數字開頭、包含`-`或`a-z A-Z 0-9 _`以外的字元）必須用單引號或雙引號括住
* 預設值運算式必須傳回與欄位相同的資料型別 — 不相符的型別無效
* 使用`params`關鍵字定義內嵌引數值時，編輯器右側的個別引數標籤會消失
* 用作預設值的函式必須封裝在括弧中

**術語：**

* 正式名稱：欄位參考 — 縮寫：無 — 變體：欄位路徑，欄位運算式
* 同義字： `@event{...}` = &quot;event field reference&quot;； `#{...}` = &quot;data source field reference&quot;
* 請勿混淆：事件欄位（前置詞`@`）≠資料來源欄位（前置詞`#`）

**常見問題集：**

* **問：我如何參照名稱以數字開頭的欄位？**  — 以單引號或雙引號括住欄位名稱，例如`#{OpenWeather.weatherData.rain.'3h'}`。
* **問：事件承載中缺少參考欄位且未設定預設值時，會發生什麼情況？**  — 運算式傳回`null`。
* **問：如何使用函式來設定動態預設值？**  — 以括弧括住函式呼叫，例如`defaultValue: (now())`。
* **問：如何擷取儲存為訂閱者對應中第一個索引鍵的電子郵件地址？**  — 在訂閱者對應欄位上使用`firstEntryKey()`函式。
* **問：如何將引數傳遞至外部資料來源，而不使用右側索引標籤？**  — 使用`params`關鍵字內嵌： `#{DataSource.group.field, params: {paramName: value}}`。

+++
