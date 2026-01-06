---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer 系統管理員快速入門
description: 作為系統管理員，深入瞭解如何使用 Journey Optimizer
feature: Get Started
role: Admin
level: Intermediate
exl-id: 24f85ced-aa45-493f-b2c4-7c7b58351b38
source-git-commit: 2d699fe8a3320400dad2d5d962028d6e2a5425f8
workflow-type: ht
source-wordcount: '965'
ht-degree: 100%

---

# 系統管理員快速入門 {#get-started-sys-admins}

您身為&#x200B;**系統管理員**，可以設定 Journey Optimizer 環境、管理存取權，讓團隊更能有效、安全地工作。 您執行必要設定步驟，讓[資料工程師](data-engineer.md)、[開發商](developer.md)和[行銷人員](marketer.md)可以開始使用[!DNL Adobe Journey Optimizer]。

您的主要職責包括設定使用者群組和權限，建立並管理沙箱，以便劃分不同使用者群組的資料和歷程，同時設定傳遞管道、訊息預設集，才能確保有透過 Journey Optimizer 傳遞各種訊息和資產，具備前後一致的品牌形象。您會確保合適的人員擁有合適的能力，同時維護資安和治理。

這些功能可由具有存取權限產品的&#x200B;**[!UICONTROL 產品系統管理員]**&#x200B;加以管理。[進一步了解權限](../../administration/permissions.md){target="_blank"}。

## 設定存取權和權限

請依照下列步驟，設定存取權管理：

1. **建立沙箱**&#x200B;以將執行個體分區到獨立的虛擬環境中。 在[!DNL Journey Optimizer]中建立的&#x200B;**沙箱**。在[沙箱](../../administration/sandboxes.md)一節中了解更多資訊。

   >[!NOTE]
   >作為&#x200B;**系統管理員**，如果您無法在[!DNL Journey Optimizer]中找到&#x200B;**[!UICONTROL 沙箱]**&#x200B;選單，就必須更新您的權限。 請到[本頁面](../../administration/permissions.md#edit-product-profile)了解如何更新您的角色。

1. **了解角色**。 角色是一組統一權限，可讓使用者存取介面中的特定功能或物件。 請到[立即可用的角色](../../administration/ootb-product-profiles.md)區段中了解更多 。

1. 針對角色&#x200B;**設定權限**，包括&#x200B;**沙箱**，並將團隊成員指派至不同的角色，以授予其存取權。 權限是統一權限，允許您定義分配給&#x200B;**[!UICONTROL 角色]**&#x200B;的授權。每個權限都是透過功能 (例如歷程或產品建議) 收集而得，這些功能代表 [!DNL Journey Optimizer] 中的不同功能或物件。在[權限層級](../../administration/high-low-permissions.md)一節中了解更多 。

1. **使用物件層級存取控制** (選填)。 可將存取標籤套用至歷程、行銷活動和頻道設定等物件，以便控制有哪些使用者可以存取特定資源。 深入瞭解[物件層級存取控制(OLAC)](../../administration/object-based-access.md)。

此外，您必須將需要存取 Assets Essentials 的使用者新增至 **Assets Essentials 消費者使用者**&#x200B;或/和 **Assets Essentials 使用者**&#x200B;角色。 [如需詳細資訊，請參閱 Assets Essentials 文件](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/deploy-administer.html?lang=zh-Hant){target="_blank"}。

首次存取 [!DNL Journey Optimizer] 系統時，會佈建生產沙箱，並根據您的合約分配特定數量的 IP。

## 設定頻道和訊息

若想讓[行銷人員](marketer.md)能夠建立、傳送訊息，就請存取&#x200B;**管理**&#x200B;選單。 瀏覽&#x200B;**[!UICONTROL 頻道]**&#x200B;選單，以便設定頻道設定。

>[!NOTE]
>作為&#x200B;**系統管理員**，如果您在 [!DNL Journey Optimizer] 中看不到&#x200B;**[!UICONTROL 頻道]**&#x200B;功能表，請在[權限](../../administration/permissions.md){target="_blank"}產品中更新您的權限。

請依照下列步驟操作：

