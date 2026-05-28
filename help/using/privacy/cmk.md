---
solution: Journey Optimizer
product: journey optimizer
title: 客戶託管金鑰
description: 了解如何在 Adobe Journey Optimizer 設定和管理客戶金鑰
feature: Privacy, Monitoring
role: Developer, User, Admin, Leader
level: Intermediate
exl-id: f0985d1f-0bcf-452f-bd46-dfeca0424f01
TQID: https://experienceleague.adobe.com/yCl5CISD1-Xx6gfcK2sWdFWAeE0LicO-3r3YndB2cVQ
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adebid: d095671a-1355-40aa-8b5f-06c33c68080bid: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
feature_v2: id: aeebb91a-f216-4d5f-8da1-3a7e6f696ed0id: bb359667-ec7d-4d4b-8663-5850fc219d32
subfeature_v2: id: a9cf78bf-e9e4-4836-85a5-b6b3cf93bf56id: f365ec33-2b99-4b7f-b4ee-c743dd7f615fid: c8d5f2ce-ba44-43e9-a2bf-94a3d7d85ec3
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 279
ht-degree: 100%

---

# 設定與管理客戶自控金鑰 {#cmk}

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
