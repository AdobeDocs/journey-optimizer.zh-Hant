---
title: 排名公式
description: 了解如何建立公式來排名選件
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 8bc808da-4796-4767-9433-71f1f2f0a432
source-git-commit: a67cabc2078debb981ee17fae9202f9fd80ec977
workflow-type: tm+mt
source-wordcount: '477'
ht-degree: 1%

---

# 排名公式 {#create-ranking-formulas}

## 關於排名公式 {#about-ranking-formulas}

**排名公式** 可讓您定義規則，以決定應先針對指定版位呈現哪個優惠方案，而非考慮優惠方案的優先順序分數。

排名公式以表示 **PQL語法** 並可運用設定檔屬性、內容資料和選件屬性。 有關如何使用PQL語法的詳細資訊，請參閱 [專屬檔案](https://experienceleague.adobe.com/docs/experience-platform/segmentation/pql/overview.html).

建立排名公式後，您可以將其指派給決策中的版位。 有關詳細資訊，請參閱 [在決策中設定選件選取項目](../offer-activities/configure-offer-selection.md).

## 建立排名公式 {#create-ranking-formula}

若要建立排名公式，請遵循下列步驟：

1. 存取 **[!UICONTROL 元件]** ，然後選取 **[!UICONTROL 排名]** 標籤。 將顯示先前建立的排名清單。

   ![](../assets/rankings-list.png)

1. 按一下 **[!UICONTROL 建立排名]** 來建立新排名公式。

   ![](../assets/ranking-create-formula.png)

1. 指定排名公式名稱、說明和公式。

   在此範例中，如果實際天氣炎熱，我們想利用「hot」屬性提升所有選件的優先順序。 若要這麼做， **contextData.weather=hot** 在決策呼叫中傳遞。

   ![](../assets/ranking-syntax.png)

1. 按一下&#x200B;**[!UICONTROL 「儲存」]**。排名公式已建立，您可以從清單中選取它以取得詳細資訊，並加以編輯或刪除。

   現在已可用於決定對符合資格的優惠方案排名以刊登版位(請參閱 [在決策中設定選件選取項目](../offer-activities/configure-offer-selection.md))。

   ![](../assets/ranking-formula-created.png)

## 排名公式範例 {#ranking-formula-examples}

您可以根據自己的需求建立許多不同的排名公式。 以下是一些範例。

<!--
Boost by offer ID

Boost the priority of an offer with the offer ID *xcore:personalized-offer:13d213cd4cb328ec* by 5.

**Ranking formula:**

```
if( offer._id = "xcore:personalized-offer:13d213cd4cb328ec", offer.rank.priority + 5, offer.rank.priority)
```

Change the offer priority based on a certain profile attribute

Set the offer priority to 30 for offer *xcore:personalized-offer:13d213cd4cb328ec* if the user lives in the city of Bondi.

**Ranking formula:**

```
if( offer._id = "xcore:personalized-offer:13d213cd4cb328ec" and homeAddress.city.equals("Bondi", false), 30, offer.rank.priority)
```

Boost multiple offers by offer ID based on the presence of a profile's segment membership

Boost the priority of offers based on whether the user is a member of a priority segment, which is configured as an attribute in the offer.

**Ranking formula:**

```
if( segmentMembership.get("ups").get(offer.characteristics.prioritySegmentId).status in (["realized","existing"]), offer.rank.priority + 10, offer.rank.priority)
```
-->

### 根據設定檔屬性，以特定選件屬性提升選件

如果設定檔位於與優惠方案相對應的城市，則該城市中所有優惠方案的優先順序會加倍。

**排名公式：**

```
if( offer.characteristics.city = homeAddress.city, offer.rank.priority * 2, offer.rank.priority)
```

### 結束日期現在後不到24小時時，提升選件

**排名公式：**

```
if( offer.selectionConstraint.endDate occurs <= 24 hours after now, offer.rank.priority * 3, offer.rank.priority)
```

### 根據內容資料，以特定選件屬性提升選件

根據決策呼叫中傳遞的內容資料，提升特定選件。 例如，若 `contextData.weather=hot` 會在決策呼叫中傳遞，且優先順序會與 `attribute=hot` 必須得到提振。

**排名公式：**

```
if (@{_xdm.context.additionalParameters;version=1}.weather.isNotNull()
and offer.characteristics.weather=@{_xdm.context.additionalParameters;version=1}.weather, offer.rank.priority + 5, offer.rank.priority)
```

請注意，使用決策API時，內容資料會新增至請求內文中的設定檔元素，如以下範例中。

**請求內文的程式碼片段：**

```
"xdm:profiles": [
{
    "xdm:identityMap": {
        "crmid": [
            {
            "xdm:id": "CRMID1"
            }
        ]
    },
    "xdm:contextData": [
        {
            "@type":"_xdm.context.additionalParameters;version=1",
            "xdm:data":{
                "xdm:weather":"hot"
            }
        }
    ]
 }],
```

### 根據客戶購買所提供產品的傾向，提升優惠方案

您可以根據客戶傾向分數來提升優惠方案的分數。

在此範例中，例項租用戶為 *_salesvelocity* 且設定檔架構包含儲存在陣列中的分數範圍：

![](../assets/ranking-example-schema.png)

有鑑於此，針對下列設定檔：

```
{"_salesvelocity": {"individualScoring": [
                    {"core": {
                            "category":"insurance",
                            "propensityScore": 96.9
                        }},
                    {"core": {
                            "category":"personalLoan",
                            "propensityScore": 45.3
                        }},
                    {"core": {
                            "category":"creditCard",
                            "propensityScore": 78.1
                        }}
                    ]}
}
```

選件會包含 *傾向類型* 會比對分數中的類別：

![](../assets/ranking-example-propensityType.png)

然後，您的排名公式可以設定每個優惠方案的優先順序，使其等於客戶 *傾向分數* 對於 *傾向類型*. 如果找不到分數，請使用選件上設定的靜態優先順序：

```
let score = (select _Individual_Scoring1 from _salesvelocity.individualScoring
             where _Individual_Scoring1.core.category.equals(offer.characteristics.propensityType, false)).head().core.propensityScore
in if(score.isNotNull(), score, offer.rank.priority)
```
