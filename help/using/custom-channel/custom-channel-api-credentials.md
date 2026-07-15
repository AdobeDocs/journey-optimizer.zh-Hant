---
title: 管理自訂通道的API認證
description: 瞭解如何在Adobe Journey Optimizer中管理自訂管道的API認證。
feature: Channel Configuration
topic: Content Management
role: Admin
level: Experienced
badge: label="有限可用性" type="Informative"
source-git-commit: 94ca2d9458152fb471e9590d053c4729a4a5134f
workflow-type: tm+mt
source-wordcount: '228'
ht-degree: 4%

---


# 管理API認證 {#api-credentials}

當使用非&#x200B;**None**&#x200B;的驗證型別建立自訂管道時，啟動管道時會自動產生初始API認證集。

您可以從&#x200B;**[!UICONTROL 管理]** > **[!UICONTROL 管道]** > **[!UICONTROL 管道產生器]** > **[!UICONTROL API認證]**&#x200B;檢視、管理和編輯認證。

![API認證](assets/custom_channel_api_credentials.png){width="100%"}

對相同管道擁有多個認證可讓您將不同的驗證值附加到不同的管道設定 — 例如，針對不同品牌或使用案例 — 而不複製管道定義。

若要編輯現有的認證集，請按一下詳細目錄清單中的專案。 所有欄位都可以編輯。

若要為相同管道建立其他認證，請遵循以下步驟。

1. 從&#x200B;**[!UICONTROL API認證]**&#x200B;清單，按一下&#x200B;**[!UICONTROL 建立API認證]**。

1. 提供名稱和說明。

   ![建立API認證](assets/custom_channel_create_api_credentials.png){width="100%"}

1. 選取您要建立認證的&#x200B;**[!UICONTROL 管道]**。

   >[!NOTE]
   >
   >下拉式清單中只會顯示驗證型別為&#x200B;**無**&#x200B;以外的已啟動自訂管道。

1. 從清單中選取&#x200B;**[!UICONTROL 驗證型別]**。
1. 填寫驗證專用欄位：
   * **[!UICONTROL API金鑰]** — 提供金鑰名稱、值和位置（查詢引數或標頭）。
   * **[!UICONTROL 基本驗證]** — 提供使用者名稱和密碼。
   * **[!UICONTROL OAuth 2.0]** — 設定OAuth 2.0驗證的裝載。
1. 按一下「**[!UICONTROL 儲存]**」。

## 後續步驟 {#next-steps}

* [委派子網域](custom-channel-subdomains.md) （選用 — 需要連結追蹤）
* [建立管道設定](custom-channel-configuration.md)
