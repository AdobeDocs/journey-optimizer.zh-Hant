---
title: 關於 Adobe Experience Platform 區段
description: 瞭解如何配置Adobe Experience Platform段
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 10d2de34-23c1-4a5e-b868-700b462312eb
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 1%

---

# 開始使用Adobe Experience Platform段 {#about-segments}

[!DNL Journey Optimizer]  允許您直接使用即時客戶配置檔案資料建立Adobe Experience Platform段 **[!UICONTROL Segments]** 把菜單和它們融入你的旅程。

請注意，段也可以從分段服務本身建立。 在 [Adobe Experience Platform分段處檔案](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html)。

您可以以不同方式在行程中利用段：

* 使用 **讀取段** 業務流程活動，使屬於指定段的所有個人進入行程。 您行程中包含的消息將發送給屬於該段的個人。 假設您有「銀色客戶」部分。 通過本練習，您可以讓所有銀發客戶輸入行程併發送一系列個性化消息。

   有關如何使用的詳細資訊 **[!UICONTROL Read segment]** 活動，請參閱 [此部分](../building-journeys/read-segment.md#configuring-segment-trigger-activity)。

* 使用 **分部資格** 活動，讓個人根據Adobe Experience Platform段出入口進入或前進行程。 例如，您可以讓所有新銀客戶輸入行程併發送消息。 有關如何使用此活動的詳細資訊，請參閱 [此部分](../building-journeys/segment-qualification-events.md)。

* 生成 **複雜條件** 使用簡單或高級表達式編輯器執行。 瞭解詳情 [此部分](../building-journeys/condition-activity.md#using-a-segment)。

## Adobe Journey Optimizer評價方法 {#evaluation-method-in-journey-optimizer}

在Adobe Journey Optimizer，使用下列評價方法之一從段定義生成受眾：

* 流分段 — 段的受眾清單在新資料流入系統時即時保持最新。
* 批分段 — 段的受眾清單根據過去一小時內到達的資料按小時更新。

系統根據分段規則的複雜度和評估成本，對每個分段定義確定分批分段和流分段。

可查看中每個段的評估方法 **[!UICONTROL Evaluation method]** 的子菜單。

在您首次定義段後，配置檔案在符合條件時添加到受眾。

從先前資料中回填觀眾最多需要24小時。 在觀眾回填後，觀眾會不斷更新，隨時準備瞄準。
