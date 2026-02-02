---
title: 開始使用決定原則
description: 瞭解如何使用決定原則來傳遞優惠方案。
feature: Decisioning
topic: Integrations
role: User
level: Experienced
exl-id: 63aa1763-2220-4726-a45d-3a3a8b8a55ec
version: Journey Orchestration
source-git-commit: 083545ff7b2dc5ce45ef3766321fdf12e1b96c5c
workflow-type: tm+mt
source-wordcount: '663'
ht-degree: 27%

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

➡️ [在影片中探索此功能](#video)

## 護欄與限制

* **支援的管道** — 這些管道有決策原則可供使用：程式碼型體驗、直接郵件、電子郵件和推播通知。
* **推送通知SDK需求** — 具有推送通知的Experience Decisioning需要特定版本的Mobile SDK。 在實作此功能之前，請檢查[發行說明](https://developer.adobe.com/client-sdks/home/release-notes/){target="_blank"}以識別所需的版本，並確定您已相應地升級。 您也可以在[本節](https://developer.adobe.com/client-sdks/home/current-sdk-versions/){target="_blank"}中檢視您平台的所有可用SDK版本。
* **電子郵件映象頁面** — 目前，決定專案不會在電子郵件映象頁面中呈現。
* **追蹤和連結型別** — 若要追蹤由決定產生的連結，請在結構描述中將其定義為「決定Assets」。 無法追蹤屬性型連結。
* **在電子郵件中巢狀內嵌決定原則** — 您無法在已經有關聯決定原則的父級電子郵件元件中巢狀內嵌多個決定原則。
* **含決策的重複歷程/行銷活動** — 如果您重複包含決策原則的歷程或行銷活動，重複版本會參考原始電子郵件或程式碼型體驗，而造成錯誤。 複製後請一律重新設定決定原則。
* **同意原則** — 同意原則的更新最多需要48小時才會生效。 如果決定原則參考與最近更新的同意原則關聯的屬性，變更將不會立即套用。

  同樣地，如果受同意原則約束的新設定檔屬性新增到決定原則中，這些設定檔屬性將可供使用，但關聯的同意原則在延遲過去後才會執行。

  同意原則僅適用於具有Adobe Healthcare Shield或Privacy and Security Shield附加元件的組織。

* **AI排名** — 目前，使用決策的歷程中的電子郵件管道不支援AI排名。

* **內容範本** — 內容中設定的任何決定原則將不會儲存在範本中。 如果您將範本套用至其他動作，則需要重新設定原則。

## 主要步驟 {#key}

在訊息中運用決定原則的主要步驟如下：

1. **建立決定原則**

   在訊息中新增決定原則，並設定要傳回的專案數、選擇策略和遞補選項。

   ➡️ [瞭解如何建立決定原則](../experience-decisioning/create-decision-policy.md)

1. **在您的內容中使用決定原則**

   透過插入您要在訊息中顯示的決定專案屬性，使用決定原則輸出個人化您的內容

   ➡️ [瞭解如何在訊息中使用決定原則](../experience-decisioning/create-decision-policy.md)

## 作法影片 {#video}

瞭解如何使用Decisioning為受眾個人化電子郵件。

>[!VIDEO](https://video.tv.adobe.com/v/3479221?captions=chi_hant&quality=12)

瞭解如何使用Decisioning為受眾個人化推播通知。

>[!VIDEO](https://video.tv.adobe.com/v/3479221?captions=chi_hant&quality=12)
