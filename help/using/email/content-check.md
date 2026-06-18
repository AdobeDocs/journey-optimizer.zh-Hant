---
solution: Journey Optimizer
product: journey optimizer
title: 電子郵件Designer中的內容檢查
description: 瞭解如何在Journey Optimizer中傳送電子郵件之前，使用電子郵件Designer中的內容檢查來捕捉HTML和CSS問題。
feature: Email Design
topic: Content Management
role: User
level: Beginner, Intermediate
keywords: 電子郵件，內容檢查， HTML， CSS，驗證，呈現，品質
source-git-commit: 5d21c045ce6b1fd70f2f966c85d364e2fcfb4bb8
workflow-type: tm+mt
source-wordcount: '1014'
ht-degree: 2%

---


# 電子郵件Designer中的內容檢查 {#content-checks}

>[!CONTEXTUALHELP]
>id="ajo_email_content_check"
>title="內容檢查"
>abstract="在傳送之前，先偵測並修正電子郵件中的HTML和CSS問題。 檢查涵蓋不支援的標籤、空白div，以及會在Gmail或Microsoft Outlook中觸發轉譯失敗的大小臨界值。 問題會顯示為錯誤、警告或資訊通知。"

[!DNL Journey Optimizer]包含直接在電子郵件Designer中的自動化技術驗證，可協助您在傳送前捕捉HTML和CSS問題。

結果會在製作面板中顯示為錯誤、警告或資訊性通知，其中包含內容詳細資訊和適用的單鍵修正，因此無需離開電子郵件Designer即可解決問題。

## 存取內容檢查 {#access-content-checks}

電子郵件Designer中一律提供內容檢查。 若要檢視，請按一下右側邊欄中的「問題」圖示，以開啟&#x200B;**[!UICONTROL 內容檢查]**&#x200B;窗格 — 此處列出所有偵測到的問題。

![電子郵件Designer中有問題的內容檢查窗格](assets/content-check.png)

