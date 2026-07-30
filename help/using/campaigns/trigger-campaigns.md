---
solution: Journey Optimizer
product: journey optimizer
title: 檢閱及啟動行銷活動
description: 瞭解如何在Journey Optimizer中檢閱及啟用行銷活動
feature: Campaigns
topic: Content Management
role: User
level: Intermediate
keywords: 行銷活動，檢閱，驗證，啟用，啟用，最佳化工具
exl-id: 86f35987-f0b7-406e-9ae6-0e4a2e651610
TQID: https://experienceleague.adobe.com/Q9UQEnAqQNFD869w4lQOQxcbH82SwDZyT8Q-9RvRD5k
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d556b755-390a-43f0-be32-a08cf6236126id: a653cc2e-bc85-4353-a306-399e5b247978
subfeature_v2: id: f7479fa1-474b-479d-8c98-f6cee5865a38id: ee67bd4a-25ee-4cdd-9eab-0d7549fde0c6
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: c1579802-ddd4-4214-8a91-97b2066abe11id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: a5c0537a45acbc708ce62bd05a569630230201ac
workflow-type: tm+mt
source-wordcount: 584
ht-degree: 1%

---

# 執行API觸發的行銷活動 {#execute}

>[!BEGINSHADEBOX]

**在此頁面上：**&#x200B;擷取產生的cURL要求，並使用它透過API觸發您的即時API觸發行銷活動，並附上疑難排解指南，以便您解決傳送延遲和驗證錯誤。

>[!ENDSHADEBOX]

啟動行銷活動後，您需要擷取產生的範例cURL請求，並將其用於API中以建置您的裝載並觸發行銷活動。

## 必讀 {#must-read}

* **行銷活動開始/結束日期** — 如果您在建立行銷活動時已設定特定的開始和/或結束日期，則不會在這些日期之外執行，且API呼叫將會失敗。

* **呼叫逾時** — 對互動式訊息執行REST API的呼叫逾時60秒。 不過，萬一發生未預期的逾時情況，內部會重試以保證傳遞。

## 觸發行銷活動 {#trigger}

1. 開啟行銷活動，然後從&#x200B;**[!UICONTROL cURL請求]**&#x200B;區段複製並貼上裝載請求。 此裝載包含訊息中使用的所有個人化（設定檔和內容）變數。 行銷活動上線後，即可使用此功能。

   ![](assets/api-triggered-curl.png)

   >[!IMPORTANT]
   >
   >cURL區段中的端點在標準和[高輸送量行銷活動](../campaigns/api-triggered-high-throughput.md)之間不同。

1. 將此cURL請求用於API以建置您的裝載並觸發行銷活動。 如需詳細資訊，請參閱[互動式訊息執行API檔案](https://developer.adobe.com/journey-optimizer-apis/references/messaging#tag/execution)，其中列出標準和高輸送量行銷活動的所有端點。

   [此頁面](https://developer.adobe.com/journey-optimizer-apis/references/messaging-samples)上也提供API呼叫範例。

## 疑難排解 {#troubleshooting}

### 電子郵件傳遞延遲 {#delivery-delays}

如果電子郵件傳送時間超過預期，請調查外部服務（例如雲端基礎結構提供者或電子郵件服務提供者）的潛在中斷或效能問題。 Journey Optimizer記錄會記錄訊息離開時間戳記，這有助於判斷傳送管道中是否發生延遲情形。

### Azure cosmos DB驗證錯誤（500內部伺服器錯誤） {#cosmosdb-auth-errors}

如果您在觸發API觸發的行銷活動時遇到&#x200B;**500內部伺服器錯誤**，且系統記錄顯示來自Azure Cosmos DB的&#x200B;**403禁止存取**&#x200B;錯誤，其中包含訊息，例如：

_「對您帳戶的存取權目前已撤銷，因為Azure Cosmos DB服務無法取得帳戶預設身分的AAD驗證Token」_

此錯誤通常發生於Cosmos DB驗證所需的Azure服務主體已停用、刪除或設定錯誤時。

+++如何解決此問題

1. **確認您的Azure服務主體** — 確認您的Azure服務主體或受管理的身分已啟用，且尚未在Azure Active Directory中停用或刪除。

1. **檢查許可權** — 確認服務主體具有存取Azure Key Vault和Cosmos DB資源的必要許可權。 服務主體必須具有適當的角色指派，才能使用Azure Cosmos DB進行驗證。

1. **檢閱Azure Cosmos DB CMK設定** — 如果您使用客戶自控金鑰(CMK)，請參閱[Azure Cosmos DB CMK疑難排解指南](https://learn.microsoft.com/en-us/azure/cosmos-db/cmk-troubleshooting-guide#azure-active-directory-token-acquisition-error){target="_blank"}，以取得還原AAD權杖贏取的詳細步驟。

1. **重新啟用並測試** — 更正設定後，如果服務主體已停用，請重新啟用服務主體，並重新測試您的交易式行銷活動API呼叫，以確認驗證成功且已傳送訊息。

>[!NOTE]
>
>此問題通常是由於Cosmos DB驗證所需的Azure服務主體設定錯誤或意外停用所導致。 將服務主體保持啟用狀態並正確設定將可防止未來發生此錯誤。

+++
