---
title: 建立排名公式
description: 了解如何在Adobe Experience Platform中建立排名公式。
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 8bc808da-4796-4767-9433-71f1f2f0a432
source-git-commit: 58dffe64b1ca8a81728ae7043ec276917d3b9616
workflow-type: tm+mt
source-wordcount: '609'
ht-degree: 1%

---

# 建立排名公式 {#create-ranking-formulas}

## 關於排名公式 {#about-ranking-formulas}

**排名** 公式化可讓您定義規則，以決定應先針對指定版位顯示哪個優惠方案，而非考慮優惠方案的優先順序分數。

排名公式以&#x200B;**PQL語法**&#x200B;表示，並且可以利用配置檔案屬性、上下文資料和選件屬性。 有關如何使用PQL語法的詳細資訊，請參閱[專用文檔](https://experienceleague.adobe.com/docs/experience-platform/segmentation/pql/overview.html)。

建立排名公式後，您就可以將其指派至決策中的版位（先前稱為優惠方案活動）。 如需詳細資訊，請參閱[在決策](../offer-activities/configure-offer-selection.md)中設定選件選取項目。

## 建立排名公式 {#create-ranking-formula}

若要建立排名公式，請遵循下列步驟：

1. 訪問&#x200B;**[!UICONTROL Components]**&#x200B;菜單，然後選擇&#x200B;**[!UICONTROL Rankings]**&#x200B;頁簽。 將顯示先前建立的排名清單。

   ![](../../assets/rankings-list.png)

1. 按一下&#x200B;**[!UICONTROL Create ranking]**&#x200B;以建立新的排名公式。

   ![](../../assets/ranking-create-formula.png)

1. 指定排名公式名稱、說明和公式。

   在此範例中，如果實際天氣炎熱，我們想利用「hot」屬性提升所有選件的優先順序。 為此，已在決策呼叫中傳遞&#x200B;**contextData.weather=hot**。

   ![](../../assets/ranking-syntax.png)

1. 按一下「**[!UICONTROL Save]**」。排名公式已建立，您可以從清單中選取它以取得詳細資訊，並加以編輯或刪除。

   現在已可用於為版位排名合格優惠方案的決策（請參閱[在決策](../offer-activities/configure-offer-selection.md)中設定優惠方案選取項目）。

   ![](../../assets/ranking-formula-created.png)

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

根據決策呼叫中傳遞的內容資料，提升特定選件。 例如，如果在決策呼叫中傳遞`contextData.weather=hot`，則必須提升所有具有`attribute=hot`選件的優先順序。

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

如果我們有2個例項&#x200B;*CustomerAI*&#x200B;計算航空公司購買&#x200B;*travelInsurance*&#x200B;和&#x200B;*extraBargage*&#x200B;的傾向，如果客戶購買該產品的傾向分數高於90，下列排名公式將提高保險或行李特有優惠的優先順序（50分）。

不過，由於每個&#x200B;*CustomerAI*&#x200B;例項在統一的設定檔架構內建立其專屬物件，因此無法根據選件傾向類型來動態選取分數。 因此，您必須連結`if`陳述式，先檢查選件傾向類型，然後從適當的設定檔欄位擷取分數。

**排名公式：**

```
if ( offer.characteristics.propensityType = "extraBaggagePropensity" and _salesvelocity.CustomerAI.extraBaggagePropensity.score > 90, offer.rank.priority + 50,
    (
        if ( offer.characteristics.propensityType = "travelInsurancePropensity" and _salesvelocity.CustomerAI.insurancePropensity.score > 90, offer.rank.priority + 50, offer.rank.priority )
    )
)
```

更好的解決方案是將分數儲存在設定檔的陣列中。 下列範例僅使用簡單的排名公式，可涵蓋各種不同的傾向分數。 期望是您的設定檔結構會包含一連串的分數。 在此範例中，例項租用戶為&#x200B;*_salesvelocity* ，而設定檔架構包含下列項目：

![](../../assets/ranking-example-schema.png)

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

選件會包含&#x200B;*傾向類型*&#x200B;的屬性，該屬性符合分數中的類別：

![](../../assets/ranking-example-propensityType.png)

然後，您的排名公式可將每個選件的優先順序設定為等於該&#x200B;*傾向類型*&#x200B;的客戶&#x200B;*傾向分數*。 如果找不到分數，請使用選件上設定的靜態優先順序：

```
let score = (select _Individual_Scoring1 from _salesvelocity.individualScoring
             where _Individual_Scoring1.core.category.equals(offer.characteristics.propensityType, false)).head().core.propensityScore
in if(score.isNotNull(), score, offer.rank.priority)
```
