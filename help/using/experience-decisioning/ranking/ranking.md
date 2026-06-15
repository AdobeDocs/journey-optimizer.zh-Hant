---
title: 排名方法
description: 瞭解如何使用排名方法
feature: Decisioning, Ranking
topic: Integrations
role: User
level: Intermediate
exl-id: c1d69bc9-4486-4037-b218-f4f704b2ba9c
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/1qUj05fLaRqqJGfaoL-y5uwtknp7HDkWKocHMde-8lc
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
subfeature_v2:
  - id: a7a194a0-75e2-4913-8a83-14714fbf68e6
  - id: eb547372-2a95-4d13-b0fd-f720c9895880
source-git-commit: ee394c77b226dd35a9c27f4a02e3b8d7a997ccbd
workflow-type: tm+mt
source-wordcount: 237
ht-degree: 14%

---

# 排名方法 {#rankings}

>[!BEGINSHADEBOX]

**在此頁面上：**&#x200B;建立排名方法（公式或AI模型），並將其指派給選取策略，讓決策引擎知道哪些符合資格的專案會先出現在每個設定檔中。

>[!ENDSHADEBOX]

排名方法可讓您針對要針對指定設定檔顯示的專案進行排名。 建立排名方法後，您可以將其指派給選擇策略以定義應先選取哪些項目。

有兩種排名方法可供使用：

* **公式**&#x200B;可讓您定義規則，以決定應該先顯示哪個專案，而不是考慮專案的優先順序分數。

* **AI模型**&#x200B;可讓您使用經過訓練的模型系統，這些系統將利用多個資料點來決定應該先顯示哪個專案。

## 建立排名方法 {#create}

若要建立排名方法，請依照下列步驟進行：

1. 導覽至&#x200B;**[!UICONTROL 策略設定]**&#x200B;功能表，然後依您要使用的排名型別選取&#x200B;**[!UICONTROL 公式]**&#x200B;或&#x200B;**[!UICONTROL AI模型]**&#x200B;功能表。

   ![](../assets/ranking-create.png)

1. 按一下畫面右上角的&#x200B;**[!UICONTROL 建立公式]**&#x200B;或&#x200B;**[!UICONTROL 建立AI模型]**&#x200B;按鈕。

   以下章節提供了有關如何建立排名公式和AI模型的詳細資訊：

   * [排名公式](ranking-formulas.md)
   * [AI 模型](ai-models.md)

1. 設定公式或AI模型以符合您的需求，然後儲存。

您的排名方法現在已準備好用於[選取策略](../selection-strategies.md)，以排名符合資格的決策專案。


