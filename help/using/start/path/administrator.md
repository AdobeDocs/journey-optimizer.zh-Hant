---
title: Journey Optimizer系統管理入門
description: 作為系統管理員，瞭解如何與Journey Optimizer合作
level: Intermediate
exl-id: 24f85ced-aa45-493f-b2c4-7c7b58351b38
source-git-commit: 40c42303b8013c1d9f4dd214ab1acbec2942e094
workflow-type: tm+mt
source-wordcount: '705'
ht-degree: 2%

---

# 系統管理員入門 {#get-started-sys-admins}

![管理員](assets/do-not-localize/user-2.png)

開始使用前 [!DNL Adobe Journey Optimizer]，準備環境需要幾個步驟。  必須執行這些步驟， [資料工程師](data-engineer.md) 和 [行程練習者](marketer.md) 可以開始使用 [!DNL Adobe Journey Optimizer]。


作為 **系統管理員**&#x200B;你需要 **瞭解產品配置檔案並分配權限** 用於沙盒管理和通道配置。 您還需要設定沙盒，並管理它們以獲取可用的產品配置檔案。 然後，您將能夠將團隊成員分配給產品配置檔案。

這些功能可由 **[!UICONTROL Product administrators]** 可以訪問管理控制台。 [瞭解有關Adobe Admin Console的詳細資訊](https://helpx.adobe.com/tw/enterprise/admin-guide.html){target=&quot;_blank&quot;}。

瞭解以下頁面中的訪問管理：

1. **建立沙箱** 將實例分區到獨立的虛擬環境。 **沙箱** 建立於 [!DNL Journey Optimizer]。 在 [沙箱](../../administration/sandboxes.md) 的子菜單。

   >[!NOTE]
   >作為 **系統管理員**，則 **[!UICONTROL Sandboxes]** 菜單 [!DNL Journey Optimizer]，更新您在 [Admin Console](https://adminconsole.adobe.com/){_blank}。 瞭解如何在中更新產品配置檔案 [此頁](../../administration/permissions.md#edit-product-profile)。

1. **瞭解產品配置檔案**。 產品配置檔案是一組單一權限，允許用戶訪問介面中的某些功能或對象。 在 [現成產品配置檔案](../../administration/ootb-product-profiles.md) 的子菜單。

1. **設定權限** 用於產品配置檔案，包括 **沙箱**，並通過將團隊成員分配給不同的產品配置檔案來授予他們訪問權限。 此步驟在 [Admin Console](https://adminconsole.adobe.com/){_blank}。 權限是唯一權限，允許您定義分配給 **[!UICONTROL Product profile]**。 每個權限都在功能（如旅程、消息或優惠）下收集，這些功能表示中的不同功能或對象 [!DNL Journey Optimizer]。 在 [權限級別](../../administration/high-low-permissions.md) 的子菜單。

此外，您必須將需要訪問Assets Essentials的用戶添加到 **Assets Essentials消費者用戶** 或 **Assets Essentials用戶** 產品配置檔案。 [閱讀Assets Essentials文檔中的更多內容](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/deploy-administer.html){target=&quot;_blank&quot;}。

>[!NOTE]
>對於2022年1月6日之前獲得的Journey Optimizer產品，必須部署 [!DNL Adobe Experience Manager Assets Essentials] 為您的組織。 在 [部署Assets Essentials](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/deploy-administer.html){target=&quot;_blank&quot;}部分。

訪問 [!DNL Journey Optimizer] 您首次配置了生產沙盒並根據合同分配了特定數量的IP。

要能夠建立您的行程和發送消息，請訪問 **管理** 的子菜單。 瀏覽 **[!UICONTROL Channels]** 的子菜單。

>[!NOTE]
>作為 **系統管理員**，則 **[!UICONTROL Channels]** 菜單 [!DNL Journey Optimizer]，更新您在 [Admin Console](https://adminconsole.adobe.com/){_blank}。 瞭解如何在中更新產品配置檔案 [此頁](../../administration/permissions.md#edit-product-profile)。

按照以下步驟操作：

1. **配置消息和通道**:定義預設、調整和自定義電子郵件和推送消息設定

   * 定義 **推送通知設定** 同時 [!DNL Adobe Experience Platform] 和 [!DNL Adobe Experience Platform Launch]。 [了解更多](../../configuration/push-gs.md)

   * 建立 **消息預設** 配置電子郵件和推送通知消息所需的所有技術參數。 [了解更多](../../configuration/message-presets.md)

   * 管理天數 **重試** 在將電子郵件地址發送到禁止顯示清單之前執行。 [了解更多](../../configuration/manage-suppression-list.md)

1. **委託子域**:對於在Journey Optimizer使用的任何新子域，第一步是將其委派。 [了解更多](../../configuration/about-subdomain-delegation.md)

   ![](../assets/subdomain.png)

1. **建立IP池**:通過將隨實例配置的IP地址組合在一起，提高電子郵件的可傳遞性和信譽。 [了解更多](../../configuration/ip-pools.md)

   ![](../assets/ip-pool.png)

1. **管理禁止顯示和允許清單**:通過抑制和允許清單提高交付能力

   * A [隱藏清單](../../reports/suppression-list.md) 包含您要從交貨中排除的電子郵件地址，因為發送到這些聯繫人可能會損害您的發送信譽和交貨率。 您可以監視在途中自動被排除在發送之外的所有電子郵件地址，如無效地址、始終軟反彈的地址，以及可能對您的電子郵件信譽產生負面影響的地址，以及針對您的某封郵件發出某種垃圾郵件投訴的收件人。 瞭解如何管理 [隱藏清單](../../configuration/manage-suppression-list.md) 和 [重試](../../configuration/retries.md)。
   ![](../assets/suppression-list-filtering-example.png)

   * 的 [允許的清單](../../reports/allow-list.md) 允許您指定單個電子郵件地址或域，這些地址或域將是唯一有權接收您從特定沙箱發送的電子郵件的收件人或域。 這可以防止您在測試環境中意外地將電子郵件發送到真實的客戶地址。 瞭解如何 [啟用允許的清單](../../reports/allow-list.md)。
   瞭解有關中的可交付性管理的詳細資訊 [!DNL Adobe Journey Optimizer] [此頁](../../reports/deliverability.md)。
