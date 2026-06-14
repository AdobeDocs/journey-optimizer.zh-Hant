---
solution: Journey Optimizer
product: journey optimizer
title: 對 Journey Optimizer 資源的稽核動作
description: 了解如何在 Journey Optimizer 資源上追蹤執行的動作。
feature: Monitoring
role: User
level: Intermediate
exl-id: 759b014a-c834-4331-bffd-5bc159ec555d
TQID: https://experienceleague.adobe.com/Usk3qin9P4IZlKw-gEI4zaKO-aRtaKq9-0GMVlOecjA
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: aeebb91a-f216-4d5f-8da1-3a7e6f696ed0id: bb359667-ec7d-4d4b-8663-5850fc219d32
subfeature_v2: id: a9cf78bf-e9e4-4836-85a5-b6b3cf93bf56id: f365ec33-2b99-4b7f-b4ee-c743dd7f615fid: c8d5f2ce-ba44-43e9-a2bf-94a3d7d85ec3
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dcid: c7d04a2c-412a-4c9d-9d7a-4456eaa5adebid: d095671a-1355-40aa-8b5f-06c33c68080bid: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 4e89993a998268ae2810c949d0669bf6dc458dd6
workflow-type: tm+mt
source-wordcount: 380
ht-degree: 90%

---

# 對 Journey Optimizer 資源的稽核動作 {#track-changes}

>[!BEGINSHADEBOX]

**在此頁面上：**&#x200B;檢閱記錄使用者對Journey Optimizer資源的動作的稽核記錄，以便提高可見度、疑難排解問題，並展示是否符合法規和資料管理政策。

>[!ENDSHADEBOX]

## 關於稽核記錄 {#audit-logs}

>[!IMPORTANT]
>
>若要檢視並匯出稽核記錄，您必須擁有&#x200B;**[!DNL View User Activity Log]**&#x200B;權限。 [了解更多](../administration/ootb-product-profiles.md)

使用 Journey Optimizer，您可以識別系統中的使用者對各種服務和功能（如歷程、訊息、登陸頁面）執行的動作。

這使您能夠提高系統中所執行的活動的可見度，疑難排解問題，並幫助您的企業遵守法規和公司資料管理策略。

每項動作都記錄在可在 Adobe Experience Platform 中存取的「稽核記錄」中的中繼資料。 有關稽核記錄的詳細資訊，包括如何在 UI 或 API 檢視並管理這些記錄，請參閱 [Adobe Experience Platform 文件](https://experienceleague.adobe.com/docs/experience-platform/landing/governance-privacy-security/audit-logs/overview.html?lang=zh-Hant)。

![](assets/audit-logs.png)

## 由稽核記錄擷取的事件類型 {#events}

下表概述稽核記錄的 Journey Optimizer 資源行動。 [Adobe Experience Platform 文件](https://experienceleague.adobe.com/docs/experience-platform/landing/governance-privacy-security/audit-logs/overview.html?lang=zh-Hant#category)提供在稽核記錄中擷取的完整操作清單。

>[!NOTE]
>
>與&#x200B;**決策管理**&#x200B;相關的稽核記錄僅在 CSV 檔案中可見，該檔案可使用&#x200B;**[!UICONTROL 下載記錄]**&#x200B;按鈕下載。

| 資源 | 動作 |
|-----------|------------------|
| AJO 行銷活動 | 建立/刪除/更新/啟動/停止 |
| AJO 管道一般設定 | 建立/刪除/更新 |
| AJO IP 池 | 建立/刪除/更新 |
| AJO 登陸頁面 | 建立/刪除/更新/發佈/取消發佈 |
| AJO 登陸頁面 HTML 範本 | 建立/刪除/更新 |
| AJO 登陸頁面預設集 | 建立/刪除/更新 |
| AJO 登陸頁面子網域 | 建立/刪除/更新 |
| AJO 訊息預設集 | 建立/刪除/更新 |
| AJO PTR 記錄 | 建立/刪除/更新 |
| AJO 儲存的運算式範本 | 建立/刪除/更新 |
| AJO簡訊API 認證 | 建立/刪除/更新 |
| AJO 子網域 | 建立/刪除/更新 |
| AJO 禁止名單 | 建立/刪除/下載 CSV |
| 欄位群組 | 建立/刪除/更新 |
| 歷程 | 建立/刪除/更新/停止/發佈 |
| 歷程自訂動作 | 建立/刪除/更新 |
| 歷程資料來源 | 建立/刪除/更新 |
| 歷程事件 | 建立/刪除/更新 |
| 歷程片段 | 建立/刪除/更新/啟動/封存 |
| 訊息頻率規則 | 建立/刪除/更新 |
| 排名策略 | 建立/刪除/更新 |
