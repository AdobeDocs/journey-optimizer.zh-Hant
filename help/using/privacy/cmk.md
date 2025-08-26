---
solution: Journey Optimizer
product: journey optimizer
title: 客戶託管金鑰
description: 了解如何在 Adobe Journey Optimizer 設定和管理客戶金鑰
feature: Privacy, Monitoring
role: Developer, User, Admin, Leader
level: Intermediate
exl-id: f0985d1f-0bcf-452f-bd46-dfeca0424f01
source-git-commit: f9e1ae68fcfb9ecc12e0b80a067ca29186fc01f7
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 100%

---

# 設定和管理客戶託管金鑰 {#cmk}

>[!AVAILABILITY]
>
>[!DNL Customer Managed Keys]目前僅適用於已購買 [Healthcare Shield 或 Privacy &amp; Security Shield](https://experienceleague.adobe.com/docs/events/customer-data-management-voices-recordings/governance/healthcare-shield.html?lang=zh-Hant){target="_blank"} 附加產品的組織。

透過 Adobe Journey Optimizer，[Healthcare Shield](https://www.adobe.com/trust/compliance/hipaa-ready.html){target="_blank"} 與 Privacy &amp; Security Shield 客戶能運用 Azure 客戶託管金鑰 (CMK)，並將該金鑰套用至其資料。

Journey Optimizer 的設定流程包含兩個部分，運用 Adobe Experience Platform 與 Customer Journey Analytics (CJA) 的技術：

* 請依照 [Adobe Experience Platform 中的客戶託管金鑰](https://experienceleague.adobe.com/docs/experience-platform/landing/governance-privacy-security/customer-managed-keys.html?lang=zh-Hant){target="_blank"}文件中所述的步驟進行。
* 請依照 [Customer Journey Analytics 中的客戶託管金鑰](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-privacy/cmk.html?lang=zh-Hant){target="_blank"}文件中所述的步驟進行。

  即使您尚未購買 Customer Journey Analytics (CJA)，也必須完成此設定流程，因為會在背景中使用某些 CJA 元件。

若要逐步進行設定流程，請參閱 [Adobe Experience Platform 中的客戶託管金鑰](https://experienceleague.adobe.com/docs/experience-platform/landing/governance-privacy-security/encryption.html?lang=zh-Hant){target="_blank"}文件中的逐步詳細指示。

Adobe Experience Platform 與客戶託管金鑰會在傳輸和存放時將資料加密，確保資料的安全性。 無論是否使用客戶託管金鑰，您的資料都會受到保護。

如需在 Adobe Experience Platform 進行資料加密的詳細資訊，請參閱資料加密[文件](https://experienceleague.adobe.com/docs/experience-platform/landing/governance-privacy-security/encryption.html?lang=zh-Hant){target="_blank"}。
