---
solution: Journey Optimizer
product: journey optimizer
title: 設定 Sinch 提供者
description: 瞭解如何使用Sinch設定您的環境以使用Journey Optimizer傳送文字訊息
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 85412a85-edf0-4069-8bc7-b80371375f1f
source-git-commit: a196a27fd22a03915838ab4a9bb6139f85242f6b
workflow-type: tm+mt
source-wordcount: '705'
ht-degree: 3%

---

# 設定 Sinch 提供者 {#sms-configuration-sinch}

搭配Journey Optimizer使用Sinch提供者時，您可以找到兩個不同的選項：

* **SMS設定**：設定您的Sinch API認證，以順暢地傳送SMS訊息。

* **MMS設定**：對於多媒體訊息(MMS)，請設定您的Sinch MMS API認證。 請注意，追蹤和回應傳入訊息由SMS設定處理。 MMS設定僅適用於MMS訊息的傳出傳遞。

## Sinch API認證{#create-api}

若要設定您的Sinch提供者使用Journey Optimizer傳送SMS訊息和MMS，請遵循下列步驟：

1. 在左側邊欄中，瀏覽至&#x200B;**[!UICONTROL 管理]** > **[!UICONTROL 管道]** `>` **[!UICONTROL SMS設定]**&#x200B;並選取&#x200B;**[!UICONTROL API認證]**&#x200B;功能表。 按一下&#x200B;**[!UICONTROL 建立新的API認證]**&#x200B;按鈕。

1. 設定您的SMS API認證，如下所述：

   * **[!UICONTROL SMS供應商]**： Sinch。

   * **[!UICONTROL 名稱]**：為您的API認證選擇一個名稱。

   * **[!UICONTROL 服務ID]**&#x200B;和&#x200B;**[!UICONTROL API Token]**：存取API頁面，您可以在SMS標籤下找到您的認證。 深入瞭解[Sinch檔案](https://developers.sinch.com/docs/sms/getting-started/){target="_blank"}。

   * **[!UICONTROL 選擇加入關鍵字]**：輸入將會自動觸發您&#x200B;**[!UICONTROL 選擇加入訊息]**&#x200B;的預設或自訂關鍵字。 對於多個關鍵字，請使用逗號分隔值。

   * **[!UICONTROL 選擇加入訊息]**：輸入自訂回應，此回應會自動傳送為您的&#x200B;**[!UICONTROL 選擇加入訊息]**。

   * **[!UICONTROL 選擇退出關鍵字]**：輸入將會自動觸發您&#x200B;**[!UICONTROL 選擇退出訊息]**&#x200B;的預設或自訂關鍵字。 對於多個關鍵字，請使用逗號分隔值。

   * **[!UICONTROL 選擇退出訊息]**：輸入自訂回應，此回應會自動傳送為您的&#x200B;**[!UICONTROL 選擇退出訊息]**。

   * **[!UICONTROL 說明關鍵字]**：輸入將會自動觸發您&#x200B;**說明訊息**&#x200B;的預設或自訂關鍵字。 對於多個關鍵字，請使用逗號分隔值。

   * **[!UICONTROL 說明訊息]**：輸入自動傳送為您&#x200B;**說明訊息**&#x200B;的自訂回應。

   * **[!UICONTROL 雙重加入關鍵字]**：輸入觸發雙重加入程式的關鍵字。 如果使用者輪廓不存在，則會在成功確認時加以建立。對於多個關鍵字，請使用逗號分隔值。 [進一步瞭解簡訊雙重選擇加入](https://video.tv.adobe.com/v/3427129/?learn=on)。

   * **[!UICONTROL 雙重加入訊息]**：輸入自動傳送以回應雙重加入確認的自訂回應。

   * **[!UICONTROL 傳入號碼]**：新增您的唯一傳入號碼或簡短代碼。 這可讓您在不同的沙箱中使用相同的API認證，每個沙箱都有自己的傳入號碼或短程式碼。

   * **[!UICONTROL 自訂傳入關鍵字]**：為特定動作（例如DISCOUNT、OFFERS、ENROLL）定義唯一的關鍵字。 這些關鍵字會擷取並儲存為設定檔中的屬性，可讓您在歷程中觸發串流區段資格，並提供自訂回應或動作。

   * **[!UICONTROL 預設傳入回複訊息]**：輸入當一般使用者傳送的傳入SMS不符合任何已定義的關鍵字時，所傳送的預設回覆。

1. 完成API認證的設定時，請按一下&#x200B;**[!UICONTROL 提交]**。

1. 在&#x200B;**[!UICONTROL API認證]**&#x200B;功能表中，按一下bin圖示以刪除您的API認證。

1. 若要修改現有認證，請找到所需的API認證，然後按一下&#x200B;**[!UICONTROL 編輯]**&#x200B;選項以進行必要的變更。

建立和設定API認證後，您現在需要建立SMS訊息的通道設定。 [了解更多](sms-configuration-surface.md)

## Sinch MMS API認證 {#sinch-mms}

>[!IMPORTANT]
>
> 除了MMS設定，您還需要建立Sinch API認證，專門用於追蹤傳入訊息及管理同意請求。

若要設定Sinch MMS以使用Journey Optimizer傳送MMS，請遵循下列步驟：

1. 在左側邊欄中，瀏覽至&#x200B;**[!UICONTROL 管理]** > **[!UICONTROL 管道]** `>` **[!UICONTROL SMS設定]**&#x200B;並選取&#x200B;**[!UICONTROL API認證]**&#x200B;功能表。 按一下&#x200B;**[!UICONTROL 建立新的API認證]**&#x200B;按鈕。

1. 設定您的MMS API認證，如下所述：

   * **[!UICONTROL SMS廠商]**： Sinch MMS。

   * **[!UICONTROL 名稱]**：為您的API認證選擇一個名稱。

   * **[!UICONTROL 專案識別碼]**、**[!UICONTROL 應用程式識別碼]**&#x200B;和&#x200B;**[!UICONTROL API權杖]**：請依照下列步驟收集您的MMS API認證。

      * 針對&#x200B;**[!UICONTROL 專案識別碼]**&#x200B;和&#x200B;**[!UICONTROL 應用程式識別碼]**：存取您Sinch儀表板上Sinch專案的[交談API總覽](https://dashboard.sinch.com/convapi/overview)頁面。
      * 針對&#x200B;**[!UICONTROL API Token]**：取得您Sinch專案的[存取金鑰](https://community.sinch.com/t5/Customer-Dashboard/Sinch-Access-Keys/ta-p/12638)，並從您的Sinch專案&#x200B;**存取金鑰**&#x200B;中產生&#x200B;**Base64 API Token**。

1. 完成API認證的設定時，請按一下&#x200B;**[!UICONTROL 提交]**。

1. 在&#x200B;**[!UICONTROL API認證]**&#x200B;功能表中，按一下bin圖示以刪除您的API認證。

1. 若要修改現有認證，請找到所需的API認證，然後按一下&#x200B;**[!UICONTROL 編輯]**&#x200B;選項以進行必要的變更。

建立和設定API認證後，您現在需要建立MMS訊息的通道設定。 [了解更多](sms-configuration-surface.md)
