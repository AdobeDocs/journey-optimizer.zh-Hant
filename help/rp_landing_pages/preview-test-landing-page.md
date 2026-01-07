---
solution: Journey Optimizer
product: Journey Optimizer
title: 預覽與測試內容
description: 啟動前驗證訊息的準確性。 使用測試設定檔預覽個人化內容、傳送校樣給利害關係人、檢查跨使用者端的電子郵件呈現、評估垃圾郵件分數，並有效測試多個內容變異。
redpen-status: CREATED_||_2025-08-11_20-30-05
exl-id: bd78e0af-573b-4880-a9f1-44467c9db159
source-git-commit: 6b83b015dfd74da9eb58bd06958d0963d81c6489
workflow-type: tm+mt
source-wordcount: '657'
ht-degree: 23%

---

# 預覽與測試內容{#section-overview}

>[!BEGINSHADEBOX]

**用途：**&#x200B;行銷活動和歷程的啟動前驗證工具\
**主要使用者：**&#x200B;行銷活動管理員、電子郵件行銷人員、內容建立者\
**主要結果：**&#x200B;客戶傳遞前發生Catch錯誤

>[!ENDSHADEBOX]

在錯誤到達客戶之前即抓取錯誤，確保無懈可擊的訊息傳送。 預覽內容會驗證不同客戶設定檔中的個人化準確性，而測試工具會顯示可能影響參與度的轉譯問題、垃圾郵件風險和內容變數。 存取向利害關係人傳送校樣的全面功能、使用範例資料模擬個人化、檢查跨使用者端的電子郵件呈現，以及評估傳遞能力量度 — 所有這些都在啟動之前。 掌握這些驗證技術以保護品牌聲譽、最大化收件匣放置並持續提供卓越的客戶體驗。

## 預覽與測試內容

:::: landing-cards-container
:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg?lang=zh-Hant)

如何預覽和測試您的內容

了解如何使用測試輪廓和範例輸入資料來預覽和測試內容、傳送校樣並確保個人化準確性。

[開始預覽和測試](../using/content-management/preview-test.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/list-check.svg?lang=zh-Hant)

如何選取測試設定檔

探索如何選取和管理測試輪廓，以有效預覽和測試個人化內容。

[了解如何選取測試輪廓。](../using/content-management/test-profiles.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg?lang=zh-Hant)

使用測試輪廓來預覽您的內容

使用測試輪廓和模擬內容變化版本來預覽個人化內容的逐步指南。

[使用測試輪廓模擬內容](../using/content-management/preview.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/envelope.svg?lang=zh-Hant)

使用測試輪廓資料，傳送校樣

使用測試輪廓資料傳送校樣以確保內容準確性，進而測試及驗證您的電子郵件訊息。

[了解如何傳送校樣](../using/content-management/proofs.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/eye.svg?lang=zh-Hant)

如何使用Litmus測試電子郵件呈現

整合 Litmus 以預覽常見電子郵件用戶端之間的電子郵件轉譯，並確保正確顯示。

[使用 Litmus 測試電子郵件轉譯](../using/content-management/rendering.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg?lang=zh-Hant)

如何模擬和測試內容變異

使用範例輸入資料來模擬內容變化版本，以測試個人化內容並確保準確性。

[模擬內容變化版本](../using/test-approve/simulate-sample-input.md)
:::

::::

## 快速決策指南

**內容：**&#x200B;此表格會將測試目標對應至Adobe Journey Optimizer中的特定工具。

根據您的目標選擇測試方法：

| **如果您需要……** | **使用此工具** |
|----------------------|-------------------|
| 驗證個人化是否正確顯示 | [測試輪廓](../using/content-management/test-profiles.md) |
| 快速測試10種以上的內容變數 | [範例輸入資料](../using/test-approve/simulate-sample-input.md) |
| 傳送前先取得利害關係人的核准 | [傳送校樣](../using/content-management/proofs.md) |
| 檢查Gmail、Outlook、Apple Mail之間的電子郵件顯示 | [Litmus演算](../using/content-management/rendering.md) |
| 改善收件匣位置 | [垃圾郵件報告](../using/content-management/spam-report.md) |
| 一次預覽所有變數 | [預覽模式](../using/content-management/preview.md) |

## 測試工作流程檢查清單

**內容：**&#x200B;適用於所有管道（電子郵件、簡訊、推播、網頁、應用程式內）的建議五步驟測試順序。

請依照下列順序進行完整驗證：

1. **預覽** — 使用測試設定檔以正確檢查個人化轉譯
2. **測試變數** — 上傳範例資料CSV/JSON以驗證多個案例
3. **檢查傳遞能力** （電子郵件） — 執行垃圾郵件報告和呈現測試
4. **傳送校樣** — 與利害關係人共用以進行檢閱和核准
5. **最終檢查** — 驗證所有連結、影像和CTA是否正常運作

**Pro提示：**&#x200B;測試包含至少3個代表不同客戶區段（高值、新增、非作用中）的設定檔，以捕捉邊緣案例。

## 常見案例

**內容：**&#x200B;實際範例，說明如何在典型使用案例中套用測試工具。

**案例1：測試多區段行銷活動的個人化電子郵件**
→使用[範例輸入資料](../using/test-approve/simulate-sample-input.md)測試20-30個變數，而不建立個別的測試設定檔。 上傳具有不同客戶屬性的CSV一次進行預覽。

**案例2：主要傳送前驗證電子郵件呈現**
→執行[Litmus測試](../using/content-management/rendering.md)以檢查主要電子郵件使用者端的顯示情形，然後檢查[垃圾郵件報告](../using/content-management/spam-report.md)以確保收件匣的位置。

**案例3：取得利害關係人的簽核**
→[傳送校樣](../using/content-management/proofs.md)給內部檢閱者，其中包含測試設定檔資料，以便他們能確切看到客戶將收到的內容。

## 重要技巧

- **測試設定檔**&#x200B;對於預覽個人化內容至關重要；請使用範例輸入資料來有效測試10個以上的變數
- **電子郵件特定工具**&#x200B;包含轉譯測試(Litmus)、垃圾郵件報告和校樣
- **建議的順序：**&#x200B;預覽→測試變數→檢查傳遞能力→傳送校樣→最終檢查
- **省時：**&#x200B;上傳具有客戶屬性的CSV/JSON，而非建立個別的測試設定檔

## 其他資源

- **[如何使用電子郵件垃圾郵件報告](../using/content-management/spam-report.md)** — 使用垃圾郵件報告功能評估電子郵件內容的垃圾郵件分數，以改善傳遞能力。

**相關主題：** [測試並核准登陸頁面](test-landing-page.md) | [核准工作流程](approve-landing-page.md) | [正在建立測試設定檔](../using/audience/creating-test-profiles.md)
