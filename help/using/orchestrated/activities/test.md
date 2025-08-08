---
solution: Journey Optimizer
product: journey optimizer
title: 在您的協調行銷活動中使用測試活動
description: 了解如何使用測試活動
exl-id: edd70849-0a21-45f2-91f3-4774a0cad9dd
source-git-commit: 3a44111345c1627610a6b026d7b19b281c4538d3
workflow-type: tm+mt
source-wordcount: '375'
ht-degree: 83%

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

「**[!UICONTROL 測試]**」活動是一種&#x200B;**[!UICONTROL 流量控制]**&#x200B;活動。您可以藉此根據指定條件啟用轉變。

## 設定測試活動 {#test-configuration}

請按照以下步驟設定&#x200B;**[!UICONTROL 測試]**&#x200B;活動：

1. 將&#x200B;**[!UICONTROL 測試]**&#x200B;活動新增至您的協調行銷活動。

1. 預設情況下，**[!UICONTROL 測試]**&#x200B;活動會呈現簡單的布林值測試。如果符合「真」轉變中定義的條件，則會啟動此轉變。否則，將會啟用預設的「假」轉變。

1. 若要設定與轉變關聯的條件，請按一下「**[!UICONTROL 開啟個人化對話方塊]**」圖示。使用運算式編輯器來定義啟動此轉變所需的規則。您也可以善用事件變數、條件和日期/時間函式。

   此外，您可以修改&#x200B;**[!UICONTROL 標籤]**&#x200B;欄位，在「已協調的行銷活動」畫布上個人化轉變名稱。

   ![](../assets/workflow-test-default.png)

1. 您可以將多個輸出轉變新增到&#x200B;**[!UICONTROL 測試]**&#x200B;活動。若要這麼做，請按一下「**[!UICONTROL 新增條件]**」按鈕，並為每個轉變設定標籤和相關聯的條件。
v
1. 在協調式行銷活動執行期間，將循序測試每個條件，直到滿足其中一個條件。如果未符合任何條件，協調的行銷活動會沿著&#x200B;**[!UICONTROL 預設條件]**&#x200B;的路徑繼續。 如果未啟用預設條件，則行銷活動會在此點停止。

## 範例 {#example}

在此範例中，會根據&#x200B;**[!UICONTROL 建立客群]**&#x200B;活動定為目標的設定檔數量啟動不同的轉變：

* 如果目標設定檔超過 10,000 個，則會傳送電子郵件訊息。
* 若為 1,000 至 10,000 個設定檔，則會傳送簡訊。
* 如果目標設定檔低於 1,000 個，則會導向至「請勿聯絡」轉變。

![](../assets/workflow-test-example.png)

為此，已在「電子郵件」和「簡訊」條件中運用 `vars.recCount` 事件變數，以計算目標設定檔的數量並啟用適當的轉變。

![](../assets/workflow-test-example-config.png)