1. **設定頻道設定。**&#x200B;定義電子郵件、簡訊、推播通知和其他通道所需的所有技術參數：

   * 可在 [!DNL Adobe Experience Platform] 和 Adobe Experience Platform 資料彙集中，定義&#x200B;**推播通知設定**。 [了解更多](../../push/push-gs.md)

   * 建立&#x200B;**頻道設定**，以便設定電子郵件、簡訊、推播、應用程式內、網頁和其他頻道所需的所有技術參數。 [了解更多](../../configuration/channel-surfaces.md)

   * 設定 **SMS 頻道**，即可設定簡訊所需的所有技術參數。 [了解更多](../../sms/sms-configuration.md)

   * 管理將電子郵件地址傳送至禁止名單前執行&#x200B;**重試**&#x200B;的天數。[了解更多](../../configuration/manage-suppression-list.md)

1. **委派子網域**：若要在 Journey Optimizer 中使用任何新子網域，第一步是將其委派。 [了解更多](../../configuration/about-subdomain-delegation.md)

   ![](../assets/subdomain.png)

1. **建立 IP 集區**：將與您執行個體佈建的 IP 位址分組，以改善電子郵件傳遞能力和信譽。 [了解更多](../../configuration/ip-pools.md)

   ![](../assets/ip-pool.png)

1. **管理隱藏和允許的清單**：透過隱藏和允許清單改善您的傳遞能力

   * [禁止名單](../../reports/suppression-list.md)包含您要從傳送中排除的電子郵件地址，因為傳送給這些聯絡人可能會損害您的傳送信譽和傳送率。 您可以監控自動排除而無法傳送歷程的所有電子郵件地址，例如無效地址、持續暫時性退信且可能對電子郵件信譽造成負面影響的地址，以及對您的其中一封電子郵件發出某種垃圾郵件投訴的收件者。 了解如何管理[禁止名單](../../configuration/manage-suppression-list.md)和[重試](../../configuration/retries.md)。

   ![](../assets/suppression-list-filtering-example.png)

   * 此[允許清單](../../configuration/allow-list.md)可讓您指定個別電子郵件地址或網域，這些地址或網域將是唯一獲授權接收您從特定沙箱傳送之電子郵件的收件者或網域。 此舉可防止您在測試環境中意外傳送電子郵件至真實的客戶地址。 了解如何[啟用允許的清單](../../configuration/allow-list.md)。

   請在此頁面](../../reports/deliverability.md)進一步了解[!DNL Adobe Journey Optimizer] [的傳遞能力管理。

## 其他功能

隨著貴組織的需求增加，請考慮下列進階功能：

* **同意原則**：如果您的組織已購買 Healthcare Shield 或 Privacy and Security Shield，請建立同意原則以尊重各管道的客戶偏好。[了解更多](../../action/consent.md)

* **資料治理原則**：套用資料使用標籤和原則來控制如何在行銷動作中使用資料。[了解更多](../../action/action-privacy.md)

* **IP 暖身計劃**：逐步增加電子郵件傳送量，以建立電子郵件提供者的寄件者信譽。[了解更多](../../configuration/ip-warmup-gs.md)

## 跨角色共同作業

您的管理工作可讓所有團隊獲得成功：

>[!BEGINTABS]

>[!TAB 支援資料工程師]

與[資料工程師](data-engineer.md)共同處理資料管理和存取權：

* 授予資料管理和結構描述建立的權限
* 核准沙箱存取權以進行開發和測試
* 協調資料保留原則和治理規則
* 啟用進階功能 (例如聯合客群構成) 的存取權

>[!TAB 支援開發人員]

與[開發人員](developer.md)共同處理 API 存取權與測試：

* 透過 Adobe Developer Console 提供 API 認證
* 設定用於開發和測試的沙箱環境
* 核准管道設定 (推播憑證、簡訊提供者)
* 協調測試環境和部署策略

>[!TAB 支援行銷人員]

與[行銷人員](marketer.md)共同處理權限和管道設定：

* 指派適當的權限以建立歷程和行銷活動
* 設定他們將使用的管道 (電子郵件、推播、簡訊等)
* 支援測試環境和核准工作流程
* 啟用新功能的存取權

>[!ENDTABS]

## 後續步驟

設定環境後：

1. **驗證設定**：確認所有團隊成員都可以存取其必要的功能
2. **監視使用情況**：使用管理儀表板追蹤系統使用情況並識別問題
3. **維持權限**：隨著團隊角色發生變化，定期檢閱和更新權限
