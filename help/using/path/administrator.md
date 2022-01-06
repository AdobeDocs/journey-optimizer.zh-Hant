---
title: Journey Optimizer系統管理員快速入門
description: 身為系統管理員，了解如何使用Journey Optimizer
level: Intermediate
exl-id: 24f85ced-aa45-493f-b2c4-7c7b58351b38
source-git-commit: 168579f8f560756282cb8ae8cb82a10e1227af02
workflow-type: tm+mt
source-wordcount: '705'
ht-degree: 2%

---

# 系統管理員快速入門

![管理員](assets/do-not-localize/user-2.png)

開始使用之前 [!DNL Adobe Journey Optimizer]，準備環境需執行數個步驟。  您必須執行這些步驟，才能 [資料工程師](data-engineer.md) 和 [歷程實踐者](marketer.md) 可以開始使用 [!DNL Adobe Journey Optimizer].


As a **系統管理員**，您需要 **了解產品設定檔並指派權限** 用於沙箱管理和通道設定。 您也需要設定沙箱，並針對可用的產品設定檔進行管理。 然後，您便能將團隊成員指派給產品設定檔。

這些功能可由管理 **[!UICONTROL Product administrators]** 具有Admin Console存取權限。 [深入了解Adobe Admin Console](https://helpx.adobe.com/tw/enterprise/admin-guide.html){target=&quot;_blank&quot;}。

請前往下列頁面，了解存取管理：

1. **建立沙箱** 將實例分區到獨立的虛擬環境中。 **沙箱** 在中建立 [!DNL Journey Optimizer]. 了解更多 [沙箱](../administration/sandboxes.md) 區段。

   >[!NOTE]
   >As a **系統管理員**，如果您看不到 **[!UICONTROL Sandboxes]** 功能表 [!DNL Journey Optimizer]，請在 [Admin Console](https://adminconsole.adobe.com/){_blank}。 了解如何在 [本頁](../administration/permissions.md#edit-product-profile).

1. **了解產品設定檔**. 產品設定檔是一組統一權限，可讓使用者存取介面中的特定功能或物件。 了解更多 [現成可用的產品設定檔](../administration/ootb-product-profiles.md) 區段。

1. **設定權限** 針對產品設定檔，包括 **沙箱**，並將團隊成員指派至不同的產品設定檔，以授予其存取權。 此步驟會在 [Admin Console](https://adminconsole.adobe.com/){_blank}。 權限是統一權限，允許您定義分配給的授權 **[!UICONTROL Product profile]**. 每個權限都是透過功能（例如歷程、訊息或選件）收集，這些功能代表中的不同功能或物件 [!DNL Journey Optimizer]. 了解更多 [權限層級](../administration/high-low-permissions.md) 區段。

此外，您必須將需要存取Assets Essentials的使用者新增至 **Assets Essentials消費者使用者** 或/和 **Assets Essentials使用者** 產品設定檔。 [如需詳細資訊，請參閱Assets Essentials檔案](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/deploy-administer.html){target=&quot;_blank&quot;}。

>[!NOTE]
>針對2022年1月6日之前取得的Journey Optimizer產品，您必須部署 [!DNL Adobe Experience Manager Assets Essentials] 貴組織。 了解更多 [部署Assets Essentials](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/deploy-administer.html){target=&quot;_blank&quot;}區段。

存取 [!DNL Journey Optimizer] 系統會首次布建生產沙箱，並根據您的合約分配特定數量的IP。

若要建立您的歷程並傳送訊息，請存取 **管理** 功能表。 瀏覽 **[!UICONTROL Channels]** 功能表來設定電子郵件訊息和預設集。

>[!NOTE]
>As a **系統管理員**，如果您看不到 **[!UICONTROL Channels]** 功能表 [!DNL Journey Optimizer]，請在 [Admin Console](https://adminconsole.adobe.com/){_blank}。 了解如何在 [本頁](../administration/permissions.md#edit-product-profile).

請遵循下列步驟：

1. **設定訊息和通道**:定義預設集、調整和自訂電子郵件和推播訊息設定

   * 定義 **推播通知設定** 在 [!DNL Adobe Experience Platform] 和 [!DNL Adobe Experience Platform Launch]. [進一步了解](../push-gs.md)

   * 建立 **訊息預設集** 設定電子郵件和推播通知訊息所需的所有技術參數。 [進一步了解](../configuration/message-presets.md)

   * 管理 **重試** 會先執行，再將電子郵件地址傳送至隱藏清單。 [進一步了解](../configuration/manage-suppression-list.md)

1. **委派子網域**:若要在Journey Optimizer中使用任何新子網域，第一步是將其委派。 [進一步了解](../configuration/about-subdomain-delegation.md)

   ![](../assets/subdomain.png)

1. **建立IP池**:將與您執行個體布建的IP位址分組，以改善電子郵件傳遞能力和信譽。 [進一步了解](../configuration/ip-pools.md)

   ![](../assets/ip-pool.png)

1. **管理隱藏和允許的清單**:透過隱藏和允許清單改善您的傳遞能力

   * A [隱藏清單](../suppression-list.md) 包含您要從傳送中排除的電子郵件地址，因為傳送給這些聯絡人可能會損害您的傳送信譽和傳送率。 您可以監控自動排除而無法傳送歷程的所有電子郵件地址，例如無效地址、持續軟退信且可能對電子郵件信譽造成負面影響的地址，以及對您的其中一封電子郵件發出某種垃圾郵件投訴的收件者。 了解如何管理 [隱藏清單](../configuration/manage-suppression-list.md) 和 [重試](../configuration/retries.md).
   ![](../assets/suppression-list-filtering-example.png)

   * 此 [允許清單](../allow-list.md) 可讓您指定個別電子郵件地址或網域，這些地址或網域將是唯一獲授權接收您從特定沙箱傳送之電子郵件的收件者或網域。 這可防止您在測試環境中意外傳送電子郵件至真實的客戶地址。 了解如何 [啟用允許的清單](../allow-list.md).
   深入了解傳遞能力管理，位於 [!DNL Adobe Journey Optimizer] [在本頁](../deliverability.md).
