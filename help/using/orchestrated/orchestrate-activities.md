---
solution: Journey Optimizer
product: journey optimizer
title: 使用Adobe Journey Optimizer建立協調的行銷活動
description: 瞭解如何使用Adobe Journey Optimizer建立協調的行銷活動
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: d1d64125-cf00-49c2-a71d-1494ede16f61
source-git-commit: 1aa4f3e24a4cb7594232c0b25da8c9fd2e62c1de
workflow-type: tm+mt
source-wordcount: '994'
ht-degree: 1%

---

# 協調行銷活動 {#orchestrate}

+++ 目錄

| 歡迎使用協調的行銷活動 | 首次建立協調的行銷活動 | 查詢資料庫 | 協調的行銷活動 |
|---|---|---|---|
| [開始使用協調的行銷活動](gs-orchestrated-campaigns.md)<br/><br/>建立和管理關聯式結構描述和資料集：</br> <ul><li>[手動結構描述](manual-schema.md)</li><li>[檔案上傳結構描述](file-upload-schema.md)</li><li>[擷取資料](ingest-data.md)</li></ul><br/><br/>[存取及管理協調的行銷活動](access-manage-orchestrated-campaigns.md)<br/><br/>[建立協調行銷活動的重要步驟](gs-campaign-creation.md) | [建立並排程行銷活動](create-orchestrated-campaign.md)<br/><br/><b>[協調活動](orchestrate-activities.md)</b><br/><br/>[開始並監視行銷活動](start-monitor-campaigns.md)<br/><br/>[報告](reporting-campaigns.md) | [使用規則產生器](orchestrated-rule-builder.md)<br/><br/>[建立您的第一個查詢](build-query.md)<br/><br/>[編輯運算式](edit-expressions.md)<br/><br/>[重新鎖定目標](retarget.md) | [開始使用活動](activities/about-activities.md)<br/><br/>活動：<br/>[並加入](activities/and-join.md) - [建立對象](activities/build-audience.md) - [變更維度](activities/change-dimension.md) - [頻道活動](activities/channels.md) - [合併](activities/combine.md) - [重複資料刪除](activities/deduplication.md) - [擴充](activities/enrichment.md) - [分支](activities/fork.md) - [調解](activities/reconciliation.md) - [儲存對象](activities/save-audience.md) - [分割](activities/split.md) - [等待](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

此頁面上的內容不是最終內容，可能會有變動。

>[!ENDSHADEBOX]

[建立協調的行銷活動](gs-campaign-creation.md)後，您就可以開始協調它將執行的不同工作。 為此，我們提供視覺畫布，讓您建構協調的行銷活動圖表。 在此圖表中，您可以新增各種活動，並依序連線它們。

## 新增活動 {#add}

在設定的這個階段，圖表會顯示開始圖示，代表協調行銷活動的開始。 若要新增您的第一個活動，請按一下連線到開始圖示的&#x200B;**+**&#x200B;按鈕。

可新增至圖表的活動清單隨即顯示。 可用的活動取決於您在協調的行銷活動圖表中的位置。 例如，新增第一個活動時，您可以透過鎖定對象、分割協調的行銷活動路徑或設定&#x200B;**等待**&#x200B;活動以延遲協調的行銷活動執行，來開始協調的行銷活動。 另一方面，在&#x200B;**建立對象**&#x200B;活動後，您可以調整目標定位活動、傳送傳遞至具有頻道活動的對象，或組織具有流量控制活動的協調行銷活動程式。

![](assets/orchestrated-start.png){zoomable="yes"}

將活動新增到圖表後，會出現右側窗格，可讓您使用特定設定進行設定。 有關如何設定每個活動的詳細資訊，請參閱[本節](activities/about-activities.md)。

![](assets/orchestrated-configure-activities.png){zoomable="yes"}

重複此程式，根據您想要協調的行銷活動執行的工作，視需要新增儘可能多的活動。 請注意，您也可以在兩個活動之間插入新活動。 若要這麼做，請按一下活動之間轉變上的&#x200B;**+**&#x200B;按鈕，選取所需的活動，並在右窗格中設定它。

您可以選擇個人化每個活動之間的轉變名稱。 要執行此操作，請選取轉變並在右窗格中變更其標籤。

![](assets/canvas-transition.png)

### 畫布工具列 {#toolbar}

畫布工具列提供可輕鬆操控活動並在畫布中導覽的選項：

![](assets/orchestrated-toolbar.png)

![多重選取模式圖示](assets/do-not-localize/canvas-multiple.svg)選取多個活動，一次刪除所有活動或複製並貼上它們。 [瞭解如何複製貼上活動](#copy)

![旋轉圖示](assets/do-not-localize/canvas-rotate.svg)垂直切換畫布。

![符合熒幕圖示](assets/do-not-localize/canvas-fit.svg)根據熒幕調整畫布縮放等級。

![縮小圖示](assets/do-not-localize/canvas-zoomout.svg) ![放大圖示](assets/do-not-localize/canvas-zoomin.svg)縮小或進入畫布。

![促銷活動設定圖示](assets/do-not-localize/canvas-map.svg)開啟畫布的快照，顯示您所在的位置。

### 管理活動 {#manage}

新增活動時，屬性窗格中會顯示動作按鈕，可讓您執行多項作業。

![](assets/activity-action.png)

![刪除圖示](assets/do-not-localize/activity-delete.svg)從畫布中刪除活動。

![停用圖示](assets/do-not-localize/activity-disable.svg) ![啟用圖示](assets/do-not-localize/activity-enable.svg)停用/啟用活動。 執行協調的行銷活動時，停用的活動以及相同路徑上的下列活動不會執行，且協調的行銷活動會停止。

![暫停圖示](assets/do-not-localize/activity-pause.svg) ![繼續圖示](assets/do-not-localize/activity-resume.svg)暫停/繼續活動。 執行協調的行銷活動時，會在暫停的活動中暫停。 系統不會執行對應的任務，以及在相同路徑中跟隨著該任務的所有任務。

    您可以使用畫布中的任何活動作為中斷點，以暫停行銷活動執行。 這表示此活動只會執行促銷活動，直到此活動為止，然後暫停執行。 暫停執行時，分段引擎會保留暫時資料供您預覽。 您可以在暫停的活動之前選取入站轉變，以檢視傳輸的資料。 深入瞭解此章節： [視覺流量監視](../orchestrated/start-monitor-campaigns.md#flow)。

![復製圖示](assets/do-not-localize/activity-copy.svg)複製活動。 [瞭解如何複製貼上活動](#copy)

![記錄檔與工作圖示](assets/do-not-localize/activity-logs.svg)存取活動的記錄檔與工作。

若干&#x200B;**目標定位**&#x200B;活動（例如&#x200B;**合併**&#x200B;或&#x200B;**重複資料刪除**），可讓您處理剩餘母體，並將其納入其他出站轉變中。 例如，如果您使用&#x200B;**分割**&#x200B;活動，則補數包含不符合任何先前定義之子集的母體。 若要使用此功能，請啟動&#x200B;**[!UICONTROL 產生補充]**&#x200B;選項。

### 複製貼上活動 {#copy}

您可以複製活動，並將其貼到任何已協調的行銷活動畫布中。 目的地行銷活動可以在不同的瀏覽器索引標籤中。

* 若要複製一個活動，請按一下活動屬性窗格中的![復製圖示](assets/do-not-localize/activity-copy.svg)按鈕。
* 若要複製多個活動，請按一下畫布工具列中的![多重選取模式圖示](assets/do-not-localize/canvas-multiple.svg)圖示。

| 複製一個活動 | 複製多個活動 |
|  ---  |  ---  |
| ![](assets/orchestrated-copy-1.png){width="200" align="center" zoomable="yes"} | ![](assets/orchestrated-copy-2.png){width="200" align="center" zoomable="yes"} |

若要貼上活動，請按一下轉變上的&#x200B;**+**&#x200B;按鈕，然後選取「貼上x活動」。

![](assets/orchestrated-copy-3.png){zoomable="yes"}{width="50%"}

## 圖表範例 {#example}

以下是精心設計的行銷活動範例，其設計旨在傳送電子郵件給購買量至少為100$的所有客戶，同時排除忠誠度低於50點的所有客戶。

![](assets/canvas-example-diagram.png){zoomable="yes"}

為達成此目的，已新增下列活動：

* **[!UICONTROL 分支]**&#x200B;活動將協調的行銷活動分為三個路徑。
* **[!UICONTROL 建立對象]**&#x200B;活動以三組客戶為目標：

   * 擁有電子郵件的客戶，
   * 已購買至少100$的客戶，
   * 忠誠點數少於50的客戶。

* **[!UICONTROL 將]**&#x200B;個活動群組與擁有電子郵件的客戶及已購買至少100$的客戶結合，
* **[!UICONTROL 合併]**&#x200B;活動會排除忠誠度低於50分的客戶，
* **[!UICONTROL 電子郵件傳遞]**&#x200B;活動會傳送電子郵件給產生的客戶。

## 後續步驟 {#next}

成功設計協調的行銷活動圖表後，您可以執行協調的行銷活動並追蹤其各種任務的進度。 [瞭解如何開始協調的行銷活動並監視其執行](start-monitor-campaigns.md)
