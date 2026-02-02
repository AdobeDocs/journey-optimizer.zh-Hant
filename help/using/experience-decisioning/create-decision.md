---
title: 開始使用決定原則
description: 瞭解如何使用決定原則來傳遞優惠方案。
feature: Decisioning
topic: Integrations
role: User
level: Experienced
exl-id: 63aa1763-2220-4726-a45d-3a3a8b8a55ec
version: Journey Orchestration
source-git-commit: c2388c84346ed9a0409270fd96f3a1458bf8ad88
workflow-type: tm+mt
source-wordcount: '625'
ht-degree: 29%

---

# 開始使用決定原則 {#create-decision}

>[!CONTEXTUALHELP]
>id="ajo_code_based_decision"
>title="什麼是決定？"
>abstract="決定原則包含決策引擎選擇最佳內容的所有選擇邏輯。決定原則是針對行銷活動的。其目標是為每個設定檔選擇最佳產品建議，而行銷活動製作允許您指明如何呈現所選決定項目，包括要在訊息中包含哪些項目屬性。"
>additional-url="https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer/using/decisioning/offer-decisioning/get-started-decision/starting-offer-decisioning" text="關於決策"

>[!CONTEXTUALHELP]
>id="ajo_journey_decision_policy"
>title="定義決策原則"
>abstract="決策原則可讓您從決策引擎中挑選最佳項目，並將其傳遞給合適的客群。"
>additional-url="https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer/using/decisioning/offer-decisioning/get-started-decision/starting-offer-decisioning" text="關於決策"

>[!CONTEXTUALHELP]
>id="ajo_exd_decision_policy"
>title="決策原則"
>abstract="決策原則可讓您先從決策引擎中挑選出最佳項目，再傳遞給所有客群。"

>[!CONTEXTUALHELP]
>id="ajo_exd_placements"
>title="刊登"
>abstract="產品建議放置環境決定從決策引擎傳回的項目出現在訊息中的位置。您可以在報告中追蹤他們在不同產品建議放置環境的效能。"

>[!CONTEXTUALHELP]
>id="ajo_exd_decision_attribute"
>title="從目錄選取決定的屬性"
>abstract="會將決定屬性儲存在目錄的結構描述中。 從選取的目錄中，選取想在此處使用的屬性。"

決策原則是優惠方案的容器，可運用決策引擎以動態方式傳回最佳內容，供每個受眾成員傳送。 其目標是為每個設定檔選取最佳優惠方案，而行銷活動/歷程製作可讓您指示應如何顯示選取的決策專案，包括要包含在訊息中的專案屬性。

>[!AVAILABILITY]
>
>目前，計畫碼型體驗管道的所有客戶都可使用決策政策。 這些變數僅供電子郵件通道使用。 請聯絡您的 Adobe 代表以取得存取權。

## 主要步驟 {#key}

在訊息中運用決定原則的主要步驟如下：

1. [建立決定原則](../experience-decisioning/create-decision-policy.md)

   選擇要傳回的專案數、設定選擇策略、遞補選項和評估順序，在您的訊息中設定決定原則。

1. [在您的內容中使用決定原則](../experience-decisioning/use-decision-policy.md)

   使用決定原則輸出和您要在訊息中顯示的決定專案屬性，個人化您的內容。

1. [建立報告儀表板](cja-reporting.md)

   建立自訂Customer Journey Analytics儀表板，以測量效能並深入瞭解您的決定政策和優惠的提供及參與方式。

## 護欄與限制

* **電子郵件映象頁面** — 目前，決定專案不會在電子郵件映象頁面中呈現。
* **追蹤和連結型別** — 若要追蹤由決定產生的連結，請在結構描述中將其定義為「決定Assets」。 無法追蹤屬性型連結。
* **在電子郵件中巢狀內嵌決定原則** — 您無法在已經有關聯決定原則的父級電子郵件元件中巢狀內嵌多個決定原則。
* **含決策的重複歷程/行銷活動** — 如果您重複包含決策原則的歷程或行銷活動，重複版本會參考原始電子郵件或程式碼型體驗，而造成錯誤。 複製後請一律重新設定決定原則。
* **同意原則** — 同意原則的更新最多需要48小時才會生效。 如果決定原則參考與最近更新的同意原則關聯的屬性，變更將不會立即套用。

  同樣地，如果受同意原則約束的新設定檔屬性新增到決定原則中，這些設定檔屬性將可供使用，但關聯的同意原則在延遲過去後才會執行。

  同意原則僅適用於具有Adobe Healthcare Shield或Privacy and Security Shield附加元件的組織。

* **AI排名** — 目前，使用決策的歷程中的電子郵件管道不支援AI排名。

## 後續步驟 {#next-steps}

現在您已了解決定原則如何運作，以及它們如何協助提供個人化優惠，您已準備好建立您的第一個決定原則。

➡️ [瞭解如何建立決定原則](../experience-decisioning/create-decision-policy.md)

## 作法影片 {#video}

瞭解如何使用Decisioning為受眾個人化電子郵件。

>[!VIDEO](https://video.tv.adobe.com/v/3479221?captions=chi_hant&quality=12)
