---
solution: Journey Optimizer
product: journey optimizer
title: 在您的協調行銷活動中使用測試活動
description: 了解如何使用測試活動
exl-id: edd70849-0a21-45f2-91f3-4774a0cad9dd
version: Campaign Orchestration
source-git-commit: b6b74e357029f4924f9699c05af3a0fcd7fcefd6
workflow-type: tm+mt
source-wordcount: '379'
ht-degree: 28%

---


# 測試 {#test}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_test"
>title="測試活動"
>abstract="「**測試**」活動是一種&#x200B;**流量控制**&#x200B;活動。您可以藉此根據指定條件啟用轉變。"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_test_conditions"
>title="條件"
>abstract="「**測試**」活動可以有多個輸出轉換。在協調式行銷活動執行期間，將循序測試每個條件，直到滿足其中一個條件。如果沒有滿足任何條件，協調式行銷活動就會沿著&#x200B;**[!UICONTROL 預設條件]**&#x200B;的路徑繼續進行。如果沒有啟用預設條件，協調式行銷活動就會到此停止。"

「**[!UICONTROL 測試]**」活動是一種&#x200B;**[!UICONTROL 流量控制]**&#x200B;活動。根據您定義的條件，透過啟用不同的轉變，使用它來分支您的行銷活動流程。 每個條件都可以評估入站轉變的資料，而且您可以選擇依評估條件的順序先執行哪個轉變。

## 設定測試活動 {#test-configuration}

若要設定&#x200B;**[!UICONTROL 測試]**&#x200B;活動：

1. 將&#x200B;**[!UICONTROL Test]**&#x200B;活動拖放至您的協調行銷活動畫布。

1. 依預設，活動會提供單一布林值測試：符合「True」條件時，就會啟用該轉變；否則，就會啟用「False」（預設）轉變。

   ![](../assets/test-1.png)

1. 完成下列欄位以定義轉變的條件：

   * **標籤**：轉變的名稱，讓您能在畫布上識別它。

   * **條件型別**：預設要評估母體計數的資料。

   * **運運算元**：要套用的比較，例如，等於、大於、小於。 運運算元清單取決於條件型別的資料型別。

   * **值**：用來比較條件型別的值。

   ![](../assets/test-2.png)

1. 若要在兩個以上的結果上分支，請按一下[新增條件] ****，並為每個額外的轉變定義標籤和條件。

1. 在執行階段，行銷活動會依序評估條件，並遵循符合的第一個條件。 若沒有符合的條件，執行將遵循&#x200B;**[!UICONTROL 預設條件]** （若已設定）；否則行銷活動會在&#x200B;**[!UICONTROL Test]**&#x200B;活動處停止。

## 範例 {#example}

在此範例中，會根據&#x200B;**[!UICONTROL 建置對象]**&#x200B;活動鎖定的設定檔數量啟動不同的轉變。 條件會依順序評估；最後一個轉變是預設值，且當沒有符合的先前條件時使用。

* 如果目標設定檔超過 10,000 個，則會傳送電子郵件訊息。
* 預設（不符合條件）：當計數為10,000或更少時，母體會導向至「不聯絡」轉變。

![](../assets/workflow-test-example.png)
