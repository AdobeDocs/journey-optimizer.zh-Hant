---
title: 排名公式
description: 瞭解如何建立公式以對優惠進行排序
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 8bc808da-4796-4767-9433-71f1f2f0a432
source-git-commit: a67cabc2078debb981ee17fae9202f9fd80ec977
workflow-type: tm+mt
source-wordcount: '472'
ht-degree: 1%

---

# 排名公式 {#create-ranking-formulas}

## 關於排名公式 {#about-ranking-formulas}

**排序公式** 允許您定義規則，以確定在給定的職位安排中應首先提供哪個職位，而不是考慮聘用的優先順序分數。

排名公式在中表示 **PQL語法** 並可利用配置檔案屬性、上下文資料和提供屬性。 有關如何使用PQL語法的詳細資訊，請參閱 [專用文檔](https://experienceleague.adobe.com/docs/experience-platform/segmentation/pql/overview.html)。

一旦建立了排名公式，您就可以將其分配給決策中的位置。 有關此的詳細資訊，請參閱 [在決策中配置服務選擇](../offer-activities/configure-offer-selection.md)。

## 建立排名公式 {#create-ranking-formula}

要建立排名公式，請執行以下步驟：

1. 訪問 **[!UICONTROL Components]** ，然後選擇 **[!UICONTROL Rankings]** 頁籤。 顯示先前建立的排名清單。

   ![](../assets/rankings-list.png)

1. 按一下 **[!UICONTROL Create ranking]** 的子菜單。

   ![](../assets/ranking-create-formula.png)

1. 指定排名公式名稱、說明和公式。

   在本示例中，如果實際天氣炎熱，我們希望提高所有優先服務的優先順序，並使用「hot」屬性。 為此， **contextData.weather=hot** 在決定呼叫中通過。

   ![](../assets/ranking-syntax.png)

1. 按一下「**[!UICONTROL Save]**」。您的排名公式已建立，您可以從清單中選擇它以獲取詳細資訊，並編輯或刪除它。

   現在，它已準備好用於對合格的職位安排報價進行排序的決定(請參閱 [在決策中配置服務選擇](../offer-activities/configure-offer-selection.md))。

   ![](../assets/ranking-formula-created.png)

## 排序公式示例 {#ranking-formula-examples}

您可以根據需要建立許多不同的排名公式。 下面是一些例子。

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

### 基於配置檔案屬性的具有特定提供屬性的Boost優惠

如果個人資料位於與報價相對應的城市，那麼該城市所有報價的優先順序將增加一倍。

**排名公式：**

```
if( offer.characteristics.city = homeAddress.city, offer.rank.priority * 2, offer.rank.priority)
```

### Boost提供，其結束日期從現在起不到24小時

**排名公式：**

```
if( offer.selectionConstraint.endDate occurs <= 24 hours after now, offer.rank.priority * 3, offer.rank.priority)
```

### 基於上下文資料的具有特定提供屬性的提供

根據在決策調用中傳遞的上下文資料提高某些優惠。 例如，如果 `contextData.weather=hot` 在決策呼叫中傳遞，所有優惠的優先順序 `attribute=hot` 必須加強。

**排名公式：**

```
if (@{_xdm.context.additionalParameters;version=1}.weather.isNotNull()
and offer.characteristics.weather=@{_xdm.context.additionalParameters;version=1}.weather, offer.rank.priority + 5, offer.rank.priority)
```

請注意，使用決策API時，上下文資料將添加到請求正文中的配置檔案元素中，如下例所示。

**來自請求正文的代碼段：**

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

### 基於客戶購買所提供產品傾向的提高報價

您可以根據客戶傾向得分提高優惠得分。

在此示例中，實例租戶為 *銷售速度* 配置檔案架構包含儲存在陣列中的分數範圍：

![](../assets/ranking-example-schema.png)

因此，對於配置檔案，例如：

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

報價將包含 *傾向類型* 與分數中的類別匹配：

![](../assets/ranking-example-propensityType.png)

然後，您的排名公式可以將每項服務的優先順序設定為等於客戶 *傾向分數* 因為 *傾向類型*。 如果找不到分數，請使用優惠上設定的靜態優先順序：

```
let score = (select _Individual_Scoring1 from _salesvelocity.individualScoring
             where _Individual_Scoring1.core.category.equals(offer.characteristics.propensityType, false)).head().core.propensityScore
in if(score.isNotNull(), score, offer.rank.priority)
```
