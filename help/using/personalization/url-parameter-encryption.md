---
solution: Journey Optimizer
product: journey optimizer
title: 加密URL引數
description: 瞭解如何加密敏感的URL查詢引數，以免PII在Journey Optimizer追蹤連結和登入頁面上以純文字顯示。
feature: Personalization
topic: Personalization
role: Admin
level: Intermediate
badge: label="有限可用性" type="Informative"
keywords: 加密， URL，追蹤，登陸頁面，金鑰登入，個人化，安全性，隱私權，沙箱
exl-id: 82e2b6e4-769f-4bdc-b2e2-19352fbaec8e
source-git-commit: 5c8d615b5f6b2c2cb80a21c59f3ea5f12325e6fd
workflow-type: tm+mt
source-wordcount: '693'
ht-degree: 2%

---

# 加密URL引數 {#url-parameter-encryption}

>[!AVAILABILITY]
>
>此功能在「有限可用性」中提供。 請聯絡您的 Adobe 代表以取得存取權。
>
>此功能目前僅適用於電子郵件頻道。

## 為何使用URL引數加密？ {#why-url-parameter-encryption}

個人化追蹤連結和登陸頁面URL通常包含查詢字串中的設定檔屬性、識別碼、權杖或其他值。 這些引數通常會在電子郵件或簡訊中顯示為純文字，而且如果有人複製、共用或書籤該連結，這些引數仍可讀取。 當值可能包含個人識別資訊(PII)或必須保護的其他敏感資料時，就可能帶來安全性和隱私風險。

[!DNL Journey Optimizer]在個人化編輯器中提供加密協助程式，讓您可以在轉譯時加密任何運算式值（例如設定檔屬性、權杖或您從數個欄位建立的字串）。 加密一律需要來自組織登入的機碼。

您只會加密您選擇的查詢引數，使用管理員在沙箱層級登入中管理的金鑰，因此在共用或檢查連結時，機密值不會以純文字顯示。

### 運作方式 {#how-it-works}

* **Administrators**&#x200B;使用金鑰登入，根據貴組織的安全性原則[建立金鑰](#create-keys)和[管理金鑰](#manage-keys)。
* **行銷人員**&#x200B;在個人化編輯器中插入`Encrypt`協助程式，並傳遞要保護的值加上登入中的作用中金鑰識別碼。 如需語法和選項，請參閱[本節](functions/helpers.md#url-parameter-encryption-helper)。

>[!IMPORTANT]
>
>解密是貴組織的責任。 [!DNL Journey Optimizer]會在訊息轉譯時加密值。 您的網站、應用程式或API必須使用您定義的相同密碼編譯材料和程式來解密引數 — 與您的安全性模式一致。

### 範例

登陸頁面URL可能會使用查詢引數，例如`token`，其值為字串權杖（例如具有選件或設定檔識別碼的JSON裝載）。 若未加密，該字串Token會以純文字形式顯示在連結中。 使用加密協助程式包裝該值，會以URL中的加密文字取代敏感裝載，而其餘連結則維持不變。

## 建立金鑰 {#create-keys}

您必須先建立金鑰，才能使用URL引數加密協助程式。 若要執行此操作，請遵循下列步驟。

>[!NOTE]
>
>目前沒有存取和管理金鑰的特定許可權。 授與&#x200B;**[!UICONTROL 管理]**&#x200B;下&#x200B;**[!UICONTROL 組態]**&#x200B;區段存取權的角色也會授與金鑰登入的存取權。 不過，預計會在未來版本中推出特定許可權。

<!--
>[!IMPORTANT]
>
>To access and manage keys, you you must have the **View Key Registry** and **Manage Key Registry** permissions granted. [Learn more](../administration/high-low-permissions.md)
-->

1. 移至&#x200B;**[!UICONTROL 管理]** > **[!UICONTROL 組態]**。

1. 按一下&#x200B;**[!UICONTROL 管理]**&#x200B;按鈕以開啟&#x200B;**[!UICONTROL 機碼登入]**。

   管理功能表中的![機碼登入區段](assets/encryption-key-registry.png){width="80%"}

1. 使用專用按鈕，根據您的組織需要建立金鑰。

   ![在機碼登入區段](assets/encryption-create-key.png){width="80%"}中建立機碼按鈕

1. 指派您的團隊可在個人化編輯器中參考的明確標籤或識別碼給他們。

   ![機碼登入區段](assets/encryption-key-details.png){width="80%"}中的機碼詳細資料

1. 按一下&#x200B;**[!UICONTROL 提交]**&#x200B;以確認您的變更。

建立金鑰之後，行銷人員可以在個人化編輯器中使用[URL引數加密](functions/helpers.md#url-parameter-encryption-helper)協助程式來加密他們放置在URL查詢引數中的特定值。

## 管理金鑰 {#manage-keys}

若要管理金鑰，請遵循下列步驟。

1. 存取&#x200B;**[!UICONTROL 機碼登入]**。 您可以在清單檢視中看到為目前沙箱建立的所有金鑰。

   ![機碼登入清單檢視](assets/encryption-key-registry-list.png){width="100%"}

1. 按一下狀態為&#x200B;**[!UICONTROL 作用中]**&#x200B;的金鑰以開啟金鑰詳細資料。

   ![使用中金鑰詳細資料](assets/encryption-key-active-details.png){width="80%"}

1. 按一下&#x200B;**[!UICONTROL 撤銷]**&#x200B;按鈕，永久停用新加密的金鑰。

   撤銷金鑰後，嘗試在協助程式中使用金鑰應該會在轉譯時失敗。 撤銷的專案仍會顯示在稽核中；您的團隊可能仍需要相應的資料來解密您自己系統上的舊裝載。

1. 按一下&#x200B;**[!UICONTROL 輪換]**&#x200B;按鈕以提供新的金鑰資料，同時保留歷程和行銷活動已參考的穩定金鑰識別碼。

   先前的資料會以撤銷狀態及適當原因（例如輪換時間戳記）保留在登入中，而新的資料列或版本會反映使用中的機碼。

   >[!NOTE]
   >
   >僅應選取作用中金鑰，以在個人化編輯器中加密新值。 請勿將撤銷的金鑰用於新內容。
