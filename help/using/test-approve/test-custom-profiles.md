---
solution: Journey Optimizer
product: journey optimizer
title: 使用範例設定檔測試您的內容
description: 瞭解如何使用範例設定檔預覽電子郵件內容及傳送校樣。
feature: Overview, Get Started
topic: Content Management
role: User
level: Intermediate
badge: label="Beta"
hide: true
hidefromtoc: true
source-git-commit: 6b3518645b9cbfbe6f728011b0889c28fa754496
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# 使用範例設定檔測試您的內容 {#custom-profiles}

>[!CONTEXTUALHELP]
>id="ajo_simulate_sample_profiles"
>title="使用範例設定檔進行模擬"
>abstract="在此畫面中，您可以預覽電子郵件內容並傳送校樣，同時模擬可從CSV檔案上傳或直接從此畫面手動新增的範例設定檔。"


<!--ATTENTE CONFIRMATION 

- nom (custom/sample)
- campaigns/journeys ou que campaigns

-->

>[!AVAILABILITY]
>
>此功能目前僅供選定使用者作為測試版使用。

Journey Optimizer可讓您使用範例設定檔來預覽和測試電子郵件內容，您可以從CSV檔案上傳設定檔，或在模擬內容時直接手動新增。 此功能可讓您選取範例設定檔，以用於預覽您的內容並傳送校樣。 系統會自動偵測您在內容中用於個人化的所有設定檔屬性，這些屬性都可用於您的測試。

若要存取此體驗，請按一下[模擬內容] ]**按鈕，然後選擇[使用CSV(Beta)模擬]]**。**[!UICONTROL **[!UICONTROL 

![](assets/simulate-sample.png)


測試內容的主要步驟如下：

1. 上傳一個CSV檔案或逐一手動新增設定檔，即可新增最多30個範例設定檔。 [瞭解如何新增範例設定檔](#profiles)
1. 使用新增的設定檔檢查內容的預覽。 [瞭解如何預覽您的內容](#preview)
1. 在模擬所需的範例設定檔時，向電子郵件地址傳送最多10個校樣。 [瞭解如何傳送校樣](#proofs)


## 護欄和限制 {#limitations}

開始使用範例設定檔測試您的內容之前，請考慮以下護欄和先決條件。

* 截至目前，使用範例設定檔進行測試僅適用於行銷活動，以及電子郵件頻道。
* 目前體驗中不提供下列功能：收件匣轉譯、垃圾郵件報告、多語言內容和內容實驗。 若要使用這些功能，請從您的內容中選取&#x200B;**[!UICONTROL 模擬內容]**&#x200B;按鈕，以存取先前的使用者介面。
* 目前僅支援設定檔屬性。 如果在您的內容中使用內容屬性進行個人化，您將無法使用這些屬性測試您的內容。
* 為您的範例設定檔輸入資料時，僅支援下列資料型別：數字（整數和小數）、字串、布林值和日期型別。 任何其他資料型別都會顯示錯誤。

## 新增範例設定檔 {#profiles}

您可以新增最多30個範例設定檔，以使用CSV檔案或手動測試您的內容：

* 若要從CSV檔案上傳設定檔，請按一下&#x200B;**[!UICONTROL 下載範本]**&#x200B;連結以擷取CSV檔案範本。 此範本包含用於內容中個人化之每個設定檔屬性的欄。

  填寫CSV檔案，然後按一下&#x200B;**[!UICONTROL 上傳範例設定檔]**&#x200B;以載入它以測試您的內容。

* 若要手動新增設定檔，請按一下&#x200B;**[!UICONTROL 建立範例設定檔]**&#x200B;按鈕，並填寫設定檔的資訊。 您的內容中用於個人化的每個設定檔屬性會顯示一個欄位。

  ![](assets/simulate-custom-add.png)

選取設定檔後，畫面左側會針對每個設定檔顯示一個方塊。 您可以使用這些設定檔來預覽您的內容並傳送校樣。

>[!NOTE]
>
>新增的範例設定檔僅作為目前內容的測試用途。 不會儲存在Adobe Experience Platform中，而是儲存在您的使用者瀏覽器工作階段中，這表示在登出時或從其他裝置工作時，不會顯示這些檔案。

## 使用範例設定檔預覽您的內容 {#preview}

若要使用其中一個設定檔預覽您的內容，請選取相關方塊，以使用為此設定檔輸入的資訊更新右側區段中的內容預覽。

您可以隨時使用右上角的省略符號按鈕並選取&#x200B;**[!UICONTROL 移除]**&#x200B;來移除方塊。 若要編輯設定檔的資訊，請按一下省略符號按鈕，然後選取&#x200B;**[!UICONTROL 編輯]**。

![](assets/simulate-custom-boxes.png)

## 發送校訂 {#proofs}

Journey Optimizer可讓您在模擬一或多個您在模擬畫面中新增的範例設定檔時，將校樣傳送至電子郵件地址。 步驟如下：

1. 確認已新增範例設定檔以測試您的內容，然後按一下&#x200B;**[!UICONTROL 傳送校樣]**&#x200B;按鈕。

1. 在&#x200B;**[!UICONTROL 收件者]**&#x200B;欄位中，輸入您要傳送證明的電子郵件地址，然後按一下&#x200B;**[!UICONTROL 新增]**。 重複操作，將校樣傳送至其他電子郵件地址。 您最多可以新增10個校訂收件者。

1. 在熒幕的底部，選取您要在校樣中模擬的範例設定檔。 您可以選取多個設定檔，在這種情況下，電子郵件將包含與所選設定檔相同數量的校樣。

   如需設定檔的詳細資訊，請選取&#x200B;**[!UICONTROL 檢視設定檔詳細資料]**&#x200B;連結。 這可讓您顯示在上一個畫面中針對不同設定檔屬性輸入的資訊。

   ![](assets/simulate-custom-proofs.png)

1. 按一下&#x200B;**[!UICONTROL 傳送校樣]**&#x200B;按鈕以開始傳送校樣。

您可以隨時按一下模擬內容畫面中的&#x200B;**[!UICONTROL 檢視校樣]**&#x200B;按鈕來追蹤傳送。

![](assets/simulate-custom-sent-proofs.png)
