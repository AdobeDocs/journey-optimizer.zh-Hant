---
title: 直接郵件中的批次決策
description: 使用Experience Decisioning個人化直接郵件擷取檔案，或匯出決策資料以用於下游系統
feature: Decisioning, Direct Mail
topic: Integrations
role: User
level: Intermediate
keywords: 批次決策、直接郵件、決策
source-git-commit: b91d7609df9d05a2ef04dbdbe2a78d9a084f95ac
workflow-type: tm+mt
source-wordcount: '853'
ht-degree: 0%

---


# 直接郵件中的批次決策 {#batch-decisioning-direct-mail}

透過批次決策，決策會為每個設定檔選取一個或幾個最佳決策專案，並將這些結果包含在直接郵件提取檔案中。 設定決定原則時，您可以設定&#x200B;**[!UICONTROL 專案數]**，為每個設定檔傳回多個專案。 匯出的檔案可用於直接郵件個人化，或用於您將設定檔和決定屬性匯出至其他系統的批次使用案例。

直接郵件中的批次決定支援兩個主要使用案例：

* **含決策的直接郵件** — 個人化每個收件者的實體郵件。 例如，使用適用性規則和排名（優先順序或公式），為每個設定檔選擇最佳影像或選件。 擷取檔案包含設定檔資料，以及您直接郵件提供者所選一或多個決策專案的屬性（例如優惠影像URL）。
* **匯出下游系統的批次** — 匯出設定檔及其決策結果（例如，選件ID、屬性）以用於其他系統。 您執行批次決定並將檔案匯出至您的伺服器；下游工具（例如協力廠商電子郵件服務提供者）會將該資料用於其自己的行銷活動或流程。

>[!NOTE]
>
>本頁面著重於搭配直接郵件使用批次決策的特定方面。 如需設定和使用直接郵件通道的完整詳細資訊 — 包括檔案路由、通道設定和擷取檔案設定 — 請參閱[開始使用直接郵件](../direct-mail/get-started-direct-mail.md)和[建立直接郵件訊息](../direct-mail/create-direct-mail.md)。

## 工作流程概觀 {#workflow}

1. **建立直接郵件行銷活動或歷程**：建立歷程或行銷活動、選取&#x200B;**[!UICONTROL 直接郵件]**&#x200B;動作、選擇直接郵件設定並定義對象。

   ➡️ [瞭解如何建立直接郵件訊息](../direct-mail/create-direct-mail.md)

1. **新增決定原則**：

   1. 按一下&#x200B;**[!UICONTROL 編輯內容]**&#x200B;以設定擷取檔案。
   1. 將欄新增至解壓縮檔案，並使用![](assets/do-no-localize/editor-icon.svg)圖示開啟個人化編輯器。

      ![](assets/decision-policy-dm-add.png)

   1. 導覽至&#x200B;**[!UICONTROL 決策]**&#x200B;功能表以建立決策原則。 在原則設定中，若每個設定檔需要多個決定專案，請設定&#x200B;**[!UICONTROL 專案數]**，然後設定選擇策略和選擇性遞補。

      ![](assets/decision-policy-dm-create.png)

   ➡️ [瞭解如何在直接郵件中新增並設定決定原則](create-decision-policy.md#add)

1. **使用決策屬性個人化直接郵件檔案**：對於應包含決策結果的欄，請開啟Personalization編輯器，瀏覽至&#x200B;**[!UICONTROL 決策原則]**，並選取&#x200B;**[!UICONTROL 插入原則]**&#x200B;以新增決策原則的程式碼。

   使用傳回的決策專案屬性，好讓選取的優惠資訊包含在每個設定檔的擷取檔案中。 當傳回多個專案時，請使用原則`#each`回圈，對應您資料行中每個專案的屬性。

   ➡️ [瞭解如何在訊息中使用決定原則 — 直接郵件索引標籤](use-decision-policy.md)

1. 使用具有測試設定檔的&#x200B;**[!UICONTROL 模擬內容]**&#x200B;來預覽匯出的列（包括決策值）。

   ![](assets/batch-decisioning-simulate.png)

   ➡️ [瞭解如何預覽和測試您的內容](../content-management/preview-test.md)

1. 啟動行銷活動或發佈歷程，以產生檔案（CSV或文字分隔）並將其匯出至您設定的伺服器。

   ➡️ [瞭解如何檢閱及啟用行銷活動](../campaigns/review-activate-campaign.md) | [瞭解如何發佈歷程](../building-journeys/publish-journey.md)

## 直接郵件+決策範例 {#example-direct-mail}

範例： fitness retailer會傳送個人化明信片給每位客戶，並附上10個可能影像之一。 他們使用Decisioning為每個設定檔挑選最佳影像。

1. 建立10個決定專案（每個影像一個），每個都具有適用性規則（例如年齡、性別）。
2. 將它們新增至集合，並使用排名方法（例如，手動優先順序或公式）建立選擇策略。
3. 在直接郵件行銷活動或歷程中，啟用決策並新增使用此選擇策略的決策原則。
4. 在擷取檔案中，新增資料為決定專案屬性的欄，該屬性可保留所選影像（例如，選件影像URL）。 其他欄可以是全名、地址、州、zip等。
5. 行銷活動執行時，每個設定檔在匯出中會取得一列，其中包含該設定檔的所選影像。 直接郵件提供者使用此檔案來產生實體郵件。

您可以搭配測試設定檔使用&#x200B;**[!UICONTROL 模擬內容]**，以檢視將針對該設定檔匯出的決策結果（例如影像）。

## 批次匯出（中介軟體）使用案例 {#example-batch-export}

有些客戶會使用批次決定來匯出設定檔及其決定結果，以供其他系統（例如CRM或電子郵件服務提供者）使用。 流程為：

1. 依上述方式設定直接郵件（檔案路由+通道設定）。
2. 建立直接郵件行銷活動或歷程，並新增決定原則。
3. 為設定檔欄位和匯出中所需的決定專案屬性新增欄。
4. 啟動行銷活動。 檔案會匯出至您的伺服器（例如Amazon S3或SFTP）。
5. 您的下游系統擷取檔案，並將設定檔和決定資料用於其自己的行銷活動或程式。

這可透過具有Experience Decisioning的直接郵件通道支援批次決定使用案例。

## 相關檔案 {#related}

* [建立直接郵件訊息](../direct-mail/create-direct-mail.md) — 設定解壓縮檔案並啟用決策
* [建立決定原則](create-decision-policy.md#add) — 在[直接郵件]索引標籤中新增決定原則
* [直接郵件設定](../direct-mail/direct-mail-configuration.md) — 檔案路由和通道設定
* [開始使用決策](gs-experience-decisioning.md) — 概念和護欄
