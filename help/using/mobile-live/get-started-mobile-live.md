---
solution: Journey Optimizer
product: journey optimizer
title: 開始使用即時動態
description: 了解如何在 Journey Optimizer 中傳送即時動態
topic: Content Management
role: User
level: Beginner
exl-id: c9766603-df19-4efd-8319-27e9764254b4
TQID: https://experienceleague.adobe.com/IB00r0QSfCthvgvyqubGwsaUoiJKBL-E96duLn4R5i0
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: b49ca41f-eb7a-4f4b-abeb-a97c06fd0c04
  - id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2:
  - id: c96d2aa5-76a2-443d-8d23-5de95577c909
  - id: ed2fba79-65cb-4680-96d2-2ad5d851714d
  - id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: ee6e1c0a2d86736e51257315fa41c4796286579f
workflow-type: tm+mt
source-wordcount: 404
ht-degree: 94%

---

# 開始使用即時動態 {#get-started-mobile-live}


即時動態是裝置鎖定畫面上所顯示的永久、可瀏覽的 UI 元素。 它們可讓您的應用程式呈現即時且最新的資訊，讓使用者在整個進行中的事件中都能接收最新資訊，而不需要他們開啟應用程式或接收重複的推播通知。

>[!AVAILABILITY]
>
>Adobe Journey Optimizer 中的即時動態僅與 Apple iOS 相容。

不同於傳統的推播通知，即時動態代表&#x200B;**以狀態為基礎的參與**：這些活動不會傳送一次性警報，而是會維持持續的、情境式的存在，並隨著事件的發展而動態更新。


<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<img alt="鎖定畫面和動態島上的 iOS 即時動態" src="assets/do-not-localize/live-activity.jpeg">
</td>
<td>
<p><strong>主要優點</strong></p>
<p>即時動態將行動參與從通知型轉變為狀態型，讓品牌能夠：</p>
<ul>
<li>在整個高價值事件中，<strong>持續存在</strong>於鎖定畫面上</li>
<li><strong>以動態方式更新資訊</strong>，避免重複通知給使用者帶來負擔</li>
<li>提供與現實事件相連結的<strong>更豐富、更情境式</strong>的行動時刻</li>
<li>在進行中交易或即時體驗期間<strong>提高參與度和保留率</strong></li>
</ul>
</td>
</tr>
</table>

使用 Adobe Journey Optimizer，您可以透過 API 觸發的行銷活動，以程式設計方式從遠端&#x200B;**開始**、**更新**&#x200B;和&#x200B;**結束**&#x200B;即時動態，以大規模支援個別和客群型使用案例。

即時活動只能&#x200B;**透過** API觸發&#x200B;**行銷活動啟動**，允許您提供自訂裝載，並透過您自己的裝載執行所有個人化。
必須根據預期的即時活動使用案例選取適當的&#x200B;**API觸發**&#x200B;行銷活動型別：

* 針對廣播使用案例選取 **API 觸發的行銷**——大規模傳送的客群型更新：

   * 體育賽事分數和即時事件倒計時
   * 航線上所有乘客的航班狀態更新
   * 跨使用者區段的共用體驗

* 針對個別使用案例選取 **API 觸發交易型**，每位使用者的 1:1 次即時更新：

   * 訂單追蹤與交付進度
   * 設施或服務狀態更新
   * 即時預訂和預約確認

## 快速入門手冊

請完成下列步驟，在您的應用程式中設定並實作即時動態：

1. **[設定 Adobe Journey Optimizer](mobile-live-configuration.md)**

   透過建立行動設定來設定您的環境。

1. **[整合 Adobe Experience Platform Mobile SDK](mobile-live-configuration-sdk.md)**

   與 Adobe Experience Platform Mobile SDK 整合，以啟用鎖定畫面和動態島上的即時動態更新。

1. **[在 Journey Optimizer 中建立即時動態](create-mobile-live.md)**

   在 Journey Optimizer 中使用 API 觸發的行銷活動來啟動您的即時動態。

1. **[監視您的行銷活動](../reports/campaign-global-report-cja-activity.md)**

   開始使用內建報告來衡量您的即時動態的影響。

## 作法影片

探索如何使用 Adobe Journey Optimizer 設定 iOS 即時動態，以在 iPhone 鎖定畫面和動態島上提供豐富的即時更新。

>[!VIDEO](https://video.tv.adobe.com/v/3479864/?learn=on)
