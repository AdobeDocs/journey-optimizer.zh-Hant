---
solution: Journey Optimizer
product: journey optimizer
title: 使用儲存對象活動
description: 瞭解如何在協調的行銷活動中使用分叉活動
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 84e34d21-dca1-4203-8539-f2b20e461936
source-git-commit: bdc584c1aae0c735d81dfc95e11f96f755bea26a
workflow-type: tm+mt
source-wordcount: '452'
ht-degree: 10%

---

# 儲存客群 {#save-audience}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_save_audience"
>title="儲存一個對象"
>abstract="使用此活動來更新現有的對象，或是從協調行銷活動中的母體運算上游建立新的對象。 建立的對象將新增至對象清單中，並可透過「**對象**」選單使用。"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_saveaudience_outbound"
>title="產生傳出轉變"
>abstract="如果您想在「**儲存對象**」活動之後新增轉變，請使用此選項。"

**儲存對象**&#x200B;活動是&#x200B;**鎖定目標**&#x200B;活動。 此活動可讓您更新現有的對象，或是從協調行銷活動中的母體運算上游建立新的對象。 建立的對象會新增至應用程式對象清單，並可透過&#x200B;**對象**&#x200B;功能表使用。

此活動主要用於將母體族群轉換為可重複使用的對象，讓母體族群可繼續在相同的協調行銷活動中運算。 將其連線到其他目標定位活動，例如&#x200B;**建立對象**&#x200B;或&#x200B;**合併**&#x200B;活動。

## 設定「儲存對象」活動{#save-audience-configuration}

請依照下列步驟設定&#x200B;**儲存對象**&#x200B;活動：

![](../assets/workflow-save-audience.png)

1. 新增&#x200B;**儲存對象**&#x200B;活動至您協調的行銷活動。

1. 在&#x200B;**模式**&#x200B;下拉式清單中，選取您要執行的動作：

   * **建立或更新現有的對象**：定義&#x200B;**對象標籤**。 如果對象已存在，則會更新，否則將建立新對象。

   * **更新現有的對象**：從現有的對象清單中選擇要更新的&#x200B;**對象**。

1. 選取將套用至現有對象的&#x200B;**更新模式**：

   * **以新資料取代對象內容**：已取代所有對象內容。 遺失舊資料。僅保留儲存對象活動之入站轉變的資料。 此選項會清除更新對象的對象型別和目標定位維度。

   * **使用新資料完成對象**：保留舊的對象內容，並將儲存對象活動入站轉變的資料新增到其中。

1. 如果要在&#x200B;**儲存對象**&#x200B;活動後新增轉變，請核取&#x200B;**產生出站轉變**&#x200B;選項。

之後儲存的對象內容便可在對象的詳細資料檢視中使用，您可從&#x200B;**對象**&#x200B;功能表存取該內容。 此檢視中可用的欄會與協調行銷活動的&#x200B;**儲存對象**&#x200B;活動之入站轉變的欄相對應。


## 範例{#save-audience-example}

以下範例說明如何從目標定位進行簡單的對象更新。 會新增排程器，以每月執行一次協調的行銷活動。 查詢會復原訂閱到不同可用應用程式的所有設定檔。 **儲存對象**&#x200B;活動會刪除自上次協調行銷活動執行以來從服務取消訂閱的設定檔，並新增新訂閱的設定檔，以更新對象。
