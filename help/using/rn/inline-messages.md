---
title: 移轉至歷程內嵌撰寫
description: 了解如何移轉訊息
exl-id: accdebba-5322-401e-8a40-3e1539e65a7e
source-git-commit: 2160d52f24af50417cdcf8c6ec553b746a544c2f
workflow-type: tm+mt
source-wordcount: '1732'
ht-degree: 3%

---


# 內嵌製作移轉概觀{#inline-authoring}

>[!CONTEXTUALHELP]
>id="ajo_messages_migration_before"
>title="深入了解全新內嵌撰寫功能"
>abstract="自2022年7月25日起，訊息會直接從歷程中撰寫。 現有訊息會自動移轉至新模型。 如果您目前在歷程中使用訊息，則在移轉後將需要其他動作。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/whats-new/inline-authoring/inline-messages-steps.html" text="移轉步驟"

>[!CONTEXTUALHELP]
>id="ajo_messages_migration_during"
>title="了解發生的事"
>abstract="自2022年7月25日起，訊息會直接從歷程中撰寫。 您的環境正在移轉。 如果您目前在歷程中使用訊息，則在移轉後將需要其他動作。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/whats-new/inline-authoring/inline-messages-steps.html" text="移轉步驟"

>[!CONTEXTUALHELP]
>id="ajo_messages_migration_after"
>title="了解如何移轉訊息"
>abstract="自2022年7月25日起，訊息會直接從歷程中撰寫。 現有訊息已移轉至新模型。 身為歷程從業者，使用訊息的歷程現在需要其他動作。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/whats-new/inline-authoring/inline-messages-steps.html" text="移轉步驟"

>[!CONTEXTUALHELP]
>id="ajo_messages_depecrated_inventory"
>title="了解如何移轉訊息"
>abstract="自2022年7月25日起，「訊息」功能表會消失，訊息會直接從歷程中製作。 如果您想在歷程中重複使用舊版訊息，需要將其儲存為範本。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/design/email-templates.html#save-as-template" text="將訊息儲存為範本"

Adobe Journey Optimizer即將推出一項新功能，可改善您編寫Journey Optimizer頻道（電子郵件、推播、簡訊）內容的方式。 作為 Journey Optimizer 的從業人員，現在可直接 建立和編寫 從歷程中傳來的訊息。 

此功能需要移轉使用訊息的現有歷程。 在本頁面中，您會找到有關此變更的必要資訊，以及您需要執行的步驟。

有關您作為Journey Optimizer從業人員的角色和職責的詳細資訊，請參閱 [頁面](../start/path/marketer.md).

<!--
Here are the main changes in the interface:

* Messages are created direcly from journeys.
* The **Messages** entry in the left navigation menu has been removed. 
* There is no separate library of messages, the journey now centralizes all components.


-->

