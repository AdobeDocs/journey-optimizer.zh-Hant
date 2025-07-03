---
solution: Journey Optimizer
product: journey optimizer
title: 使用調解活動
description: 瞭解如何在協調的行銷活動中使用調解活動
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 0d5cfffe-bc6c-40bc-b3e1-5b44368ac76f
source-git-commit: 8a5026cdeb63b7b261ec0dfa690c5bd41d7de772
workflow-type: tm+mt
source-wordcount: '627'
ht-degree: 32%

---

# 調和 {#reconciliation}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation"
>title="調和活動"
>abstract="「**調和**」活動是&#x200B;**目標定位**&#x200B;活動，可讓您定義 Adobe Journey Optimizer 和工作表資料之間的連結。"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_field"
>title="調和選取欄位"
>abstract="調和選取欄位"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_condition"
>title="調和建立條件"
>abstract="調和建立條件"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_complement"
>title="調和產生補集"
>abstract="調和產生補集"


+++ 目錄

| 歡迎使用協調的行銷活動 | 首次建立協調的行銷活動 | 查詢資料庫 | 協調的行銷活動 |
|---|---|---|---|
| [開始使用協調的行銷活動](../gs-orchestrated-campaigns.md)<br/><br/>[設定步驟](../configuration-steps.md)<br/><br/>[存取和管理協調的行銷活動](../access-manage-orchestrated-campaigns.md) | [建立協調行銷活動的關鍵步驟](../gs-campaign-creation.md)<br/><br/>[建立並排程行銷活動](../create-orchestrated-campaign.md)<br/><br/>[協調活動](../orchestrate-activities.md)<br/><br/>[開始並監視行銷活動](../start-monitor-campaigns.md)<br/><br/>[報告](../reporting-campaigns.md) | [使用規則產生器](../orchestrated-rule-builder.md)<br/><br/>[建立您的第一個查詢](../build-query.md)<br/><br/>[編輯運算式](../edit-expressions.md)<br/><br/>[重新鎖定目標](../retarget.md) | [開始使用活動](about-activities.md)<br/><br/>活動：<br/>[並加入](and-join.md) - [建立對象](build-audience.md) - [變更維度](change-dimension.md) - [頻道活動](channels.md) - [合併](combine.md) - [重複資料刪除](deduplication.md) - [擴充](enrichment.md) - [分支](fork.md) - <b>[調解](reconciliation.md)</b> - [儲存對象](save-audience.md) - [分割](split.md) - [等待](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

**[!UICONTROL 調解]**&#x200B;活動是&#x200B;**[!UICONTROL 鎖定目標]**&#x200B;活動，可讓您定義Adobe Journey Optimizer中的資料與工作表中的資料之間的連結，例如從外部檔案載入的資料。

**[!UICONTROL 擴充]**&#x200B;活動可讓您新增其他資料至您的協調行銷活動，例如，合併來自多個來源的資料或連結至暫時資源。 相對地，**[!UICONTROL 調解]**&#x200B;活動用來比對未識別或外部資料與資料庫中現有的資源。

**[!UICONTROL 調解]**&#x200B;要求系統中已存在相關記錄。 例如，如果您匯入列有產品、時間戳記和客戶資訊的購買檔案，產品和客戶必須已存在於資料庫中才能建立連結。

## 設定調和活動 {#reconciliation-configuration}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_targeting"
>title="目標市場選擇維度"
>abstract="選取新的目標市場選擇維度。維度可讓您定義目標群體：收件者、應用程式訂閱者、操作者、訂閱者等。預設會選取目前的目標市場選擇維度。"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_rules"
>title="調和規則"
>abstract="選取用於重複資料刪除的調和規則。若要使用屬性，請選取&#x200B;**簡單屬性**&#x200B;選項，然後選擇來源欄位和目的地欄位。若要使用查詢建模工具建立您自己的調和條件，請選取&#x200B;**進階調和條件**&#x200B;選項。"
>additional-url="https://experienceleague.adobe.com/zh-hant/docs/campaign-web/v8/query-database/query-modeler-overview" text="使用查詢建模工具"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_targeting_selection"
>title="選取目標市場選擇維度"
>abstract="選取要調和之輸入資料的目標市場選擇維度。"
>additional-url="https://experienceleague.adobe.com/docs/campaign-web/v8/audiences/gs-audiences-recipients.html?#targeting-dimensions" text="目標市場選擇維度"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_keep_unreconciled_data"
>title="保留未調和的資料"
>abstract="依預設，未調和的資料保留在傳出轉變中，並可在工作表中供未來使用。若要移除未調和的資料，請停用「**保留未調和的資料**」選項。"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_attribute"
>title="調和屬性"
>abstract="選取用於調和資料的屬性，然後按一下「確認」。"

請依照下列步驟設定&#x200B;**[!UICONTROL 調解]**&#x200B;活動：

1. 將&#x200B;**[!UICONTROL 調解]**&#x200B;活動新增至工作流程。

1. 選擇新的目標維度，以定義您要鎖定的對象，例如收件者或訂閱者。

1. 設定欄位以用於將傳入資料與現有設定檔進行比對。

1. 若要使用基本欄位比對資料，請選取&#x200B;**[!UICONTROL 簡單屬性]**。

1. 設定比對欄位：

   * **[!UICONTROL Source]**：列出傳入的資料欄位。

   * **[!UICONTROL 目的地]**：參考所選目標維度中的欄位。

   當兩個值相等時，就會發生相符專案，例如，以&#x200B;**[!UICONTROL 電子郵件]**&#x200B;相符來識別設定檔。

   ![](../assets/workflow-reconciliation-criteria.png)

1. 若要新增更多相符規則，請按一下[新增規則]。**&#x200B;** 必須符合所有條件，才會發生比對。

1. 如需更複雜的條件，請選擇&#x200B;**[!UICONTROL 進階調解條件]**。 使用[查詢模型工具](../orchestrated-rule-builder.md)來定義自訂邏輯。

1. 若要篩選要調解的資料，請按一下&#x200B;**[!UICONTROL 建立篩選器]**，並在查詢模型工具中定義條件。

1. 依預設，不相符的記錄會保留在出站轉變中，並儲存在工作表中。 若要移除這些專案，請啟用&#x200B;**[!UICONTROL 保留未調解的資料]**&#x200B;選項。

## 範例 {#example-reconciliation}

此範例使用Adobe Journey Optimizer中的&#x200B;**[!UICONTROL 調解]**&#x200B;活動，以確保只傳送電子郵件給可識別的客戶。 資料會透過&#x200B;**[!UICONTROL 讀取對象]**&#x200B;活動傳入，該活動會鎖定具有先前訂單的使用者。 然後&#x200B;**[!UICONTROL 調解]**&#x200B;活動會使用電子郵件欄位，將此傳入資料與資料庫中的現有設定檔比對。

![](../assets/workflow-reconciliation-sample-1.0.png)
