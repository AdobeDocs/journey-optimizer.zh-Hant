---
solution: Journey Optimizer
product: journey optimizer
title: IP熱身傳遞指南
description: 瞭解IP熱身的可傳遞性基礎和最佳實務
feature: IP Warmup Plans
topic: Administration
role: Admin
level: Experienced
keywords: IP、傳遞能力、信譽、ISP、參與
exl-id: TBD
source-git-commit: b1b9b34aec305d6690d93e68238aed852ef689b7
workflow-type: tm+mt
source-wordcount: '1088'
ht-degree: 6%

---

# IP熱身傳遞指南 {#ip-warmup-deliverability-guide}

在Adobe Journey Optimizer中以新IP位址或網域啟動電子郵件行銷活動時，瞭解傳遞能力基礎對於建立強大的寄件者信譽至關重要。 本指南涵蓋重要概念、準備步驟和最佳實務，協助您從零信譽轉變為成功的收件匣放置。

➡️ [觀看此影片以瞭解IP熱身傳遞基礎知識](#video)

>[!NOTE]
>
>如需在Adobe Journey Optimizer中實作IP預熱計畫的逐步指示，請參閱[開始使用IP預熱計畫](ip-warmup-gs.md)。

## 為什麼IP和網域信譽很重要 {#reputation-matters}

信箱提供者(Gmail、Yahoo、Microsoft、Apple Mail等)會根據四大支柱評估每個寄件者：

* **投訴**：收件者是否將您的郵件標示為垃圾訊息？
* **參與**：收件者是否開啟、按一下或回覆您的電子郵件？
* **基礎架構**：您的傳送基礎架構是否已驗證、穩定且值得信賴？
* **內容**：您的訊息內容是否顯示合法且有價值？

IP熱身主要處理前三大支柱，方法是在您擴充至完整傳送量之前，逐步向信箱提供者證明您的新基礎架構是合法且想要的。

## 預檢檢查清單 {#pre-flight-checklist}

開始準備IP位址之前，請確定所有基本元素都已準備就緒。 下表概述在開始IP熱身計畫之前要完成的基本工作。

| 任務 | 為何這項能力很重要 | 完成方式 |
|------|----------------|-------------------|
| 在AJO中保留固定IP並委派子網域 | 所有未來的信譽都附加到這些基礎結構元素 | 瀏覽至&#x200B;**[!UICONTROL 管理]** > **[!UICONTROL 管道]** > **[!UICONTROL 電子郵件設定]** > **[!UICONTROL 子網域]**。 [了解更多](delegate-subdomain.md) |
| 設定SPF和DKIM | 確認您的傳送伺服器是否合法且已授權 | 子網域委派和通道設定建立後，Adobe會自動處理。 [了解更多](delegate-subdomain.md) |
| 設定 DMARC 記錄 | 啟用電子郵件驗證報告和未來執行政策 | 子網域委派和通道設定建立後，Adobe會自動處理。 [了解更多](dmarc-record.md) |
| 設定種子清單監視 | 在預熱流程早期偵測收件匣位置問題 | 建立管道設定時新增種子地址。 [了解更多](seed-lists.md) |
| 建置階段1高參與度對象 | 與最活躍的收件者提高早期參與量度 | 建立過去30天內開啟或點按少於5,000個連絡人的對象 |

>[!CAUTION]
>
>驗證問題(SPF、DKIM、DMARC)無法透過大量調整來解決。 在開始傳送之前，請確定已正確設定這些專案。

## 四周熱身行事曆範例 {#warmup-calendar}

此範例行事曆會根據您的最終每日容量(UDV)的百分比，提供漸進式容量增加。 調整這些數字以符合您的特定傳送需求，並與您的傳遞顧問合作，建立自訂計畫。

| 日 | UDV的% | 目標客群 | 內容建議 |
|------|----------|-----------------|------------------------|
| 1-3 | 0.5% | 您參與度最高的收件者 | 使用簡短的純文字格式，並在摺頁上方加上清楚的call-to-action |
| 4-7 | 1% | 參與的使用者加上最近的購買者 | 新增輕量型主圖影像，將連結限製為3個或更少 |
| 8-14 | 5% | 更廣泛的作用中訂閱者清單 | 介紹您的標準電子郵件範本，但避免大量促銷內容 |
| 15-21 | 25% | 作用中及輕度非作用中的訂閱者 | 使用一般行銷內容，同時密切監控投訴率 |
| 22-28 | 50-100% | 完整清單（遵循隱藏清單） | 轉換為您的穩定狀態傳送步調 |

>[!NOTE]
>
>Adobe Journey Optimizer提供專屬的[IP熱身計畫功能](ip-warmup-gs.md)，可自動化磁碟區管理並簡化熱身程式，而不需要複雜的歷程設定。

## 使用AJO的IP熱身計畫功能 {#ajo-warmup-feature}

Adobe Journey Optimizer包含簡化的IP熱身計畫功能，可免除透過複雜歷程設定手動設定容量上限的需求。 此功能可確保以標準化方式建立傳送者信譽。

### 運作方式

1. **建立IP熱身行銷活動**：在啟用&#x200B;**[!UICONTROL IP熱身計畫啟用]**&#x200B;選項的情況下建立一或多個行銷活動。 [了解更多](ip-warmup-campaign.md)

1. **設定您的計畫**：存取&#x200B;**[!UICONTROL 管理]** > **[!UICONTROL 管道]** > **[!UICONTROL 電子郵件設定]** > **[!UICONTROL IP熱身計畫]**，並上傳您與傳遞顧問準備的分階段熱身範本。 [了解更多](ip-warmup-plan.md)

1. **執行階段**：為每個階段選取行銷活動並啟動對應的執行。 系統會自動將設定檔排除在先前執行之外，以防止過度聯絡。 [了解更多](ip-warmup-execution.md)

1. **監視和調整**：使用整合的報告儀表板來追蹤進度、監視執行狀態，並在發生問題時修改您的計畫。 [了解更多](ip-warmup-execution.md#monitor-plan)

## 即時監控和關鍵量度 {#monitoring}

Adobe Journey Optimizer提供內建的報告功能，可追蹤您的IP熱身效能：

* **即時報表**：從&#x200B;**[!UICONTROL 過去24小時]**&#x200B;索引標籤存取行銷活動的即時測量和視覺化。 [了解更多](../reports/live-report.md)

* **Customer Journey Analytics整合**：如需更深入的見解，請利用Customer Journey Analytics分析來自Adobe Experience Platform的資料並建立自訂視覺效果。 [了解更多](../reports/report-gs-cja.md)

### 目標量度

在整個熱身過程中監視這些關鍵效能指標：

| 量度 | 目標臨界值 | 超過時的動作 |
|--------|-----------------|-------------------|
| 投訴率 | ≤ 0.1% | 稽核區段並抑制慢性投訴者 |
| 硬跳出率 | ≤ 2% | 檢閱清單品質和衛生實務 |
| 開啟率 | ≥ 10% | 確認您正在鎖定參與的對象 |

>[!TIP]
>
>如需完整的行銷活動分析，請使用[行銷活動即時報告](../reports/campaign-live-report.md#email-live)和[Customer Journey Analytics報告](../reports/campaign-global-report-cja-email.md)功能。

## 疑難排解Playbook {#troubleshooting}

使用此決策矩陣解決預熱期間的常見問題：

| 症狀 | 可能的原因 | 建議的動作 |
|---------|--------------|-------------------|
| Yahoo暫時失敗（421錯誤） | 音量增加太快 | 暫停傳送24小時，然後在先前的層級重新啟動 |
| 種子帳戶的開啟率低於2% | IP封鎖清單 | 檢查[Google Postmaster Tools](https://postmaster.google.com/)和[Microsoft SNDS](https://sendersupport.olc.protection.outlook.com/snds/)；視需要開啟傳遞能力票證 |
| 投訴率超過0.3% | 目標定位錯誤或對象過時 | 稽核區段定義並從您的[隱藏清單](manage-suppression-list.md)中排除慢性申訴者 |

>[!IMPORTANT]
>
>減緩您的熱身速度比稍後嘗試修復損壞的寄件者信譽要好。 永遠將維持健康量度優先於大幅增加量。

## 熱身後最佳實務 {#post-warmup}

完成熱身計畫且量度穩定後：

* **維持一致性**：將每日流量每週增加量保持在30%以下，以維護您既定的信譽

* **持續監視**：排程每季的信譽健康情況檢查，以主動識別並解決問題

* **遵守參與訊號**：繼續將參與的收件者排定優先順序，並對非作用中訂閱者實施重新參與行銷活動

* **保持驗證最新**：定期確認您的SPF、DKIM和DMARC記錄保持正確設定

## 重要技巧 {#key-takeaways}

* **IP熱身是必要的**：略過熱身程式所花費的時間和聲譽比正確執行它所需的花費更多

* **資料導向式決策**：每天追蹤投訴、跳出和參與率，並在ISP懲罰您之前調整您的策略

* **先驗證，然後磁碟區**：先解決所有SPF、DKIM和DMARC問題，再開始遞增磁碟區

* **一致性很重要**：信箱提供者偏好可預測的傳送模式；避免突然的磁碟量尖峰或不規則的傳送排程

## 作法影片 {#video}

瞭解Adobe Journey Optimizer中的傳遞能力基礎知識、信譽建立和IP熱身最佳實務。

>[!VIDEO](https://video.tv.adobe.com/v/3463793/?captions=chi_hant&learn=on)

<!--
>[!NOTE]
>
>For more guidance, explore the [Adobe Journey Optimizer Deliverability Guide blog post](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/adobe-journey-optimizer-deliverability-guide-from-zero/ba-p/761950).-->

## 相關主題 {#related-topics}

* [開始使用 IP 暖身計劃](ip-warmup-gs.md)
* [建立 IP 暖身行銷活動](ip-warmup-campaign.md)
* [建立 IP 暖身計劃](ip-warmup-plan.md)
* [執行 IP 暖身計劃](ip-warmup-execution.md)
* [設定管道設定](channel-surfaces.md)
* [委派子網域](delegate-subdomain.md)
* [管理禁止名單](manage-suppression-list.md)
* [傳遞能力最佳實務指南](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/introduction.html?lang=zh-Hant)

