---
solution: Journey Optimizer
product: journey optimizer
title: 設定WhatsApp頻道
description: 瞭解如何設定您的環境，以使用Journey Optimizer傳送WhatsApp訊息
feature: Whatsapp, Channel Configuration
role: Admin
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta" type="Informative"
exl-id: d1f40cd8-f311-4df6-b401-8858095cef3e
source-git-commit: a40907925c7f8c783a3baf9673009a54f433b960
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 4%

---

# 開始使用WhatsApp設定 {#whatsapp-config}

>[!BEGINSHADEBOX]

**目錄**

* [開始使用WhatsApp訊息](get-started-whatsapp.md)
* **[開始使用WhatsApp設定](whatsapp-configuration.md)**
* [建立WhatsApp訊息](create-whatsapp.md)
* [檢查並傳送您的WhatsApp訊息](send-whatsapp.md)

>[!ENDSHADEBOX]

在傳送WhatsApp訊息之前，您必須先設定Adobe Journey Optimizer環境，並與您的WhatsApp帳戶建立關聯。 若要執行此動作：

1. [建立您的WhatsApp API認證](#WhatsApp-credentials)
1. [建立您的WhatsApp設定](#WhatsApp-configuration)

這些步驟必須由Adobe Journey Optimizer [系統管理員](../start/path/administrator.md)執行。

## 建立WhatsApp API認證 {#whatsapp-credentials}

1. 在左側邊欄中，瀏覽至&#x200B;**[!UICONTROL 管理]** `>` **[!UICONTROL 管道]**&#x200B;並選取&#x200B;**[!UICONTROL API認證]**&#x200B;功能表。 按一下&#x200B;**[!UICONTROL 建立新的API認證]**&#x200B;按鈕。

1. 設定您的API認證，如下所述：

   * **API Token**：輸入您的API Token。 進一步瞭解[中繼檔案](https://developers.facebook.com/docs/facebook-login/guides/access-tokens/)
   * **企業帳戶ID**：輸入與您的企業組合相關的唯一編號。 進一步瞭解[中繼檔案](https://www.facebook.com/business/help/1181250022022158?id=180505742745347)。

   ![](assets/whatsapp-api.png)

1. 按一下&#x200B;**[!UICONTROL 繼續]**。

1. 選擇您要連線至您的WhatsApp API認證的&#x200B;**商務帳戶**。

   ![](assets/whatsapp-api-2.png)

1. 選取用來傳送您的Whatsapp訊息的&#x200B;**電話號碼**。

1. 您的電話號碼設定會自動填寫：

   * **品質評等**：反映客戶對過去24小時內傳送的訊息的意見反應。
      * 綠色：高品質
      * 黃色：Medium品質
      * 紅色：低品質

     深入瞭解[品質評等](https://www.facebook.com/business/help/766346674749731#)

   * **輸送量**：表示您的電話號碼可以傳送訊息的速率。

1. 完成API認證的設定時，請按一下&#x200B;**[!UICONTROL 提交]**。

建立和設定API認證後，您現在需要建立WhatsApp訊息的通道設定。 [了解更多](#whatsapp-configuration)

## 建立WhatsApp設定 {#whatsapp-configuration}

1. 在左側邊欄中，瀏覽至&#x200B;**[!UICONTROL 管理]** > **[!UICONTROL 管道]**&#x200B;並選取&#x200B;**[!UICONTROL 一般設定]** > **[!UICONTROL 管道設定]**。 按一下&#x200B;**[!UICONTROL 建立通道組態]**&#x200B;按鈕。

   ![](assets/whatsapp-config-1.png)

1. 輸入設定的名稱和說明（選用），然後選取WhatsApp通道。

   >[!NOTE]
   >
   > 名稱必須以字母(A-Z)開頭。 它只能包含英數字元。 您也可以使用底線 `_`、點 `.` 和連字號 `-` 字元。

1. 選取&#x200B;**[!DNL WhatsApp]**&#x200B;作為您的頻道。

   ![](assets/whatsapp-config-2.png)

1. 選取&#x200B;**[!UICONTROL 行銷動作]**，以使用此設定將同意原則與訊息相關聯。 系統會運用與行銷動作相關的所有同意政策，以尊重客戶的偏好設定。 了解更多

1. 選取先前建立的&#x200B;**[!UICONTROL WhatsApp API組態]**。

   ![](assets/whatsapp-config-3.png)

1. 輸入&#x200B;您要用於通訊的&#x200B;**[!UICONTROL 寄件者號碼]**。

1. 設定完所有引數後，按一下&#x200B;**[!UICONTROL 提交]**&#x200B;確認。 您也可以將頻道設定儲存為草稿，並稍後繼續其設定。

1. 建立管道設定後，它就會顯示在狀態為&#x200B;**[!UICONTROL 處理中]**&#x200B;的清單中。

   >[!NOTE]
   >
   >如果檢查不成功，請在[本節](../configuration/channel-surfaces.md)中進一步瞭解可能的失敗原因。

1. 檢查成功後，通道設定會取得&#x200B;**[!UICONTROL 作用中]**&#x200B;狀態。 已準備好用於傳遞訊息。

您現在可以使用Journey Optimizer傳送WhatsApp訊息。
