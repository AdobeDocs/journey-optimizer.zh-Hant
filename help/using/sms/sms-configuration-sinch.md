---
solution: Journey Optimizer
product: journey optimizer
title: 設定 Sinch 提供者
description: 瞭解如何使用Sinch設定您的環境以使用Journey Optimizer傳送文字訊息
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 85412a85-edf0-4069-8bc7-b80371375f1f
source-git-commit: 794ac45177e467be4bd5b8f7288e07c85e4d806a
workflow-type: tm+mt
source-wordcount: '584'
ht-degree: 3%

---

# 設定 Sinch 提供者 {#sms-configuration-sinch}

搭配Journey Optimizer使用Sinch提供者時，您可以找到兩個不同的選項：

* **簡訊設定**：設定您的Sinch API認證，以順暢地傳送SMS訊息。

* **MMS設定**：針對多媒體訊息(MMS)，請設定您的Sinch MMS API認證。 請注意，追蹤和回應傳入訊息由SMS設定處理。 MMS設定僅適用於MMS訊息的傳出傳遞。

## Sinch API認證{#create-api}

若要設定您的Sinch提供者使用Journey Optimizer傳送SMS訊息和MMS，請遵循下列步驟：

1. 在左側邊欄中，瀏覽至 **[!UICONTROL 管理]** > **[!UICONTROL 頻道]** 並選取 **[!UICONTROL API認證]** 功能表。 按一下 **[!UICONTROL 建立新的API認證]** 按鈕。

1. 設定您的SMS API認證，如下所述：

   * **[!UICONTROL 簡訊供應商]**：Sinch。

   * **[!UICONTROL 名稱]**：為您的API認證選擇名稱。

   * **[!UICONTROL 服務ID]** 和 **[!UICONTROL API Token]**：存取API頁面，您可以在SMS標籤下找到您的認證。 進一步瞭解 [Sinch檔案](https://developers.sinch.com/docs/sms/getting-started/){target="_blank"}.

   * **[!UICONTROL 選擇加入關鍵字]**：輸入將會自動觸發的預設或自訂關鍵字 **[!UICONTROL 選擇加入訊息]**. 對於多個關鍵字，請使用逗號分隔值。

   * **[!UICONTROL 選擇加入訊息]**：輸入自訂回應，此回應會作為 **[!UICONTROL 選擇加入訊息]**.

   * **[!UICONTROL 選擇退出關鍵字]**：輸入將會自動觸發的預設或自訂關鍵字 **[!UICONTROL 選擇退出訊息]**. 對於多個關鍵字，請使用逗號分隔值。

   * **[!UICONTROL 選擇退出訊息]**：輸入自訂回應，此回應會作為 **[!UICONTROL 選擇退出訊息]**.

   * **[!UICONTROL 說明關鍵字]**：輸入將會自動觸發的預設或自訂關鍵字 **說明訊息**. 對於多個關鍵字，請使用逗號分隔值。

   * **[!UICONTROL 說明訊息]**：輸入自訂回應，此回應會作為 **說明訊息**.

   * **[!UICONTROL 雙重選擇加入關鍵字]**：輸入觸發雙重加入流程的關鍵字。 如果使用者設定檔不存在，則會在成功確認時加以建立。對於多個關鍵字，請使用逗號分隔值。 [進一步瞭解簡訊雙重選擇加入](https://video.tv.adobe.com/v/3427129/?learn=on).

   * **[!UICONTROL 雙重選擇加入訊息]**：輸入自動傳送以回應雙重選擇加入確認的自訂回應。

   * **[!UICONTROL 傳入號碼]**：新增您的不重複傳入號碼。 這可讓您在不同的沙箱中使用相同的API認證，每個沙箱都有自己的傳入號碼。

1. 按一下 **[!UICONTROL 提交]** 完成API認證的設定時。

建立和設定API認證後，您現在需要建立SMS訊息的頻道介面。 [了解更多](sms-configuration-surface.md)

## Sinch MMS API認證 {#sinch-mms}

>[!IMPORTANT]
>
> 除了MMS設定，您還需要建立Sinch API認證，專門用於追蹤傳入訊息及管理同意請求。

若要設定Sinch MMS以使用Journey Optimizer傳送MMS，請遵循下列步驟：

1. 在左側邊欄中，瀏覽至 **[!UICONTROL 管理]** > **[!UICONTROL 頻道]** 並選取 **[!UICONTROL API認證]** 功能表。 按一下 **[!UICONTROL 建立新的API認證]** 按鈕。

1. 設定您的MMS API認證，如下所述：

   * **[!UICONTROL 簡訊供應商]**：Sinch多媒體簡訊。

   * **[!UICONTROL 名稱]**：為您的API認證選擇名稱。

   * **[!UICONTROL 專案ID]**， **[!UICONTROL 應用程式ID]** 和 **[!UICONTROL API Token]**：請依照下列步驟收集您的MMS API認證。

      * 的 **[!UICONTROL 專案ID]** 和 **[!UICONTROL 應用程式ID]**：存取 [交談API總覽](https://dashboard.sinch.com/convapi/overview) 「Sinch儀表板」上Sinch專案的頁面。
      * 的 **[!UICONTROL API Token]**：取得 [存取金鑰](https://community.sinch.com/t5/Customer-Dashboard/Sinch-Access-Keys/ta-p/12638) ，並產生 **Base64 API Token** 移出您的Sinch專案 **存取金鑰**.

   * **[!UICONTROL 服務計畫ID]** 和 **[!UICONTROL SMS API Token]**：您的 **[!UICONTROL 服務計畫ID]** 和 **[!UICONTROL SMS API Token]** 位於API頁面的SMS標籤上。

1. 按一下 **[!UICONTROL 提交]** 完成API認證的設定時。

建立和設定API認證後，您現在需要建立MMS訊息的管道表面。 [了解更多](sms-configuration-surface.md)
