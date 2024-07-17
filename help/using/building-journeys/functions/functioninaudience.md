---
product: journey optimizer
title: inAudience
description: 瞭解inAudience中的函式
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inAudience，函式，運算式，歷程
exl-id: 8417af75-6e97-4ad4-86b4-3ecd264a5560
source-git-commit: d3f0adab52ed8e44a6097c5079396d1e9c06e0a7
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 6%

---

# inAudience {#inAudience}

檢查個人是否屬於指定對象。

>[!NOTE]
>
>您最多可以擷取100個對象。

對象名稱必須是字串常數。 它不能是欄位參考或運算式。

對象是在[Adobe Experience Platform](https://platform.adobe.com/audience/overview)中定義。 運算式編輯器提供自動完成的對象清單。

對象可以有三種狀態：

* 現有：實體會繼續存在於對象中。
* 已實現：實體正在進入對象。
* 已退出：實體正在退出對象。

只有具有&#x200B;**已實現**&#x200B;和&#x200B;**現有**&#x200B;對象參與狀態的個人，才會被視為對象的成員。 如需如何評估對象的詳細資訊，請參閱[Segmentation Service檔案](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html#interpret-segment-results)。

`inAudience('audienceName') == true`表示您擁有segmentMembership且狀態為entered/existing。

`inAudience('audienceName') == false`表示您擁有退出狀態的segmentMembership。

## 類別

Adobe Experience Platform

## 函式語法

`inAudience(<parameter>)`

## 參數

| 參數 | 說明 | 類型 |
|--- |--- |--- |
| 對象 | 對象名稱 | `<string>` |

## 簽章與傳回的型別

`inAudience(<string>)`

傳回布林值。

## 範例

`inAudience("men over 50")`

說明：

如果歷程執行個體中的個人是名為「超過50歲的男性」的Adobe Experience Platform對象的一部分，則函式會傳回&#x200B;**[!UICONTROL true]**，否則會傳回&#x200B;**[!UICONTROL false]**。
