---
solution: Journey Optimizer
product: journey optimizer
title: 建立多媒體簡訊
description: 瞭解如何在Journey Optimizer中建立多媒體簡訊
feature: SMS
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
source-git-commit: a6b2c1585867719a48f9abc4bf0eb81558855d85
workflow-type: tm+mt
source-wordcount: '1093'
ht-degree: 9%

---

# 建立MMS訊息 {#create-mms}

## 先決條件{#sms-prerequisites}

建立SMS訊息之前，您必須先使用Journey Optimizer設定SMS供應商，請遵循下列步驟：

* 在傳送簡訊之前，您必須將提供者設定和 Journey Optimizer 整合。

+++ 瞭解如何建立新的Sinch MMS API認證。

   1. 在左側邊欄中，瀏覽至 **[!UICONTROL 管理]** > **[!UICONTROL 頻道]** 並選取 **[!UICONTROL API認證]** 功能表。 按一下 **[!UICONTROL 建立新的API認證]** 按鈕。

      ![](assets/sms_6.png)

   1. 設定您的SMS API認證：

   * 的 **[!DNL Sinch MMS]**：

      * **[!UICONTROL 名稱]**：為您的API認證選擇名稱。

      * **[!UICONTROL 專案ID]**， **[!UICONTROL 應用程式ID]** 和 **[!UICONTROL API Token]**：您可以在「Conversation API」功能表的「應用程式」功能表中找到您的認證。  [了解更多](https://docs.cc.sinch.com/cloud/service-configuration/en/oxy_ex-1/common/wln1620131604643.html)

     ![](assets/mms_provider.png)

   1. 按一下 **[!UICONTROL 提交]** 完成API認證的設定時。

  建立和設定API認證後，您現在需要建立SMS訊息的頻道介面（即訊息預設集）。

+++

* 完成後，您將需要建立一個簡訊表面。這些步驟必須由 Adobe Journey Optimizer 系統管理員執行。

+++ 瞭解如何建立您的管道表面。

   1. 在左側邊欄中，瀏覽至 **[!UICONTROL 管理]** > **[!UICONTROL 頻道]** 並選取 **[!UICONTROL 品牌化]** > **[!UICONTROL 管道表面]**. 按一下 **[!UICONTROL 建立管道表面]** 按鈕。

      ![](assets/preset-create.png)

   1. 輸入表面的名稱和說明（選擇性），然後選取SMS通道。

      ![](assets/sms-create-surface.png)

      >[!NOTE]
      >
      > 名稱必須以字母(A-Z)開頭。 它只能包含英數字元。 您也可以使用底線 `_`，點`.` 和連字型大小 `-` 個字元。

   1. 定義 **簡訊設定**.

      ![](assets/sms-surface-settings.png)

      首先，選取 **[!UICONTROL 簡訊型別]** 將與介面一併傳送的郵件： **[!UICONTROL 異動]** 或 **[!UICONTROL 行銷]**.

      * 選擇 **行銷** 促銷簡訊：這些訊息需要使用者同意。
      * 選擇 **異動** 非商業訊息，例如訂單確認、密碼重設通知或傳遞資訊。

      建立SMS訊息時，您必須選擇與您為訊息選取的類別相符的有效頻道介面。

      >[!CAUTION]
      >
      >**異動** SMS訊息可傳送給取消訂閱行銷通訊的設定檔。 這些訊息只能在特定內容中傳送。

   1. 選取 **[!UICONTROL 簡訊設定]** 以與曲面相關聯。

      有關如何設定環境以傳送SMS訊息的詳細資訊，請參閱 [本節](#create-api).

   1. 輸入 **[!UICONTROL 寄件者號碼]** 您&#x200B;要用於通訊。

   1. 選取您的 **[!UICONTROL 簡訊執行欄位]** 以選取 **[!UICONTROL 設定檔屬性]** 與設定檔的電話號碼相關聯。

   1. 如果您想要在SMS訊息中使用URL縮短功能，請從 **[!UICONTROL 子網域]** 清單。

      >[!NOTE]
      >
      >若要能夠選取子網域，請確定您先前已設定至少一個SMS子網域。 [了解作法](sms-subdomains.md)

   1. 輸入 **[!UICONTROL 選擇退出號碼]** 您要用於此曲面。 當設定檔選擇退出此號碼時，您仍然可以從其他號碼傳送訊息給設定檔，而您可能會使用其他號碼傳送簡訊給設定檔 [!DNL Journey Optimizer].

      >[!NOTE]
      >
      >在 [!DNL Journey Optimizer]，頻道層級不再管理簡訊選擇退出。 它現在特定於數字。

   1. 設定好所有引數後，按一下 **[!UICONTROL 提交]** 以確認。 您也可以將管路曲面儲存為草繪，並稍後恢復其組態。

      ![](assets/sms-submit-surface.png)

   1. 建立管道曲面後，它會顯示於清單中，其中包含 **[!UICONTROL 處理中]** 狀態。

      >[!NOTE]
      >
      >如果檢查不成功，請在中進一步瞭解可能的失敗原因 [本節](#monitor-channel-surfaces).

   1. 檢查成功後，管道表面會取得 **[!UICONTROL 作用中]** 狀態。 已準備好用於傳遞訊息。

      ![](assets/preset-active.png)


## 建立簡訊訊息 {#create-sms-journey-campaign}

瀏覽下列標籤，瞭解如何在行銷活動或歷程中新增SMS訊息。

>[!BEGINTABS]

>[!TAB 將SMS訊息新增至歷程]

1. 開啟您的歷程，然後從拖放簡訊活動 **動作** 區段。

   ![](assets/sms_create_1.png)

1. 提供訊息的基本資訊（標籤、說明、類別），然後選擇要使用的訊息介面。

   ![](assets/sms_create_2.png)

   有關如何設定歷程的詳細資訊，請參閱 [此頁面](../building-journeys/journey-gs.md)

   此 **[!UICONTROL 表面]** 依預設，欄位會預先填入使用者用於該管道的最後一個表面。

您現在可以從以下網址開始設計簡訊的內容： **[!UICONTROL 編輯內容]** 按鈕。 [定義您的簡訊內容](#sms-content)

>[!TAB 新增簡訊至行銷活動]

1. 建立新的排程或API觸發的行銷活動，選取 **[!UICONTROL 簡訊]** 作為您的動作，然後選擇 **[!UICONTROL 應用程式表面]** 以使用。 [進一步瞭解簡訊設定](sms-configuration.md).

   ![](assets/sms_create_3.png)

1. 按一下&#x200B;**[!UICONTROL 建立]**。

1. 從 **[!UICONTROL 屬性]** 區段，編輯您的行銷活動 **[!UICONTROL 標題]** 和 **[!UICONTROL 說明]**.

   ![](assets/sms_create_4.png)

1. 按一下 **[!UICONTROL 選取對象]** 按鈕，從可用的Adobe Experience Platform對象清單定義要定位的對象。 [了解更多](../audience/about-audiences.md)。

1. 在 **[!UICONTROL 身分名稱空間]** 欄位，選擇要使用的名稱空間，以識別所選對象中的個人。 [了解更多](../event/about-creating.md#select-the-namespace)。

   ![](assets/sms_create_5.png)

1. 按一下 **[!UICONTROL 建立實驗]** 開始設定內容實驗並建立處理方式，以測量其效能並識別目標對象的最佳選項。 [了解更多](../campaigns/content-experiment.md)

1. 在 **[!UICONTROL 動作追蹤]** 區段，指定您是否想要追蹤SMS訊息中連結的點按。

1. 行銷活動旨在特定日期或循環頻率執行。 瞭解如何設定 **[!UICONTROL 排程]** 中的行銷活動 [本節](../campaigns/create-campaign.md#schedule).

1. 從 **[!UICONTROL 動作觸發程式]** 功能表，選擇 **[!UICONTROL 頻率]** SMS訊息的：

   * 一次
   * 每日
   * 每週
   * 月

您現在可以從以下網址開始設計簡訊的內容： **[!UICONTROL 編輯內容]** 按鈕。 [設計您的簡訊內容](#sms-content)

>[!ENDTABS]

## 定義多媒體簡訊內容{#mms-content}

1. 在歷程或行銷活動設定畫面中，按一下 **[!UICONTROL 編輯內容]** 按鈕以設定簡訊內容。

1. 按一下 **[!UICONTROL 訊息]** 欄位以開啟運算式編輯器。

   ![](assets/sms-content.png)

1. 使用運算式編輯器來定義內容及新增動態內容。 您可以使用任何屬性，例如設定檔名稱或城市。 進一步瞭解 [個人化](../personalization/personalize.md) 和 [動態內容](../personalization/get-started-dynamic-content.md) 在運算式編輯器中。

1. 啟用MMS選項以將媒體新增到您的SMS內容。

   >[!NOTE]
   >
   > MMS選項僅適用於Sinch。 您需要建立特定的API認證才能建立MMS。 [了解更多](sms-configuration.md#create-new-api)

   ![](assets/sms_create_6.png)

1. 新增 **[!UICONTROL 標題]** 至您的媒體。

1. 在「 」中輸入媒體的URL **[!UICONTROL 媒體]** 欄位。

   ![](assets/sms_create_7.png)

1. 按一下「**[!UICONTROL 儲存]**」並在預覽中查看您的訊息。您可以使用 **[!UICONTROL 模擬內容]** 以預覽您縮短的URL或個人化內容。

您現在可以測試並傳送簡訊給對象。 [瞭解更多](send-sms.md)
傳送後，您可以在行銷活動或歷程報告中測量簡訊的影響。 如需報告的詳細資訊，請參閱[本區段](../reports/campaign-global-report.md#sms-tab)。

>[!NOTE]
>
>根據行業標準及法規，所有簡訊行銷訊息都必須包含讓收件者輕鬆取消訂閱的方式。 要執行此操作，簡訊收件者可以使用選擇加入和選擇退出關鍵字進行回覆。 [瞭解如何管理選擇退出](../privacy/opt-out.md#sms-opt-out-management-sms-opt-out-management)

**相關主題**

* [預覽、測試和傳送您的SMS訊息](send-sms.md)
* [設定簡訊頻道](sms-configuration.md)
* [簡訊報告](../reports/journey-global-report.md#sms-global)