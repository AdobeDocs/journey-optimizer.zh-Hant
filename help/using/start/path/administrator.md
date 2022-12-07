---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer 系統管理員快速入門
description: 作為系統管理員，深入瞭解如何使用 Journey Optimizer
level: Intermediate
exl-id: 24f85ced-aa45-493f-b2c4-7c7b58351b38
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '732'
ht-degree: 100%

---

# 系統管理員快速入門 {#get-started-sys-admins}

開始使用 [!DNL Adobe Journey Optimizer] 之前，準備環境需執行數個步驟。  您必須執行這些步驟，[資料工程師](data-engineer.md)和[歷程實務人員](marketer.md)才能開始使用[!DNL Adobe Journey Optimizer]。


作為&#x200B;**系統管理員**，您需要&#x200B;**了解產品設定檔並指派權限**&#x200B;用於沙箱管理和通道設定。 您也需要設定沙箱，並針對可用的產品設定檔進行管理。 然後，您便能將團隊成員指派至產品設定檔。

這些權限可由具有 Admin Console 存取權限的&#x200B;**[!UICONTROL 產品系統管理員]**&#x200B;加以管理。[進一步瞭解 Adobe Admin Console](https://helpx.adobe.com/tw/enterprise/admin-guide.html){target=&quot;_blank&quot;}。

請前往下列頁面，了解存取管理：

1. **建立沙箱**&#x200B;以將執行個體分區到獨立的虛擬環境中。 在[!DNL Journey Optimizer]中建立的&#x200B;**沙箱**。在[沙箱](../../administration/sandboxes.md)一節中了解更多資訊。

   >[!NOTE]
   >作為&#x200B;**系統管理員**，如果您在[!DNL Journey Optimizer]中看不到&#x200B;**[!UICONTROL 沙箱]**&#x200B;功能表，請在 [Admin Console](https://adminconsole.adobe.com/){_blank} 更新您的權限。 在[本頁](../../administration/permissions.md#edit-product-profile)了解如何更新您的產品設定檔。

1. **了解產品設定檔**。產品設定檔是一組統一權限，可讓使用者存取介面中的特定功能或物件。 在[現成可用的產品設定檔](../../administration/ootb-product-profiles.md)區段中了解更多。

1. 針對產品設定檔&#x200B;**設定權限**，包括&#x200B;**沙箱**，並將團隊成員指派至不同的產品設定檔，以授予其存取權。 此步驟會在 [Admin Console](https://adminconsole.adobe.com/){_blank} 中完成。 權限是統一權限，允許您定義分配至&#x200B;**[!UICONTROL 產品設定檔]**&#x200B;的授權。每個權限都是透過功能 (例如歷程或優惠) 收集而得，這些功能代表 [!DNL Journey Optimizer] 中的不同功能或物件。在[權限層級](../../administration/high-low-permissions.md)一節中了解更多 。

此外，您必須將需要存取 Assets Essentials 的使用者新增至 **Assets Essentials 消費者使用者**&#x200B;或/和 **Assets Essentials 使用者**&#x200B;產品設定檔。 [如需詳細資訊，請參閱 Assets Essentials 檔案](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/deploy-administer.html?lang=zh-Hant){target=&quot;_blank&quot;}。

>[!NOTE]
>針對 2022 年 1 月 6 日之前取得的 Journey Optimizer 產品，您必須為貴組織部署 [!DNL Adobe Experience Manager Assets Essentials] 。 在[部署 Assets Essentials](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/deploy-administer.html){target=&quot;_blank&quot;} 一節中了解更多。

首次存取 [!DNL Journey Optimizer] 系統時，會佈建生產沙箱，並根據您的合約分配特定數量的 IP。

若要建立您的歷程並傳送訊息，請存取&#x200B;**系統管理**&#x200B;功能表。 瀏覽&#x200B;**[!UICONTROL 管道]**&#x200B;功能表來設定訊息和通道表面 (即訊息預設集)。

>[!NOTE]
>作為&#x200B;**系統管理員**，如果您在 [!DNL Journey Optimizer] 中看不到&#x200B;**[!UICONTROL 管道]**&#x200B;功能表，請在 [Admin Console](https://adminconsole.adobe.com/){_blank} 中更新您的權限。 在[本頁](../../administration/permissions.md#edit-product-profile)了解如何更新您的產品設定檔。

請遵循以下步驟：

1. **設定訊息和通道**&#x200B;定義介面、調整和自訂電子郵件、簡訊和推播訊息設定

   * 在 [!DNL Adobe Experience Platform] 和 [!DNL Adobe Experience Platform Launch] 中定義&#x200B;**推播通知設定**[了解更多](../../push/push-gs.md)

   * 建立&#x200B;**通道表面** (即訊息預設集)，以設定電子郵件、簡訊和推播通知所需的所有技術參數。 [了解更多](../../configuration/channel-surfaces.md)

   * 設定 **SMS 通道**&#x200B;來設定簡訊所需的所有技術參數。 [了解更多](../../sms/sms-configuration.md)

   * 管理將電子郵件地址傳送至隱藏清單前執行&#x200B;**重試**&#x200B;的天數。[了解更多](../../configuration/manage-suppression-list.md)

1. **委派子網域**：若要在 Journey Optimizer 中使用任何新子網域，第一步是將其委派。 [了解更多](../../configuration/about-subdomain-delegation.md)

   ![](../assets/subdomain.png)

1. **建立 IP 集區**：將與您執行個體佈建的 IP 位址分組，以改善電子郵件傳遞能力和信譽。 [了解更多](../../configuration/ip-pools.md)

   ![](../assets/ip-pool.png)

1. **管理隱藏和允許的清單**：透過隱藏和允許清單改善您的傳遞能力

   * [隱藏清單](../../reports/suppression-list.md)包含您要從傳送中排除的電子郵件地址，因為傳送給這些聯絡人可能會損害您的傳送信譽和傳送率。 您可以監控自動排除而無法傳送歷程的所有電子郵件地址，例如無效地址、持續暫時性退信且可能對電子郵件信譽造成負面影響的地址，以及對您的其中一封電子郵件發出某種垃圾郵件投訴的收件者。 了解如何管理[隱藏清單](../../configuration/manage-suppression-list.md)和[重試](../../configuration/retries.md)。
   ![](../assets/suppression-list-filtering-example.png)

   * 此[允許清單](../../configuration/allow-list.md)可讓您指定個別電子郵件地址或網域，這些地址或網域將是唯一獲授權接收您從特定沙箱傳送之電子郵件的收件者或網域。 此舉可防止您在測試環境中意外傳送電子郵件至真實的客戶地址。 了解如何[啟用允許的清單](../../configuration/allow-list.md)。
   在[此頁面](../../reports/deliverability.md)進一步瞭解 [!DNL Adobe Journey Optimizer] 中的傳遞管理。
