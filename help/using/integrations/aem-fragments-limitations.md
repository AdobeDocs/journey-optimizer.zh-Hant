---
solution: Journey Optimizer
product: journey optimizer
title: Adobe Experience Manager內容片段考量事項和疑難排解
description: Journey Optimizer中AEM內容片段的考量事項和常見問題。
topic: Content Management
role: User
level: Beginner
source-git-commit: 4f7e36a6cc19e4138e867950e34c5a5e6452b364
workflow-type: tm+mt
source-wordcount: '733'
ht-degree: 0%

---

# 考量事項和疑難排解 {#aem-fragments-limitations}

## 主要考量事項 {#considerations}

在[!DNL Adobe Experience Manager]中使用[!DNL Journey Optimizer]的內容片段時，請記住下列事項：

* **內容片段型別**
   * 支援簡單內容片段、巢狀內容片段和&#x200B;**內容片段變數**。 當您在[!DNL Journey Optimizer]中插入片段時，請選擇變數。 如果您未選取變數，則會使用&#x200B;**主要**&#x200B;變數（片段在[!DNL Adobe Experience Manager]中的主要內容）。

* **多語言內容**
   * 必須在[!DNL Adobe Experience Manager]中編寫、標籤和發佈每個變數。 在[!DNL Journey Optimizer]中，選取符合每個訊息語言或地區設定的片段變數。
   * 沒有自動的語言解析或變數之間的遞補。

* **存放庫存取權**
   * [!DNL Journey Optimizer]僅與[!DNL Adobe Experience Manager] **發佈**&#x200B;層（網站、內容片段）整合。 內容片段可透過公開、未驗證的端點使用。
   * 存放庫選擇器中可能會顯示作者存放庫，但只有發佈至&#x200B;**發佈**&#x200B;的片段才能在[!DNL Journey Optimizer]中使用。

* **內容片段狀態**
   * 片段可以顯示&#x200B;**[!UICONTROL 已發佈]**&#x200B;或&#x200B;**[!UICONTROL 已修改]**&#x200B;狀態；[!DNL Journey Optimizer]一律使用&#x200B;**最新發佈的版本**。
   * 在[!DNL Journey Optimizer]中重新發佈片段之前，發佈後所做的變更不會反映在[!DNL Adobe Experience Manager]中。 這兩個產品之間沒有自動版本調解。

* **個人化**
   * 支援：設定檔屬性、內容屬性、靜態字串和預先宣告的變數。
   * 不支援：衍生或計算屬性。

* **更新與版本設定**
   * 更新需要從[!DNL Adobe Experience Manager]手動重新發佈。 沒有自動版本調解。
   * 在[!DNL Adobe Experience Manager]中發佈或重新發佈內容片段時，[!DNL Journey Optimizer]會更新該片段，並重新整理&#x200B;**在作用中行銷活動或歷程中參考之該片段的所有變數**。
   * [!DNL Adobe Experience Manager] [發佈動作](https://experienceleague.adobe.com/zh-hant/docs/experience-manager-cloud-service/content/assets/manage/manage-publication)可能延遲。 完成時，[!DNL Journey Optimizer]會收到事件並重新整理內容。
   * 成功更新後，單一歷程的變更通常會在約&#x200B;**5分鐘**&#x200B;內提供，批次使用案例的變更通常會在約&#x200B;**下一個批次**&#x200B;內提供。

* **快取和校樣**
   * 片段首次新增至行銷活動或歷程時，[!DNL Journey Optimizer]會快取它。 如果您透過&#x200B;**[!UICONTROL 開啟AEM CF選取器]**&#x200B;選取已在其他地方使用的片段，則會從[!DNL Journey Optimizer]快取載入該片段。
   * 當您在[!DNL Adobe Experience Manager]中重新發佈修改的片段後，[!DNL Journey Optimizer]會接聽該事件並更新快取。
   * 校訂一律會反映&#x200B;**最近發佈的**&#x200B;版本；您無法鎖定歷史版本以進行校訂。

## 疑難排解 {#troubleshooting}

如果您在Journey Optimizer中使用Adobe Experience Manager內容片段時遇到問題，請參閱下列常見問題和解決方案：

| 問題 | 原因 | 解決方法 |
|-|-|-|
| **找不到標籤**&#x200B;或選擇器中看不到&#x200B;**內容片段** | Adobe Experience Manager標籤語法不符合必要的格式`ajo-enabled:{OrgId}/{SandboxName}` | 驗證標籤ID是否使用正確的&#x200B;**組織識別碼**&#x200B;和&#x200B;**沙箱名稱**。 請確定沒有空格或不正確的分隔符號。 更正標籤後重新發佈內容片段。 |
| **內容片段未出現在清單**&#x200B;中 | 內容片段處於草稿狀態或未發佈 | Journey Optimizer選擇器中只會顯示已核准和已發佈的內容片段。 在Adobe Experience Manager中發佈內容片段並確保其擁有已發佈狀態。 |
| **變數未定義錯誤** | Personalization預留位置未在片段協助程式標籤中宣告 | 在片段Helper標籤中新增所有必要引數。 內容片段中使用的每個預留位置都必須透過其對應明確宣告。 |
| **校訂顯示未預期的內容** | 校訂使用最新發佈的Adobe Experience Manager版本 | 校樣一律反映Adobe Experience Manager中內容片段的最新出版物。 如果您最近在Adobe Experience Manager中進行了變更，請重新發佈片段並重新整理您的校訂。 |
| **拒絕存取(CPES)錯誤** | 使用者角色無權存取某些屬性 | 請聯絡您的系統管理員，以確認您的角色具有個人化中所使用之設定檔或內容屬性的適當許可權。 |
| **片段顯示空白或遺漏內容** | 缺少必要的個人化引數或遞補值 | 請確定已提供所有必要引數，並考慮為選用屬性新增遞補值。 |
| **影像未演算或似乎已損毀** | 內容片段中的影像URL為相對路徑，或無法從頻道存取 | 影像欄位使用&#x200B;**絕對** URL (`https://...`)。 不支援來自Adobe Experience Manager的相對路徑。 在瀏覽器或訊息預覽中確認URL。 |
| **Experience League AEM連結傳回404** | 過時的書籤、預覽建置或未發佈的AEM說明頁面 | 從即時Experience Manager檔案中開啟[具有Adobe Journey Optimizer的內容片段](https://experienceleague.adobe.com/zh-hant/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/content-fragments-with-journey-optimizer){target="_blank"}主題，並從頁面上的目錄導覽，或搜尋區段名稱（例如&#x200B;**Dispatcher設定**）。 |

如果問題仍然存在，請聯絡您的Adobe代表，提供有關您的內容片段ID、行銷活動或歷程ID的詳細資訊，以及任何顯示的錯誤訊息。
