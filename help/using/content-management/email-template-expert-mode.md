---
solution: Journey Optimizer
product: journey optimizer
title: 使用進階HTML編輯器編輯電子郵件範本
description: 使用專家模式在WYSIWYG編輯器中檢視和編輯電子郵件內容的HTML來源，包含功能標幟控制、護欄和儲存驗證。
feature: Templates
topic: Content Management
role: User
hidefromtoc: true
hide: true
level: Experienced
exl-id: 0c586565-0c65-435f-986d-cd08b59de159
source-git-commit: 76bb202375cdfe1c8abacc1670ba6e794175215d
workflow-type: tm+mt
source-wordcount: '495'
ht-degree: 5%

---

# 使用進階HTML編輯器編輯電子郵件範本 {#email-template-expert-mode}

>[!AVAILABILITY]
>
>此功能為有限可用性。請聯絡您的 Adobe 代表以取得存取權。

**進階HTML編輯器**&#x200B;是專家模式，可讓您直接從[!DNL Journey Optimizer]電子郵件Designer介面檢視及編輯電子郵件內容範本的原始原始程式碼。

此功能可讓您直接在來源中插入進階運算式（例如條件）。 當您切換回視覺（案頭）檢視時，內容會重新呈現，因此您可以檢查內容外觀，並繼續在任一檢視中進行編輯。

>[!NOTE]
>
>此功能僅適用於內容範本和電子郵件頻道。

## 護欄 {#guardrails}

當您使用進階HTML編輯器時，系統會設定以下護欄來保護內容相容性並設定預期。

* 目前，進階HTML編輯器中有&#x200B;**沒有驗證程式**。 不會檢查語法錯誤和中斷的配置。 儲存前，請務必仔細檢閱您的內容。

* 未來的系統更新可能會還原對預設標籤所做的變更。 請注意&#x200B;**您的變更可能被覆寫**。

* 自訂程式碼和手動變更所造成的問題&#x200B;**無法疑難排解**&#x200B;或由[!DNL Adobe]支援團隊解決。 確保您有內容備份，以備您需要回覆至先前的版本時使用。

* 為確保內容相容性，進階HTML檢視中無法使用&#x200B;**儲存**。 當您準備好儲存變更時，您必須切換回[案頭]檢視。

>[!WARNING]
>
>內容範本中的進階HTML編輯器與電子郵件Designer中的&#x200B;**[!UICONTROL 為您自己的]**&#x200B;模式編碼不同。 在[!UICONTROL 以您自己的]模式編碼，您無法切換回視覺化編輯器 — 一旦您選擇該路徑，您就會停留在僅編碼編輯中。 相較之下，進階HTML編輯器可讓您隨時在HTML檢視和案頭（視覺）檢視之間切換。 [進一步了解程式碼編輯器](../email/code-content.md)

## 切換到進階HTML檢視 {#switch-to-desktop-view}

1. 開啟或建立[電子郵件範本](../content-management/create-content-templates.md)，然後開啟[電子郵件Designer](../email/get-started-email-design.md)以編輯內容。

1. 按一下畫面右上角的&#x200B;**[!UICONTROL HTML]**&#x200B;按鈕。

   ![](assets/email-template-expert-mode-button.png)

1. 第一次開啟進階HTML編輯器時，會顯示警告訊息。 請仔細檢閱，然後按一下[確定] **[!UICONTROL 以繼續。]**&#x200B;[了解更多](#guardrails)

   >[!NOTE]
   >
   >此警告只會在您首次開啟進階HTML編輯器時顯示，並在每月重設。

   ![](assets/email-template-expert-mode-warning.png){zoomable="yes"}

1. 進階HTML編輯器隨即顯示。

   ![](assets/email-template-expert-mode.png)

1. 將所需的變更新增至您的電子郵件內容。

   >[!WARNING]
   >
   >請務必輸入正確的HTML和CSS程式碼，因為沒有語法驗證程式，且[!DNL Adobe]也不提供支援。 [了解更多](#guardrails)

1. 進階HTML檢視中不提供儲存功能。 切換回[案頭]檢視以儲存變更。

   ![](assets/email-template-expert-mode-save.png){zoomable="yes"}

   >[!NOTE]
   >
   >基於內容相容性的理由，內容只能儲存在案頭檢視中。 當您切換檢視時，您的編輯會保留。

1. 進階HTML檢視中不提供內容模擬。 若要模擬您的內容，請切換至案頭檢視。

   ![](assets/email-template-expert-mode-simulate.png){zoomable="yes"}

