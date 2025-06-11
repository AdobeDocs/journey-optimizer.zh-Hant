---
solution: Journey Optimizer
product: journey optimizer
title: 使用調解活動
description: 瞭解如何在協調的行銷活動中使用調解活動
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 0d5cfffe-bc6c-40bc-b3e1-5b44368ac76f
source-git-commit: d59643f18a335fe1e094156a1cfee65b717b9fce
workflow-type: tm+mt
source-wordcount: '621'
ht-degree: 34%

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

| 歡迎使用協調的行銷活動 | 啟動您的第一個協調行銷活動 | 查詢資料庫 | 協調的行銷活動活動 |
|---|---|---|---|
| [開始使用協調的行銷活動](../gs-orchestrated-campaigns.md)<br/><br/>[設定步驟](../configuration-steps.md)<br/><br/>[建立協調行銷活動的重要步驟](../gs-campaign-creation.md) | [建立協調的行銷活動](../create-orchestrated-campaign.md)<br/><br/>[協調活動](../orchestrate-activities.md)<br/><br/>[使用協調的行銷活動傳送訊息](../send-messages.md)<br/><br/>[開始並監視行銷活動](../start-monitor-campaigns.md)<br/><br/>[報告](../reporting-campaigns.md) | [使用查詢Modeler](../orchestrated-rule-builder.md)<br/><br/>[建置您的第一個查詢](../build-query.md)<br/><br/>[編輯運算式](../edit-expressions.md) | [開始使用活動](about-activities.md)<br/><br/>活動：<br/>[並加入](and-join.md) - [建置對象](build-audience.md) - [變更維度](change-dimension.md) - [合併](combine.md) - [重複資料刪除](deduplication.md) - [擴充](enrichment.md) - [分支](fork.md) - [調解](reconciliation.md) - [分割](split.md) - [等待](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

**調解**&#x200B;活動是&#x200B;**鎖定目標**&#x200B;活動，可讓您定義Adobe Journey Optimizer中的資料與工作表中的資料之間的連結，例如從外部檔案載入的資料。

擴充活動可讓您將其他資料新增至您的協調行銷活動，例如，合併來自多個來源的資料或連結至暫時資源。 相對地，調解活動用於比對未識別或外部資料與資料庫中的現有資源。

調解需要系統中已存在相關記錄。 例如，如果您匯入列有產品、時間戳記和客戶資訊的購買檔案，產品和客戶必須已存在於資料庫中才能建立連結。

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

請依照下列步驟設定&#x200B;**調解**&#x200B;活動：

1. 將&#x200B;**調解**&#x200B;活動新增至您協調的行銷活動。

1. 選取新的目標市場選擇維度。維度可讓您定義目標母體：收件者、應用程式訂閱者、操作者、訂閱者等。

1. 選取要用於調解的欄位。 您可以使用一個或多個調和標準。

   1. 若要使用屬性來調解資料，請選取&#x200B;**簡單屬性**&#x200B;選項。 **Source**&#x200B;欄位會列出輸入轉變中可供調解的欄位。 **目的地**&#x200B;欄位對應到所選目標維度的欄位。 當來源和目的地相等時，資料就會進行協調。 例如，選取&#x200B;**電子郵件**&#x200B;欄位，以根據設定檔的電子郵件地址刪除重複設定檔。

      若要新增其他調解條件，請按一下&#x200B;**新增規則**&#x200B;按鈕。 如果指定了多個連線條件，則必須全部驗證這些條件，才能將資料連結在一起。

      ![](../assets/workflow-reconciliation-criteria.png)

   1. 若要使用其他屬性來調解資料，請選取&#x200B;**進階調解條件**&#x200B;選項。 然後，您可以使用查詢建模器建立自己的調解條件。

1. 您可以使用&#x200B;**建立篩選器**&#x200B;按鈕來篩選要調解的資料。 這可讓您使用查詢建模器建立自訂條件。

依預設，未調解的資料會保留在出站轉變中，並可在工作表中供未來使用。 若要移除未調和的資料，請停用「**保留未調和的資料**」選項。