>[!NOTE]
>
>系統會自動針對您電子郵件的目前狀態執行檢查，並在每次編輯後執行。 [了解更多](#recalculation)

檢查會以三個嚴重性層級顯示：

| 嚴重性 | 顏色 | 說明 |
|---|---|---|
| **錯誤** | 紅色 | 會造成傳遞或轉譯失敗的嚴重問題。 傳送前請先解決。 |
| **Warning** | 橙色 | 可能影響特定電子郵件使用者端轉譯的潛在問題。 建議檢閱並解決。 |
| **資訊** | 藍色 | 有關不封鎖傳送但可能影響內容長期可維護性之條件的資訊性通知。 |

未偵測到問題時，窗格會顯示&#x200B;**未偵測到任何問題**，而對應的圖示為綠色。

![電子郵件Designer中的內容檢查窗格沒有問題](assets/content-check-no-issues.png)

視問題而定，您可以檢視更多內容、套用一鍵式修正，或儲存電子郵件以重新整理檢查結果。

* 對於某些偵測到的問題，您可以按一下&#x200B;**[!UICONTROL 顯示詳細資料]**&#x200B;按鈕來檢視更多內容。按一下&#x200B;**[!UICONTROL 隱藏詳細資料]**&#x200B;以摺疊。
  ![電子郵件Designer中的內容檢查窗格，包含詳細資料](assets/content-check-details.png){width="80%"}
* 同樣地，您可以按一下&#x200B;**[!UICONTROL Show fix]**&#x200B;按鈕，並在可用處套用一鍵修正。如果無法自動套用修正，則會顯示訊息，您必須手動解決問題。
  ![電子郵件Designer中的[內容檢查]窗格及[套用]修正按鈕](assets/content-check-fix.png){width="80%"}

### 重新計算支票 {#recalculation}

大部分檢查（例如不支援的HTML元素、空白div和HTML大小）會在您每次編輯電子郵件時重新計算，因此一律會反映您目前的內容。

其他檢查（例如CSS大小）是根據序列化內容（您的電子郵件載入或儲存時的版本）計算，而非根據電子郵件Designer中的即時編輯狀態計算。 在此情況下，儲存的內容可能會與您編輯時看到的內容稍有不同。 如果您不儲存就進行編輯，會出現&#x200B;**[!UICONTROL 過時檢查]**&#x200B;標籤，表示結果可能不再準確。 儲存您的電子郵件以重新整理計算。

![電子郵件Designer中的內容檢查窗格，具有過時的檢查標籤](assets/content-check-stale.png){width="100%"}

## 修正偵測到的問題 {#fix-issues}

下表列出所有可能的訊息，以及每個訊息的建議動作。 展開與您在&#x200B;**[!UICONTROL 內容檢查]**&#x200B;窗格中看到的郵件相符的類別。

+++ 不支援的HTML元素

| 訊息 | 嚴重性 | 該做什麼 |
|---|---|---|
| 您的內容包含`<script>`標籤，任何電子郵件系統都不支援此標籤。 將其移除以避免傳送和轉譯問題。 | 錯誤 | 找出並移除您HTML內容中的所有`<script>`標籤。 |
| 您的內容包含`<base>`標籤，這可能會導致電子郵件Designer中出現連結和資源解析問題。 若要修正，您必須將其移除。 | 錯誤 | 從您的HTML移除`<base>`標籤。 |
| 您的內容包含具有重新整理的HTML中繼標籤，電子郵件Designer不支援此標籤。 將其移除以防止非預期行為。 | 警告 | 從您的HTML中移除meta重新整理標籤。 |
| 您的內容包含空白的div，這可能會導致Microsoft Outlook (MSO)中的版面配置問題。 若要修正此問題，請移除空白的div，並改用同層級元素的間距。 | 警告 | 刪除空的`<div>`元素，並調整周圍元素的邊框間距或邊界，以維持間距。 |

+++

+++ CSS問題

| 訊息 | 嚴重性 | 該做什麼 |
|---|---|---|
| CSS總大小超過Gmail的16 KB限制，將導致Gmail中出現轉譯問題。 | 錯誤 | 使用&#x200B;**[!UICONTROL 套用修正]**&#x200B;自動移除未使用的CSS規則，或手動簡化您的樣式。 |
| CSS大小總計接近Gmail的16 KB限制，若新增更多CSS，可能導致轉譯問題。 | 警告 | 使用&#x200B;**[!UICONTROL 套用修正]**&#x200B;移除未使用的CSS規則，或在新增更多內容之前先減少樣式。 |
| 此片段的CSS總大小超過3 KB。 將此與其他片段合併可能會造成電子郵件CSS總數超過Gmail的16 KB限制，並導致轉譯問題。 | 警告 | 簡化此片段中的CSS，將合併的電子郵件CSS維持在16 KB以下。 |
| 內容包含未使用的CSS規則。 這可能會導致Gmail中出現轉譯問題。 | 警告 | 使用&#x200B;**[!UICONTROL 套用修正]**&#x200B;自動移除參照電子郵件中不再出現之元素的CSS規則。 |

<!--
| Message | Severity | What to do |
|---|---|---|
| Your content has modifications to the system-generated default CSS. These changes may be overridden by future Email Designer updates. To preserve your styles, add them using the Custom CSS feature instead. | Info | Move your custom styles to [Custom CSS](custom-css.md) to ensure they are preserved across Email Designer updates. |
-->

+++

+++ HTML大小

| 訊息 | 嚴重性 | 該做什麼 |
|---|---|---|
| 預估的HTML大小超過Gmail的100 KB限制，將導致Gmail出現轉譯問題。 傳送時的實際HTML大小可能不同。 | 錯誤 | 減少電子郵件內容 — 移除不必要的元素、簡化結構，或將內容分割為多個傳送。 |
| 預估的HTML大小接近Gmail的100 KB限制，如果新增更多HTML，可能會導致轉譯問題。 傳送時的實際HTML大小可能不同。 | 警告 | 先簡化內容，再新增更多內容。 超過Gmail限制的電子郵件將會剪裁給收件者。 |
| 此片段的預計HTML大小超過20 KB。 將此與其他片段合併可能會導致HTML的電子郵件總數超過Gmail的100 KB限制，並導致轉譯問題。 傳送時的實際HTML大小可能不同。 | 警告 | 請減少此片段中的HTML，使合併的電子郵件大小低於Gmail的100 KB限制。 |

+++

## 關於HTML和CSS大小 {#size-estimation}

HTML和CSS大小值是在編寫時計算的&#x200B;**估計值**，並且可能與傳遞給收件者的實際大小不同，例如，當您的電子郵件使用條件式區塊（每個收件者只有一個分支呈現）時，或在傳送時啟用HTML縮制時。

大小警告是主動訊號，可協助您在傳送前最佳化內容，而非硬區塊。
