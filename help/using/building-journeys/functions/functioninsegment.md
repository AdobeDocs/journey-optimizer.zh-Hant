---
product: journey optimizer
title: inSegment
description: 瞭解中的函式
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inSegment，函式，運算式，歷程
exl-id: 8417af75-6e97-4ad4-86b4-3ecd264a5560
version: Journey Orchestration
source-git-commit: 62783c5731a8b78a8171fdadb1da8a680d249efd
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 6%

---

# inSegment {#inSegment}

檢查個人是否屬於指定對象。

>[!NOTE]
>
>您最多可以擷取100個對象。

對象名稱必須是字串常數。 它不能是欄位參考或運算式。

對象是在[Adobe Experience Platform](https://platform.adobe.com/audience/overview)中定義。 運算式編輯器提供自動完成的對象清單。

對象可以有兩種狀態：

* 已實現：實體符合區段定義的資格。
* 已退出：實體正在退出區段定義。

只有具有&#x200B;**已實現**&#x200B;對象參與狀態的個人才會被視為對象的成員。 如需如何評估對象的詳細資訊，請參閱[Segmentation Service檔案](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html#interpret-segment-results)。

`IF inSegment('segmentName') == true`表示您擁有segmentMembership且狀態為entered/existing。

`ELSE inSegment('segmentName') == false`表示您擁有退出狀態的segmentMembership。

## 類別

Adobe Experience Platform

## 函式語法

`inSegment(<parameter>)`

## 參數

| 參數 | 說明 | 類型 |
|--- |--- |--- |
| 區段 | 對象名稱 | `<string>` |

## 簽章與傳回的型別

`inSegment(<string>)`

傳回布林值。

## 範例

`inSegment("men over 50")`

說明：

如果歷程執行個體中的個人是名為「超過50歲的男性」的Adobe Experience Platform對象的一部分，則函式會傳回&#x200B;**[!UICONTROL true]**，否則會傳回&#x200B;**[!UICONTROL false]**。
