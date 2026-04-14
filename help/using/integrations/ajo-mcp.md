---
solution: Journey Optimizer
product: journey optimizer
title: 透過MCP與AI助理合作
description: 瞭解如何使用MCP伺服器將Adobe Journey Optimizer連線至AI助理
feature: Integrations
topic: Content Management, Artificial Intelligence
badge: label="Beta" type="Informative"
role: User, Developer
level: Beginner, Intermediate
hide: true
source-git-commit: 03ac391f57c271416506b1213c4b8da5f06b32d5
workflow-type: tm+mt
source-wordcount: '793'
ht-degree: 1%

---

# 透過MCP與AI助理合作 {#ajo-mcp}

>[!AVAILABILITY]
>
>[!DNL Adobe Journey Optimizer] MCP伺服器目前只能在&#x200B;**Claude Web**&#x200B;和&#x200B;**Claude Desktop**&#x200B;中使用。 未來版本將新增對其他MCP相容應用程式的支援。

[!DNL Adobe Journey Optimizer] MCP整合可讓您使用純語言提示來查詢行銷活動、歷程和優惠方案，而不需要撰寫API呼叫或導覽產品熒幕。 此頁面說明整合的運作方式、您可以執行哪些操作，以及如何開始使用。

## 什麼是模型內容通訊協定？ {#mcp-overview}

行銷和客戶體驗團隊越來越仰賴聊天式應用程式和開發人員工具（例如Anthropic Claude、OpenAI ChatGPT、Cursor和Microsoft Copilot Studio）來簡化日常工作。 這些應用程式支援&#x200B;**模型內容通訊協定(MCP)**，這是開放標準，可讓應用程式以統一的方式將後端工具公開給大型語言模型(LLM)。

[!DNL Adobe Journey Optimizer]現在提供MCP伺服器，直接在任何MCP相容應用程式中呈現行銷活動、歷程、忠誠度和沙箱作業。 透過[!DNL Adobe Journey Optimizer] MCP整合，不同的角色可以圍繞相同的協調流程資料共同作業，而不需要針對[!DNL Adobe Journey Optimizer] REST API撰寫查詢，或導覽多個UI熒幕。 客戶可以用對話方式描述他們的意圖，讓LLM叫用適當的MCP工具。

## 主要功能 {#mcp-capabilities}

[!DNL Adobe Journey Optimizer] MCP伺服器可讓您直接從AI助理檢查、摘要和疑難排解歷程、行銷活動和選件。 所有作業都是&#x200B;**唯讀** — MCP伺服器介面會擷取API作為純語言回答，因此您可以：

* **瞭解歷程邏輯** — 取得任何歷程分支、條件和動作的人類可讀摘要。
* **檢查行銷活動整備** — 識別防止行銷活動發佈的封鎖程式。
* **點狀涵蓋範圍差距** — 檢視哪些頻道涵蓋您的即時歷程和行銷活動，以及哪些頻道存在差距。
* **稽核您的協調流程組合** — 檢閱行銷活動和歷程的完整狀態，而不需要剖析JSON或跨產品畫面跳轉。

## 使用案例 {#mcp-use-cases}

下列範例顯示如何使用自然語言與[!DNL Adobe Journey Optimizer] MCP伺服器互動：

| 目標 | 範例提示 |
|---|---|
| **摘要行銷活動詳細資料** | 「取得行銷活動cmp456並摘要說明對象、排程、狀態和套件。」 |
| **清查與狀態稽核** | 「我們有什麼，處於什麼狀態？ 顯示行銷活動的即時與草稿計數，以及已完成/已停止/已封存的計數。」 |
| **檢查發佈整備** | 「為什麼campaign cmp456尚未準備好發佈？ 給我看看封鎖程式。」 |
| **比較物件** | 「比較行銷活動abc123與xyz789 — 狀態和排程有什麼改變？」 |
| **稽核您的投資組合** | 「所有即時歷程與行銷活動，涵蓋哪些管道，以及差距在哪裡？」 |
| **頻道涵蓋範圍與組合** | 「顯示歷程、行銷活動和優惠方案位置的頻道足跡 — 僅限電子郵件與多頻道、推播/簡訊/應用程式內使用，以及歷程頻道之間的不相符專案。」 |

## 先決條件 {#mcp-prerequisites}

在將[!DNL Adobe Journey Optimizer] MCP伺服器連線到您的AI助理之前，請確定下列事項：

* 您有使用中的[!DNL Adobe Journey Optimizer]授權。
* 您可以存取支援的MCP相容應用程式（目前為Claude Web或Claude Desktop）。
* 您在[!DNL Adobe Journey Optimizer]中擁有檢視行銷活動、歷程和優惠方案的必要許可權。

## 連線[!DNL Adobe Journey Optimizer] MCP伺服器 {#mcp-connect}

>[!NOTE]
>
>這項整合位於Beta中。 當設定步驟全面推出時，將會發佈詳細的設定步驟。 請聯絡您的Adobe代表，要求搶先使用許可權並收到設定指示。

在Beta階段中，您的Adobe代表將提供：

* 貴組織專屬的MCP伺服器端點URL。
* 用於將AI助理連線到[!DNL Adobe Journey Optimizer]的驗證認證。
* 在Claude Desktop或Claude Web中設定MCP伺服器的指南。

<!--
Step-by-step connection instructions to be added here, including:
- How to obtain MCP server credentials from [!DNL Adobe Journey Optimizer]
- How to configure the MCP server in Claude Desktop / Claude Web
- How to authenticate
-->

## 常見問題 {#mcp-faq}

+++支援哪些AI助理？

[!DNL Adobe Journey Optimizer] MCP伺服器目前可用於&#x200B;**Claude Web**&#x200B;和&#x200B;**Claude Desktop**。 未來版本可能會新增對其他MCP相容應用程式的支援。
+++

+++我可以透過MCP存取哪些[!DNL Adobe Journey Optimizer]物件？

您可以存取行銷活動、歷程、優惠方案、忠誠度資料和沙箱資訊。 操作是唯讀的（擷取API）；目前版本不支援寫入操作。
+++

+++我需要開發人員存取權才能使用[!DNL Adobe Journey Optimizer] MCP伺服器嗎？

不可以。 MCP伺服器是專為行銷和技術人員所設計。 行銷人員可以在Claude中使用自然語言提示與其互動，而開發人員也可以在支援MCP的開發人員工具中使用它。
+++

+++我的資料是否傳送給AI助理提供者？

當您提交提示時，AI助理可能會將相關內容（包括MCP伺服器傳回的[!DNL Adobe Journey Optimizer]資料）傳送至其模型以進行處理。 在連線到生產資料之前，請檢閱AI助理提供者的隱私權和資料處理原則。
+++

+++我在[!DNL Adobe Journey Optimizer]中需要哪些許可權？

您要查詢的物件（行銷活動、歷程或選件）至少需要&#x200B;**檢視**&#x200B;許可權。 不需要寫入許可權，因為MCP伺服器只會執行讀取作業。 如果您不確定目前的存取層級，請連絡您的[!DNL Adobe Journey Optimizer]系統管理員。
+++

+++我可以在沙箱環境中使用MCP伺服器嗎？

可以。 MCP伺服器遵循您的[!DNL Adobe Journey Optimizer]沙箱設定。 您可以在提示中指定沙箱，或使用限定於特定沙箱的憑證連線，以查詢沙箱專屬的資料。
+++
