---
solution: Journey Optimizer
product: journey optimizer
title: 關於整合的常見問題
description: 關於訊息中外部資料和內容的Journey Optimizer整合的常見問題集。
feature: Integrations
topic: Content Management
role: User
level: Intermediate
keywords: 整合，常見問題集，外部資料，個人化
hide: true
source-git-commit: e4c298fb1c47501920a27a93b43878327b6c5861
workflow-type: tm+mt
source-wordcount: '892'
ht-degree: 2%

---

# 關於整合的常見問題 {#vendor-integration-faq}

>[!BEGINSHADEBOX]

目錄：

* [使用整合](integrations.md)
* [開始使用廠商整合](vendor-integration-gs.md)
* [可用的廠商](vendor-integration.md)
* **[常見問題集](vendor-integration-faq.md)**

>[!ENDSHADEBOX]

以下是有關Adobe Journey Optimizer中&#x200B;**整合**&#x200B;的常見問題。


## 開始使用

+++ Journey Optimizer中的整合有什麼功能？

它將外部資料來源連線至Journey Optimizer，因此您可以將來自協力廠商系統的內容和資料提取至您的行銷活動和歷程中，並使用該資料個人化訊息。

➡️ [進一步瞭解整合概述](integrations.md)

+++

+++ 誰會設定整合，以及誰會在內容中使用整合？

管理員建立並啟用技術設定（**[!UICONTROL 設定]** > **[!UICONTROL 整合]** > **[!UICONTROL 管理]** > **[!UICONTROL 建立整合]**）。 行銷人員在文字或HTML元件中使用&#x200B;**[!UICONTROL 新增個人化]**、開啟&#x200B;**[!UICONTROL 整合]**、選擇使用中的整合，以及對應屬性。

➡️ [進一步瞭解管理員和行銷人員工作流程](integrations.md)

+++

+++ 我該如何以管理員身分在UI中建立或管理整合？

前往左側功能表中的&#x200B;**[!UICONTROL 組態]**&#x200B;區段，從&#x200B;**[!UICONTROL 整合]**&#x200B;卡片開啟&#x200B;**[!UICONTROL 管理]**，然後選取&#x200B;**[!UICONTROL 建立整合]**。

