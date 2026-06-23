---
solution: Journey Optimizer
product: journey optimizer
title: 條件式指令(if， then， else)
description: 瞭解條件式指令
feature: Journeys
role: Developer
level: Experienced
keywords: 進階，條件，動作，歷程
exl-id: 5a5b35a7-e3b5-4dc0-8a87-e985956b04a4
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/SObpEvgu0D-pcoLVaKM7iRffLTSP1stp1zcg4Ygs-vQ
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: cce82f05-fc3c-4af7-85ff-8bba603861a7
  - id: d8353d85-5da7-453d-bd68-40ad33fa0ab7
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 576
ht-degree: 0%

---

# 條件式指令(if， then， else) {#conditional-instruction}

進階編輯器支援條件式指令(if， then， else)。 它可讓您定義更複雜的運算式。 它由下列元素組成：

* **[!UICONTROL if]**：先評估條件。
* **[!UICONTROL then]**：條件評估結果為true時要評估的運算式。
* **[!UICONTROL else]**：條件評估結果為false時要評估的運算式。

>[!NOTE]
>
>所有運算式都必須加上括弧。

```json
if  (<expression1>)
then
   (<expression2>)
else
   (<expression3>)
```

`<expression1>`必須傳回&#x200B;**布林值**。

`<expression2>`和`<expression3>`必須具有相同的型別或相容的型別。 支援的簽章和傳回的型別包括：

```json
boolean,boolean : boolean
dateTime,dateTime : dateTime
dateTimeOnly,dateTimeOnly : dateTimeOnly
decimal,integer : decimal
integer,decimal : integer
integer,decimal : decimal
duration,duration : duration
string,string : string
listBoolean,listBoolean : listBoolean
listDateTime,listDateTime : listDateTime
listDateTimeOnly,listDateTimeOnly : listDateTimeOnly
listDateOnly,listDateOnly : listDateOnly
listDecimal,listDecimal : listDecimal
listInteger,listInteger : listInteger
listString,listString : listString
```

**使用狀況**

條件式指示可讓您透過減少條件活動的數量，將歷程工作流程最佳化。 例如，在相同動作活動中，您僅能使用一個條件運算式，即可為欄位定義指定兩個替代方案。

動作活動的範例（適用於預期字串為條件指令結果的欄位）：

```json
if (startWithIgnoreCase(@event{eventiOSPushPermissionAllowed.device.model}, 'iPad') or startWithIgnoreCase(@event{eventiOSPushPermissionAllowed.device.model}, 'iOS'))
then
   ('apns')
else
   ('fcm')
```

+++ AI知識參考

本節包含結構化知識，用於支援與本主題相關的解譯、擷取和問答。

如需完整瞭解，此資訊應結合本頁的檔案。 兩者皆非獨立來源；頁面說明功能，本節提供額外內容，以協助去除術語、意圖、適用性和限制條件的歧義。

* **TL；DR：**&#x200B;此頁面說明Journey進階運算式編輯器中可用的`if / then / else`條件式指令，包括語法規則、支援的型別組合，以及實際使用範例。

**意圖：**

* 使用`if`、`then`和`else`寫入條件運算式，以根據布林條件傳回不同的值
* 將內嵌條件式邏輯內嵌在單一動作活動中，以減少歷程中的條件式活動數
* 決定哪些資料型別組合對`then`和`else`分支有效
* 根據裝置型號，套用條件式指示以將推播通知權杖路由至APNS或FCM

**字彙表：**

* **條件式指令**：進階編輯器中的`if / then / else`運算式建構，會評估布林值並傳回兩個運算式之一&#x200B;*（產品特定）*
* **進階運算式編輯器**：用於寫入條件、等待活動及動作引數對應&#x200B;*（產品特定）*&#x200B;中使用的複雜運算式的Journey Optimizer介面

**護欄：**

* 在`if`、`then`和`else`子句中的所有運算式都必須加上括弧
* `if`子句(`<expression1>`)必須傳回布林型別
* `then`和`else`運算式（`<expression2>`和`<expression3>`）必須有相同型別或相容型別（例如`decimal`和`integer`相容，`string`和`integer`不相容）
* 並非所有型別組合都受支援 — 只有支援的簽名表格中所列的配對才有效

**術語：**

* 正式名稱：條件式指令 — 縮寫：none — 變體：if/then/else，三元樣式條件
* 同義字：&quot;conditional instruction&quot; = &quot;inline condition&quot; = &quot;if-then-else expression&quot;
* 請勿混淆：條件式指令（內嵌運算式）≠條件活動（歷程畫布節點）

**常見問題集：**

* **問： `if`子句是否需要以括弧括住？**  — 是，所有運算式都必須加上括弧，包括`if`子句中的條件。
* **問：我可以使用`if / then / else`傳回一個分支的數字，以及另一個分支的字串嗎？**  — 否；`<expression2>`和`<expression3>`必須有相同或相容的型別。
* **問：條件式指令如何降低歷程複雜度？**  — 它可讓您使用單一運算式，在單一動作活動中指定兩個欄位值替代專案，以避免在畫布上出現個別的「條件」活動節點。
* **問：如果兩個分支都是字串，則條件式指令會傳回什麼型別？**  — 它會傳回`string`。
* **問：`if / then / else`是否可用來選取推播通知頻道？**  — 是；例如，評估裝置模型以傳回Apple裝置的`'apns'`或其他裝置的`'fcm'`。

+++
