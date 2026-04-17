---
solution: Journey Optimizer
product: journey optimizer
title: 使用MCP使用者端(Beta)
description: 瞭解如何使用MCP伺服器將Adobe Journey Optimizer連線至MCP使用者端
feature: Integrations
topic: Content Management, Artificial Intelligence
badge: label="Beta" type="Informative"
role: User, Developer
level: Beginner, Intermediate
hide: true
source-git-commit: aebdc15b5ca46a2aa623c8c245f00c74a43c9bb2
workflow-type: tm+mt
source-wordcount: '1300'
ht-degree: 1%

---

# 使用MCP使用者端(Beta) {#ajo-mcp}

>[!CAUTION]
>
>**Beta檔案通知：**&#x200B;此檔案涵蓋Beta功能，不構成最終檔案。 此處描述的內容與Beta版本有關，且在正式發行前可能會有所變更。 Adobe不對本檔案的完整性或準確性發表任何宣告。
>
>藉由使用Adobe Journey Optimizer MCP Server (Beta) (「Beta」)，您在此確認Beta係依&#x200B;**「原樣」提供，並無任何保固**。 Adobe沒有義務維護、更正、更新、變更、修改或以其他方式支援Beta。 建議您謹慎使用，切勿依賴這類Beta及/或隨附資料的正確運作或效能。 Beta視為Adobe的機密資訊。 任何「意見回饋」（有關Beta的資訊，包括但不限於您在使用Beta時遇到的問題或缺陷、建議、改進和建議）會在此指派給Adobe，包括所有權利、標題，以及對此等意見回饋的興趣。

[!DNL Adobe Journey Optimizer] MCP整合可讓您使用純語言提示來查詢行銷活動和優惠方案，而不需撰寫API呼叫或導覽產品熒幕。 此頁面說明整合的運作方式、您可以執行哪些操作，以及如何開始使用。

>[!AVAILABILITY]
>
>[!DNL Adobe Journey Optimizer] MCP伺服器目前只能在&#x200B;**Claude Web**&#x200B;和&#x200B;**Claude Desktop**&#x200B;中使用。 未來版本將新增對其他MCP相容應用程式的支援。

## 什麼是模型內容通訊協定？ {#mcp-overview}

行銷和客戶體驗團隊越來越仰賴聊天式應用程式和開發人員工具（例如Anthropic Claude、OpenAI ChatGPT、Cursor和Microsoft Copilot Studio）來簡化日常工作。 這些應用程式支援&#x200B;**模型內容通訊協定(MCP)**，這是開放標準，可讓應用程式以統一的方式將後端工具公開給大型語言模型(LLM)。

[!DNL Adobe Journey Optimizer]現在提供MCP伺服器，直接在任何MCP相容應用程式中呈現行銷活動、忠誠度和沙箱作業。 透過[!DNL Adobe Journey Optimizer] MCP整合，不同的角色可以圍繞相同的協調流程資料共同作業，而不需要針對[!DNL Adobe Journey Optimizer] REST API撰寫查詢，或導覽多個UI熒幕。 客戶可以用對話方式描述他們的意圖，讓LLM叫用適當的MCP工具。

## 主要功能 {#mcp-capabilities}

[!DNL Adobe Journey Optimizer] MCP伺服器可讓您直接從AI助理檢查、摘要和疑難排解行銷活動和選件。 所有作業都是&#x200B;**唯讀** — MCP伺服器介面會擷取API作為純語言回答，因此您可以：

<!--* **Understand journey logic** — Get a human-readable summary of any journey's branching, conditions, and actions.-->
* **立即取得行銷活動可見度** — 以簡單語言詢問行銷活動狀態和管道設定，並立即取得解答，無需瀏覽功能表或手動提取報告。
* **提早發現問題** — 表面停止行銷活動、孤立草稿，以及您提出要求的頻道設定問題，讓您的團隊可以快速採取行動。
* **圍繞即時資料共同作業** — 行銷人員、行銷活動經理和利害關係人可以透過其AI助理查詢相同的即時[!DNL Adobe Journey Optimizer]資料，更輕鬆地保持一致、決定和移動。
* **稽核您的協調流程產品組合** — 檢閱行銷活動的完整狀態，而不剖析JSON或跨產品畫面跳躍。

## 可用的工具 {#mcp-tools}

[!DNL Adobe Journey Optimizer] MCP伺服器公開下列工具：

| 工具 | 說明 |
|---|---|
| **列出行銷活動** | 瀏覽您的[!DNL Adobe Journey Optimizer]行銷活動。 支援依狀態篩選（草稿、即時、已停止、已完成）。 |
| **取得行銷活動** | 依ID擷取特定行銷活動的完整詳細資料和設定，包括對象目標定位、排程、頻道和內容設定。 |
| **列出頻道設定** | 檢視電子郵件、簡訊、推播或WhatsApp頻道的表面預設集和品牌設定。 |

>[!NOTE]
>
>所有工具均為唯讀。 目前的Beta版本不支援寫入操作（建立、更新或刪除物件）。

## 使用案例 {#mcp-use-cases}

下列範例顯示如何使用自然語言與[!DNL Adobe Journey Optimizer] MCP伺服器互動：