>[!VIDEO](https://video.tv.adobe.com/v/344698)


## 重要的離家出走{#keys}

* **我是否受到影響**:如果您從 **訊息** 功能表，並在您的歷程中使用。 如果您使用協力廠商系統(例如Adobe Campaign)，則不會受此移轉影響。

* **產品變更**:在GA（7月25日），您的頻道內容會在每個歷程中建立及管理。 此 **訊息** 功能表中，左側導覽中的已無法使用([了解更多](../rn/inline-messages.md#change))。 我們會繼續移轉您現有的歷程。

* **時間表**:每個區域在夜間遷移，通過 [迭代](../rn/inline-messages.md#iterations).

   ![](assets/inline-migration-timeline.png)

* **必要動作**:會為您執行歷程的自動轉換。 話雖如此，我們需要你協助幾個步驟。 進一步了解此檔案中的必要步驟 [頁面](../rn/inline-messages-steps.md).

* **淘汰**:9月6日之後，所有仍使用舊版訊息的歷程都會停止，並在稍後刪除。

## 優點和產品變更{#change}

Adobe的願景是不斷簡化產品，以提供有效和最佳化的使用者流程。 這種新的訊息建立方式可更簡化使用者程式。

我們設計了這個新的工作流程，將內容集中在一個位置，直接用於使用中。

內容的建立現在會直接在歷程中執行。 立即 **福利** 您會：

* 在單一流量中使用Journey Optimizer管道，加快建立歷程速度。
* 在歷程中的所有電子郵件、推播和簡訊內容之間順暢地切換，以快速視覺化內容。
* 使用畫布中的內容個人化改善電子郵件和推播的流程。
* 歷程報告可集中化詳細的管道報告資訊。

以下是 **產品變更** 由這項新功能帶來：

<table>
<tr>
<th>移轉前</th>
<th>移轉後</th>
</tr>
<tr>
<td><img src="assets/inline-migration-before.png"><p>之前，您是從 <strong>訊息</strong> 功能表。 </p></td>
<td><img src="assets/inline-migration-after.png"><p>現在， <strong>訊息</strong> 功能表中的任何其他參數。 </p></td>
</tr>
<tr>
<td><img src="assets/inline-migration-before2.png"><p>接著您建立了歷程，並新增 <strong>訊息</strong> 活動，並選取先前建立的訊息。</p></td>
<td><img src="assets/inline-migration-after2.png"><p>您現在只需將所需的管道動作活動（電子郵件、簡訊、推播）新增至歷程即可。 在活動中，您可以直接設定訊息參數並存取內容編輯器。</p></td>
</tr>
<tr>
<td><img src="assets/inline-migration-before3.png"><p>之前，您可在訊息和歷程層級存取報表。 您必須在訊息執行標籤和歷程報表之間導覽。</p></td>
<td><img src="assets/inline-migration-after3.png"><p>所有報表現在都會集中在歷程層級。 這可改善導覽和使用者體驗。 若您在歷程中有多封電子郵件，則可使用 <strong>動作</strong> 下拉式功能表來檢視相關報表。
</p></td>
</tr>
</table>

在正式發行（7月25日）時，此新使用者流程會套用至所有新歷程。 此 **訊息** 功能表中的任何其他參數。

## 移轉時間表{#iterations}

若要使用 **訊息** 包含內嵌撰寫動作的歷程。 將為您執行自動轉換歷程。 話雖如此，我們需要你協助幾個步驟。 

每個區域在夜間，經過數次迭代進行移轉。 以下是移轉時間表：

* 2022年7月25日：GA — 第1次迭代
* 2022年8月1日：第2次迭代
* 2022年9月5日：第3次迭代
* 2022年9月6日：淘汰

為什麼需要多次迭代？

在迭代期間，我們會逐步處理每個歷程，並盡可能移轉這些歷程。 有些情況下，我們不想自動移轉：當歷程為即時（這表示其中仍會有設定檔）。 在這些情況下，我們會要求您執行動作，然後下一個迭代會移轉這些在先前的迭代中無法移轉的歷程。

## 常見問題集 {#faq}

### 如何通知我變更？{#inform}

Adobe在第一次迭代前與您通信。

此變更會在一夜之間部署，經過數次反覆操作。 深入了解 [迭代](../rn/inline-messages.md#inline-authoring).

產品內通知也會通知您，顯示在歷程畫面上：

* 更改部署前

   ![](assets/inline-migration-banner1.png)

* 迭代期間

   ![](assets/inline-migration-banner2.png)

* 迭代後

   ![](assets/inline-migration-banner3.png)

   迭代後， **檢查狀態** 按鈕。 這可讓您以JSON格式檢視所有歷程及其各自的移轉狀態。 看這個 [節](../rn/inline-messages.md#status).

* 當橫幅消失時，你就可以走了。 您無需執行任何動作。

### 什麼是移轉程式？{#process}

非上線或關閉的歷程會完全自動移轉。 我們不想影響即時或已關閉的歷程，以避免對生產造成任何影響。 請您發佈我們為您建立的新版本。

客戶組織的所有沙箱會同時處理。 在更改部署期間，將執行以下操作：

**未使用訊息的任何歷程**

這些不受變更影響。 移轉只會鎖定使用訊息的歷程。 不過，您仍可以透過下列URL存取歷程中未使用的訊息：https://experience.adobe.com/#/@[ORG]/sname:[沙箱]/journey-optimizer/messages/

**使用至少一則訊息的草稿歷程**

移轉期間會修改訊息的草稿版本。 他們不再參考訊息。 此 **訊息** 活動會以適當的管道動作活動取代。 每個都包含頻道參數和內容。

照常，請先測試您的草稿歷程，再發佈。

**使用至少一則訊息的即時歷程**

歷程的即時版本會持續執行，以避免對生產造成任何影響。

移轉期間會建立此歷程的新草稿版本。 這個新草稿版本是您即時版本的復本，但訊息會以內嵌撰寫的管道動作取代。 每個管道動作活動都包含管道參數和內容。 內容不會遺失。 報表不會遺失。

我們希望您能檢閱此草稿版本、測試並發佈，使其成為即時版本。

**已完成或已停止歷程（使用至少一則訊息）**

這些歷程也會移轉。

查看歷程報表時，報表現在會更豐富，並包含先前可在訊息報表中使用的資訊等級。

**使用至少一則訊息的CLOSED歷程**

歷程的封閉版本會針對內的任何設定檔持續執行，以避免對生產造成任何影響。

30天後，已關閉的歷程會自動切換為「已完成」狀態。 完成後，會在下一個迭代中考慮這些參數。

**多管道歷程**

這些不會移轉。 你必須重新建立它們。

### 身為客戶的我有哪些動作項目？{#actions}

系統會為您執行歷程的自動轉換，但需要一些步驟。 進一步了解此檔案中的必要步驟 [頁面](../rn/inline-messages-steps.md).

<!--

The process timeline is indicated in a blue banner on the Journeys screen. See this [section](../rn/inline-messages.md#inform). 

**Before migration**

* Check the date indicated in the banner. 
* Stop non-critical journeys, on development, stage and production environments.
* If you have draft messages that you want to keep using, add them to a journey so they are migrated.

**During migration**

* Migration occurs at night-time
* Do not to create, edit or delete journeys.

**After migration**

* After each iteration, click the **Check status** button in the top banner. This page lists all journeys and their migration status. See this [section](../rn/inline-messages.md#status). 

* For each live journey, a new version is created. Review the new version, test it and publish it. 

* The **Messages** menu, in the left navigation is no longer available. You need to use the new in-line message feature. See this [section](../rn/inline-messages.md#change). 

* If you need to access a specific message which was not used in a journey, you can use this URL and save the content as a template: https://experience.adobe.com/#/@[ORG]/sname:[SANDBOX]/journey-optimizer/messages/

## How can I check the migration status?{#status}

Click the **Check status** button in the top banner. The following page is displayed.

![](assets/inline-migration-log.png)

The status report is at sandbox level. This report includes several useful sections:

**migrationStatus**

This section displays the migration information since the first iteration. Numbers are incremented after each iteration.

* MIGRATED: number of draft journeys migrated successfully.
* NEW_VERSION_CREATED: number of live journeys migrated. For each live journey, a new draft version is created: you must test and publish this version.
* ERROR: number of draft journeys not migrated because of a failure. You need to re-create them.
* ERROR_ON_NEW_VERSION_CREATION: number of live journeys not migrated because of a failure. new draft journey versions not migrated because of a failure. You need to re-create them.

**eligibilityStatus**

This section lists the remaining items after the last iteration:

* toMigrate: number of draft journeys that need to be migrated.
* createNewVersion: number of live journeys to migrate.
* noMigration_live: number of live journeys that do not need to be migrated
* noMigration: number of draft journeys that do not need to be migrated.

The **details** section gives, for each of the above indicators, the list of related journeys.

-->

### 如何檢查移轉狀態？{#status}

按一下 **檢查狀態** 按鈕。 將顯示以下頁面。

![](assets/inline-migration-log.png)

狀態報表位於沙箱層級。 此報表包含數個實用章節：

**migrationStatus**

此部分顯示自第一次迭代以來的遷移資訊。 數字會在每次迭代後增加。

* 已移轉：成功移轉草稿、已完成和已停止的歷程數。
* NEW_VERSION_CREATED:已移轉的即時歷程數量。 系統會針對每個即時歷程建立新的草稿版本：您必須測試並發佈此版本。
* 錯誤：因失敗而未移轉的草稿、已完成和已停止歷程數。 你需要重新建立它們。
* ERROR_ON_NEW_VERSION_CREATION:因失敗而未移轉的即時歷程數。 因為失敗而未移轉新的草稿歷程版本。 尚未為其建立新草稿版本。 您必須手動重新建立。

**apilityStatus**

本節列出上次迭代後的剩餘項目：

* toMigrate:需要移轉的草稿、已完成和已停止歷程數。
* createNewVersion:要移轉的即時歷程數量。
* noMigration_live:不需要移轉的即時歷程數量。 此處也會列出已關閉的歷程。
* noMigration:不需要移轉的歷程數量。

此 **詳細資訊** 一節會針對上述各節提供相關歷程的清單。

### 這項變更是否會造成服務中斷？{#interruption}

服務不會中斷。

* 在即時歷程：沒有影響，它們一直在運行。
* 在製作歷程中：在移轉期間（在夜間），強烈建議不要建立、編輯或刪除歷程。

### 資料會丟失嗎？ {#data}

不會遺失資料，也不會影響即時歷程。 您將可控制發佈更新的歷程版本。

### 是否會失去功能？{#functionality}

您製作訊息的方式將有所變更。 不會失去功能。

### 在遷移過程中是否可以訪問環境？

遷移發生在夜間。 您將能使用產品。 但請勿建立、編輯或刪除歷程。

### 訊息是否會繼續傳送？

是的，即時歷程會持續執行。

### 如何知道移轉已完成？

橫幅消失時，移轉完成。 看這個 [節](../rn/inline-messages.md#inform).

### 訊息相關權限會受到哪些影響？

內嵌製作功能會影響權限。 每個與訊息相關的權限，例如 [!DNL View Messages] 或 [!DNL Manage Messages]，會自動納入連結至歷程功能的權限中。

了解更多資訊 [頁面](../administration/ootb-product-profiles.md).

<!--
* Improved authoring flow and navigation
* Personalization: improved contextual personalization flow
* Reporting: the message execution screen will no longer exist. Reporting is centralized in journeys.
* You will still be able to update content in a live journey.
->>
