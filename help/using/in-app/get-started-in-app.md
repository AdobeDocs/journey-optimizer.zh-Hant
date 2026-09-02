---
title: 開始使用應用程式內傳送訊息
description: 了解如何透過 Journey Optimizer 傳送應用程式內通知
feature: In App
topic: Content Management
role: User
level: Beginner
keywords: 應用程式內、訊息、建立、開始
exl-id: 51562843-7b50-4eb5-bf79-5ce03f7549cb
TQID: https://experienceleague.adobe.com/b139LQsPe3HwKe1O5cyBx4Nj4jpW3GXCFIVIWTAIlbg
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2: id: b3a93754-a8b8-46eb-9421-7eccaeeb3dffid: cc5c44e2-54a1-4927-b794-442cd87d8f74id: c96d2aa5-76a2-443d-8d23-5de95577c909id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: 75ebd043971ce40e2da0f627622441a46a8e667c
workflow-type: ht
source-wordcount: 601
ht-degree: 100%

---

# 開始使用應用程式內頻道 {#gs-in-app}

>[!BEGINSHADEBOX]

**在此頁面上：**&#x200B;開始使用 Adobe Journey Optimizer 中的應用程式內傳訊管道，透過通知與應用程式使用者互動，以推廣功能、產品建議和上線。

>[!ENDSHADEBOX]

應用程式內訊息是可傳送給應用程式內使用者的通知，可引導他們前往特定興趣點。 這些通知可用於不同的用途，例如推廣新功能、呈現優惠或協助使用者上線。 藉由善用應用程式內訊息，您可有效與客群進行互動，並引導他們關注應用程式的重要環節。

使用 Journey Optimizer 建立應用程式內通知，並設定體驗選項，包括訊息版面及顯示、文字與按鈕選項。

</br>

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="inapp-configuration.md">
<img alt="驗證" src="../assets/do-not-localize/inapp-config.jpg">
</a>
<div>
<a href="inapp-configuration.md"><strong>設定應用程式內頻道</strong></a>。
</div>
<p>
</td>
<td>
<a href="create-in-app.md">
<img alt="銷售機會" src="../assets/do-not-localize/inapp-create.jpeg">
</a>
<div><a href="create-in-app.md"><strong>建立應用程式內訊息</strong>
</div>
<p>
</td>
<td>
<a href="design-in-app.md">
<img alt="不頻繁" src="../assets/do-not-localize/inapp-design.jpg">
</a>
<div>
<a href="design-in-app.md"><strong>設計您的應用程式內內容</strong></a>
</div>
<p></td>
<td>
<a href="../reports/campaign-global-report-cja-inapp.md">
<img alt="驗證" src="../assets/do-not-localize/inapp-report.jpg">
</a>
<div>
<a href="../reports/campaign-global-report-cja-inapp.md"><strong>存取應用程式內報告</strong></a>
</div>
<p>
</td>
</tr></table>

## 使用案例

當您想在使用者已經與應用程式互動時引導或影響他們，並把握其主動關注的時機，應用程式內訊息最能發揮效果。

| 優點 | 原因 | 使用案例範例 |
| --- | --- | --- |
| 高使用者參與度 | 在使用者主動進行應用程式工作階段時觸及他們 | 功能公告、入門提示 |
| 符合情境的觸發條件 | 可根據應用程式內行為或位置觸發 | 在使用者造訪相關畫面後立即醒目提示某項功能 |
| 即時傳遞 | 不依賴推播權杖或外部傳遞服務 | 目前工作階段期間顯示的時效性提示 |
| 不依賴外部管道 | 完全在應用程式內運作，不受其他管道的選擇加入狀態影響 | 觸及已選擇退出推播通知的使用者 |
| 更高的轉換潛力 | 在使用者主動關注的時刻傳遞，提高回應率 | 追加銷售或交叉銷售優惠、調查提示 |
| 自訂和細分 | 可針對特定客群調整版面、文字和按鈕 | 針對不同使用者區段的個人化入門流程 |
| 非侵入式設計 | 可設計為補充使用者體驗，而不是中斷使用者體驗 | 符合應用程式 UI 的橫幅或強制回應視窗 |

## 不適用情境

應用程式內訊息仰賴作用中工作階段，因此不適合所有情境。在下列情況下，建議考慮採用其他管道：

* 使用者並未主動使用應用程式，因為訊息將永遠不會顯示
* 訊息涉及重大或時效性問題，需要在應用程式外觸及使用者，例如服務中斷或安全性警示
* 通訊內容涉及法規或法律要求，且需要應用程式內訊息無法提供的已讀確認
* 目標是為不太可能開啟應用程式的非使用中使用者重新啟用帳戶或進行贏回行銷活動
* 訊息是大量交易型更新，例如訂單確認，更適合電子郵件或簡訊
* 過度使用可能導致橫幅失明，即使用者開始忽略顯示過於頻繁的訊息
* 當訊息要傳送時，使用者可能處於離線狀態或沒有應用程式連線



## 其他資源

* **[建立應用程式內訊息](create-in-app.md)** - 了解如何為行動應用程式建立和設定應用程式內訊息。
* **[設定應用程式內管道](inapp-configuration.md)** - 使用適當的行動應用程式設定來設定您的應用程式內傳訊管道。
* **[設計應用程式內內容](design-in-app.md)** - 自訂應用程式內訊息版面、樣式、按鈕和互動式元素。
* **[網頁應用程式內](create-in-app-web.md)** - 探索如何建立和傳遞網頁應用程式的應用程式內訊息。
* **[應用程式內管道教學課程](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer-learn/tutorials/channels/in-app-channel/in-app-messages-overview){target="_blank"}** - 探索應用程式內傳訊功能和最佳做法的逐步教學課程影片。