➡️ [進一步瞭解如何建立整合](integrations.md#configure)

+++

+++ 整合的常見使用案例為何？

例如，忠誠度系統的獎勵積分、產品價格資訊、推薦引擎的建議以及傳遞狀態等物流更新。

➡️ [進一步瞭解來自協力廠商系統的範例資料](integrations.md)

➡️ [進一步瞭解廠商整合範例](vendor-integration.md)

+++

## 設定

+++ 我該如何以管理員身分設定高層級的整合？

您提供名稱和說明、API端點URL （可選擇包含路徑變數）、路徑範本值、**[!UICONTROL GET]**&#x200B;或&#x200B;**[!UICONTROL POST]**、選用的標頭和查詢引數、驗證方法、原則設定（例如逾時和選用的快取或重試）、對應欄位的範例JSON回應，然後執行&#x200B;**[!UICONTROL 傳送測試連線]**&#x200B;並在有效時執行&#x200B;**[!UICONTROL 啟用]**。

➡️ [進一步瞭解整合設定](integrations.md#configure)

+++

+++ 支援哪些驗證型別？

這些驗證型別可供使用： **[!UICONTROL 無驗證]**、**[!UICONTROL API金鑰]**、**[!UICONTROL 基本驗證]**&#x200B;和&#x200B;**[!UICONTROL OAuth 2.0]** （在適用情況下，具有OAuth的承載設定）。

➡️ [進一步瞭解驗證型別](integrations.md#configure)

+++

+++ 回應裝載步驟的功能為何？

貼上JSON回應範例，讓系統可偵測資料型別，且您可以選擇哪些欄位可公開供訊息中的個人化使用。 您可以限制行銷人員在編寫期間可以使用哪些欄位。

➡️ [進一步瞭解回應裝載對應](integrations.md#configure)

+++

+++ 行銷人員如何將整合新增至訊息？

在行銷活動或歷程內容中，在文字或HTML元件上使用&#x200B;**[!UICONTROL 新增個人化]**，前往&#x200B;**[!UICONTROL 整合]**，選取整合，然後儲存。 使用個人化編輯器中的Pills模式，您可以將值對應至設定中的變數（例如URL中的標頭或查詢引數或路徑變數）。

➡️ [進一步瞭解整合的個人化](integrations.md#personalization)

+++

## 功能與使用案例

+++ 我可以在歷程與行銷活動中使用整合嗎？

可以。 在目前產品限制內，此功能可用於&#x200B;**傳出**&#x200B;管道（例如電子郵件、簡訊和推播）的歷程和行銷活動。

➡️ [進一步瞭解歷程與行銷活動](integrations.md#limitations)

+++

+++ 我可以在可重複使用的片段中使用整合嗎？

整合功能在片段中&#x200B;**不支援**。 在產品支援的行銷活動和歷程訊息內容中使用整合。

➡️ [進一步瞭解片段和Beta版限制](integrations.md#limitations)

+++

## 限制

+++ 哪些管道支援整合？

支援&#x200B;**傳出**&#x200B;管道（例如電子郵件、簡訊和推播）。

➡️ [進一步瞭解支援的頻道](integrations.md#limitations)

+++

+++ 支援哪些API回應格式？

對於API呼叫回應，欄位對應支援&#x200B;**JSON**。 此工作流程無法使用非JSON的原始二進位影像輸出和格式。

➡️ [進一步瞭解JSON和回應格式](integrations.md#limitations)

+++

+++ 我可以連線到哪些API模式？

支援目標為特定內容的&#x200B;**擷取** API。 此整合模型不支援&#x200B;**清單** API （廣泛清單或分頁模式）。

➡️ [進一步瞭解擷取與列出API](integrations.md#limitations)

+++

## 許可權和相關功能

+++ 設定整合需要哪些許可權？

組態是&#x200B;**[!UICONTROL 組態]** > **[!UICONTROL 整合]**&#x200B;下的管理員工作流程。 確切的許可權名稱取決於貴組織的Admin Console和Journey Optimizer產品設定檔。 請向您的管理員或Adobe代表確認。

➡️ [進一步瞭解整合的設定位置](integrations.md#configure)

+++

+++ 整合是否會取代Experience Platform來源的Adobe Journey Optimizer聯結器？

不會。 **整合**&#x200B;適用於您從API驅動之訊息內容中的個人化欄位。 **來源**&#x200B;和其他資料擷取功能有不同的用途（例如批次資料擷取和設定檔擴充）。 將每項功能用於其預期範圍。

➡️ [深入瞭解整合的功能](integrations.md)

➡️ [進一步瞭解Experience Platform來源](https://experienceleague.adobe.com/docs/experience-platform/sources/home.html?lang=zh-Hant){target="_blank"}

+++

## 疑難排解

+++ 為何測試連線失敗或持續無效？

驗證端點URL、HTTP方法、路徑範本、標頭和查詢引數、驗證以及原則逾時。 調整後使用&#x200B;**[!UICONTROL 傳送測試連線]**。 針對裝載問題，請確定範例反映有效的JSON，且所選欄位符合API傳回的內容。

➡️ [進一步瞭解測試連線和裝載驗證](integrations.md#configure)

+++

+++ 為什麼行銷人員在選擇器中看不到我的整合？

整合必須在成功測試後&#x200B;**啟動**。 當行銷人員開啟&#x200B;**[!UICONTROL 整合]**&#x200B;時，只會顯示作用中的整合。 如果整合仍為草稿或非使用中，請先完成啟用。

➡️ [進一步瞭解測試連線和啟用](integrations.md#configure)

+++

## 第三方廠商

+++ 有哪些廠商範例可用，以及誰負責保護API？

您可以與任何公開相容API端點的協力廠商平台整合。 **說明性**&#x200B;廠商模式和設定範例可協助您建立相容API的模型。 保護端點的責任在於協力廠商平台和您的團隊。

➡️ [進一步瞭解廠商整合程式](vendor-integration.md)

+++
