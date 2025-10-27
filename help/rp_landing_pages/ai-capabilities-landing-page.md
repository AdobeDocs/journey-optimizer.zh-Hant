---
solution: Journey Optimizer
product: Journey Optimizer
title: Adobe Journey Optimizer中的AI功能
description: Adobe Journey Optimizer中的AI功能
hide: true
hidefromtoc: true
source-git-commit: 2b377fea2f54c15d04fd0fc16633951c58598580
workflow-type: tm+mt
source-wordcount: '1013'
ht-degree: 4%

---

# Adobe Journey Optimizer中的AI功能{#section-overview}

Adobe Journey Optimizer運用人工智慧和機器學習的力量，轉變您建立、最佳化和提供客戶體驗的方式。 從跨管道產生個人化內容到預測與客戶互動的最佳時間，AI功能都能簡化您的工作流程並發揮最大影響力。 本節探討AI支援的功能如何搭配運作，協助您做出更聰明的決策、自動化複雜的工作，並建立真正能引起觀眾共鳴的體驗。 無論您是使用創作AI進行內容建立、使用預測模型做出決策，還是最佳化傳送時間以獲得更好的參與，您都能發現實用的工具和策略，以充分發揮AI在客戶歷程協調中的潛力。

## AI支援的功能

:::: landing-cards-container
:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg)

用於內容產生的 AI 助理

利用創作AI在電子郵件、簡訊、推播通知、網頁和登入頁面間建立並個人化內容。

[探索AI助理](ai-assistant-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg)

傳送時間最佳化

使用人工智慧來預測傳送訊息的最佳時間，並根據歷史行為最大化客戶參與。

[瞭解傳送時間最佳化](../using/building-journeys/send-time-optimization.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg)

用於決策的AI模型

建立自動最佳化和個人化最佳化模型，以便為客戶提供排名和最佳優惠方案。

[探索AI模型](ai-models-landing-page.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/book.svg)

AI助理產品知識

使用對話式AI取得有關Adobe Journey Optimizer的即時答案和營運深入分析。

[使用 AI 助理](../using/start/ai-assistant.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg)

使用AI進行內容實驗

產生多個內容變體並執行實驗，找出適合您對象的最佳執行內容。

[瞭解AI實驗](../using/content-management/generative-experimentation.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/puzzle-piece.svg)

Customer AI整合

與Adobe智慧型服務整合，以預測客戶行為並在您的歷程中使用流失和轉換分數。

[探索智慧型服務](../using/building-journeys/ai-services-overview.md)
:::

::::


## 其他資源

- **[品牌一致性評分](../using/content-management/brands-score.md)** — 使用AI支援的評分，評估您的AI產生的內容與品牌指引的一致程度。
- **[Experiment Accelerator](../using/content-management/experiment-accelerator-gs.md)** — 利用AI驅動的見解和建議加速您的內容實驗程式。
- **[AI支援的API](../using/configuration/ajo-apis.md)** — 透過API以程式設計方式存取Journey Optimizer的AI和機器學習功能。

## 常見問題

+++**使用AI功能需要哪些許可權？**

若要使用AI助理來產生內容，使用者必須被授予&#x200B;**產生內容**&#x200B;許可權。 此許可權會透過許可權產品中的AI助理資源指派。 若要使用AI助理來獲取產品知識和營運見解，使用者必須同意Adobe Experience Cloud Generative AI使用者指南。

[進一步瞭解許可權](../using/administration/ootb-permissions.md)

+++

+++**哪些頻道支援AI助理產生內容？**

產生內容的AI助理可用於&#x200B;**電子郵件**、**推播**、**簡訊**&#x200B;和&#x200B;**網頁**&#x200B;頻道。 目前不適用於直接郵件、內容卡、LINE或WhatsApp頻道。

+++

+++**使用AI助理的最佳實務是什麼？**

- **使用定義良好的提示** — 產生的內容品質受到您的行銷目標與提示的強烈影響。 明確無誤。
- **上傳品牌資產** — 提供PDF、JPEG、PNG或ZIP格式的品牌資產（最多50MB），以取得準確的品牌內內容。
- **使用自訂範本** — 利用最多8至10個影像的品牌特定電子郵件範本，以獲得最佳結果。
- **提供意見回饋** — 使用縮圖向上、向下或標幟圖示報告有問題的輸出，以協助調整模型。
- **每一代僅能利用一個品牌資產** — 雖然您可以上傳多個資產，但每個特定世代僅能使用一個。