| 目標 | 範例提示 |
|---|---|
| **行銷活動概覽** | 「顯示所有AJO行銷活動」/「在AJO中設定了多少行銷活動？」 |
| **狀態稽核** | 「哪些行銷活動目前處於上線狀態？」 / 「列出任何暫停或停止的行銷活動。」 |
| **行銷活動詳細資料** | 「取得行銷活動[ID]的完整詳細資料」/「逐步說明行銷活動[ID]中設定的所有專案」。 |
| **對象和目標** | 「行銷活動[ID]的目標對象為何？」 / 「促銷活動[ID]上設定了哪些適用性規則？」 |
| **排程與時間** | 「行銷活動[ID]何時排定執行？」 / 「促銷活動[ID]是單次傳送還是週期性？」 |
| **疑難排解** | 「為什麼行銷活動[ID]不會傳送？」 /「檢閱行銷活動[ID]的設定是否有任何問題。」 |
| **管道設定** | 「我的沙箱中有哪些管道預設集可用？」 / 「顯示我所有的電子郵件通道設定。」 |
| **管道稽核** | 「哪些管道設定遺漏或不完整？」 / 「我跨所有管道有多少管道設定？」 |

## 先決條件 {#mcp-prerequisites}

在將[!DNL Adobe Journey Optimizer] MCP伺服器連線到您的MCP使用者端之前，請確定下列事項：

* 您有使用中的[!DNL Adobe Journey Optimizer]授權。
* 您可以存取支援的MCP相容應用程式（目前為Claude Web或Claude Desktop）。
* 您在[!DNL Adobe Journey Optimizer]中擁有檢視行銷活動和優惠方案的必要許可權。

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

## 已知限制(Beta) {#mcp-limitations}

下列限制適用於[!DNL Adobe Journey Optimizer] MCP伺服器的目前Beta版本：

| 限制 | 說明 | 因應措施 |
|---|---|---|
| **沒有參與或績效量度** | MCP伺服器不會公開任何報表資料。 工具不會傳回曝光數、點進率、轉換或傳遞統計資料。 | 針對量度使用AJO報表UI、CJA MCP或Adobe Analytics MCP。 AEP Query Service可使用行銷活動執行ID查詢原始事件資料。 |
| **行銷活動清單分頁受到限制** | `List Campaigns`一律會傳回結果的第一頁（最多50個行銷活動，按字母排序）。 未套用位移和限制值，因此完整列舉對於大型沙箱而言是不切實際的。 | 如果行銷活動ID或名稱已知，請直接使用`Get Campaign`。 使用AJO UI來瀏覽和篩選完整清單。 |
| **沒有依日期、頻道或排程的伺服器端篩選** | `List Campaigns`僅支援依狀態篩選。 伺服器端無法使用依發佈日期、排程日期、頻道或促銷活動型別篩選。 | 使用AJO UI行銷活動清單，此清單支援原生日期和管道篩選。 |
| **無法擷取訊息內容** | 訊息內容工具會為所有頻道型別（電子郵件、程式碼型和其他型別）傳回HTTP 502。 訊息HTML、主旨行、個人化權杖和選件內容無法透過MCP擷取。 | 直接在AJO UI中的&#x200B;**行銷活動> [行銷活動] >內容**&#x200B;下檢視訊息內容和個人化權杖。 |

## 常見問題 {#mcp-faq}

+++支援哪些MCP使用者端？

[!DNL Adobe Journey Optimizer] MCP伺服器目前可用於&#x200B;**Claude Web**&#x200B;和&#x200B;**Claude Desktop**。 未來版本可能會新增對其他MCP相容應用程式的支援。
+++

+++我可以透過MCP存取哪些[!DNL Adobe Journey Optimizer]物件？

您可以存取行銷活動、優惠方案、忠誠度資料和沙箱資訊。 操作是唯讀的（擷取API）；目前版本不支援寫入操作。
+++

+++我需要開發人員存取權才能使用[!DNL Adobe Journey Optimizer] MCP伺服器嗎？

不可以。 MCP伺服器是專為行銷和技術人員所設計。 行銷人員可以在任何支援的MCP使用者端中使用自然語言提示與其互動，而開發人員也可以在支援MCP的開發人員工具中使用它。
+++

+++我的資料是否傳送給MCP使用者端提供者？

當您提交提示時，MCP使用者端可能會傳送相關內容（包括MCP伺服器傳回的[!DNL Adobe Journey Optimizer]資料）到其模型以進行處理。 在連線到生產資料之前，請檢閱MCP使用者端提供者的隱私權和資料處理原則。
+++

+++我在[!DNL Adobe Journey Optimizer]中需要哪些許可權？

您要查詢的物件（促銷活動或優惠方案）至少需要&#x200B;**檢視**&#x200B;許可權。 不需要寫入許可權，因為MCP伺服器只會執行讀取作業。 如果您不確定目前的存取層級，請連絡您的[!DNL Adobe Journey Optimizer]系統管理員。
+++

+++我可以在沙箱環境中使用MCP伺服器嗎？

可以。 MCP伺服器遵循您的[!DNL Adobe Journey Optimizer]沙箱設定。 您可以在提示中指定沙箱，或使用限定於特定沙箱的憑證連線，以查詢沙箱專屬的資料。
+++