[深入瞭解AI Assistant護欄](../using/content-management/gs-generative.md#generative-guardrails)

+++

+++**傳送時間最佳化的最佳實務是什麼？**

- **等待30天** — 在啟用傳送時間最佳化之前使用電子郵件和推播動作至少30天，以確保足夠的資料收集。
- **選擇最佳等待時間** — 設定介於6到24小時之間的最大等待時間，以獲得最佳結果。 較短的持續時間會限制最佳化潛力；較長的持續時間可能會導致訊息過時。
- **針對正確的量度最佳化** — 對於電子郵件，針對驅動動作時的點按次數或資訊內容的開啟次數最佳化。 推送訊息一律會針對開啟次數進行最佳化。
- **避免傳送對時間敏感的訊息** — 請勿將傳送時間最佳化用於緊急作業訊息，例如訂單確認、密碼重設或航班通知。 最適合行銷通訊，例如促銷活動和電子報。
- **排程早上傳送以進行推播** — 為避免夜間通知，請排程在早上傳送時間較短的批次推播（例如，上午9點傳送及8小時的等候時間）。

[深入瞭解傳送時間最佳化](../using/building-journeys/send-time-optimization.md)

+++

+++**傳送時間最佳化的限制有哪些？**

- **管道** — 僅適用於歷程中的電子郵件和推播通知管道。 無法用於Campaigns或透過自訂動作。
- **可用性** — 必須由Adobe客戶服務或您的Adobe代表啟用。
- **訓練期間** — 至少需要30天的歷史電子郵件或推播資料才能使用。
- **模型訓練** — 模型最初每週使用過去16週的資料進行訓練，然後每月重新訓練。
- **探索與最佳化** - 5%的訊息會接收隨機探索傳送時間；95%會接收最佳化的傳送時間。

+++

+++**在Decisioning中AI模型有哪些限制？**

- **最大AI模型** — 每個組織最多5個AI排名模型。
- **資料集需求** — 對於自動最佳化模型，在過去14天內，至少2個選件必須具有100個以上的顯示事件和5個以上的點按事件。
- **意見反應事件** — 必須以體驗事件的形式傳送；不會在Journey Optimizer頻道中自動收集。
- **API限制** — 自動最佳化模型不適用於批次決策API （僅限決策管理）。

[深入了解 AI 模型](../using/experience-decisioning/ranking/ai-models.md)

+++

+++**哪些護欄適用於AI支援的決策？**

| 元件 | 限制 |
|-----------|-------|
| AI排名模型 | 每個組織5個 |
| 決策請求(以Edge分段為基礎的程式碼) | 每秒 1,500 個 |
| 決策請求(程式碼型，不含Edge分段) | 每秒 5,000 個 |
| 項目集合 | 總計10,000 |
| 每個集合的優惠方案專案 | 500 |
| 每個決定原則的選擇策略 | 10 |
| 依決定原則傳回的優惠專案 | 30 |
| 適用性規則+排名公式 | 10,000個組合 |
| 每個規則的設定檔屬性 | 25 |
| 每個規則的內容資料屬性 | 30 |

[進一步瞭解Decisioning護欄](../using/experience-decisioning/decisioning-guardrails.md)

+++

+++**要使用AI功能，我是否需要同意任何條款？**

是，您必須先同意[Adobe Experience Cloud Generative AI使用者指南](https://www.adobe.com/tw/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html)，才能在Journey Optimizer中使用AI小幫手。 如需詳細資訊，請聯絡您的Adobe代表。 此外，Adobe也將Content Credentials套用至Firefly產生的資產，作為承諾產生式AI使用透明度的一部分。

+++

+++**AI產生的內容是否一律正確？**

不可以。 產生式AI內容不一定都是準確的。 請務必檢閱AI產生的輸出是否準確，並確保其適合您的使用案例。 使用提供的評等工具分享意見，以協助工程師調整模型。

+++

