---
solution: Journey Optimizer
product: journey optimizer
title: 使用自訂設定檔測試您的內容
description: 瞭解如何使用自訂設定檔預覽您的內容並傳送校樣。
feature: Overview, Get Started
topic: Content Management
role: User
level: Intermediate
badge: label="Beta"
hide: true
hidefromtoc: true
source-git-commit: 6229f295b961b0535139b64928216e40c3759947
workflow-type: tm+mt
source-wordcount: '599'
ht-degree: 0%

---


# 使用自訂設定檔測試您的內容 {#custom-profiles}

>[!CONTEXTUALHELP]
>id="ajo_simulate_sample_profiles"
>title="使用自訂設定檔模擬"
>abstract="在此畫面中，您可以預覽內容並傳送校樣，同時模擬您可以從CSV檔案上傳或直接從此畫面手動新增的自訂設定檔。"

>[!AVAILABILITY]
>
>此功能目前僅供選定使用者作為測試版使用。
>
>目前體驗中無法使用收件匣轉譯和垃圾郵件報告。 若要使用這些功能，請從您的內容中選取&#x200B;**[!UICONTROL 模擬內容]**&#x200B;按鈕，以存取舊版使用者介面。

Journey Optimizer可讓您使用自訂設定檔來預覽和測試內容，您可以從CSV檔案上傳設定檔，或在模擬內容時直接手動新增。

若要存取此體驗，請按一下[模擬內容] ]**按鈕，然後選擇[使用CSV(Beta)模擬]]**。**[!UICONTROL **[!UICONTROL 

此畫面可讓您選取用來預覽您的內容並傳送校樣的設定檔。 系統會自動偵測您在內容中用於個人化的所有屬性，這些屬性可用於您的測試。

測試內容的主要步驟如下：

1. 透過上傳CSV檔案或手動逐一新增自訂設定檔，來新增自訂設定檔。 [瞭解如何新增自訂設定檔](#profiles)
1. 使用新增的設定檔檢查內容的預覽。 [瞭解如何預覽您的內容](#preview)
1. 在模擬所需的自訂設定檔時，向電子郵件地址傳送最多10個校樣。 [瞭解如何傳送校樣](#proofs)


## 新增自訂設定檔 {#profiles}

您可以使用CSV檔案或手動新增自訂設定檔以測試您的內容：

* 若要從CSV檔案上傳設定檔，請按一下&#x200B;**[!UICONTROL 下載範本]**&#x200B;連結以擷取CSV檔案範本。 此範本包含內容中所使用之每個個人化屬性的欄。

  填寫CSV檔案，然後按一下&#x200B;**[!UICONTROL 上傳範例設定檔]**&#x200B;以載入它以測試您的內容。

* 若要手動新增設定檔，請按一下&#x200B;**[!UICONTROL 建立範例設定檔]**&#x200B;按鈕，並填寫設定檔的資訊。 針對內容中使用的每個個人化屬性，都會顯示一個欄位。

  ![](assets/simulate-custom-add.png)

選取設定檔後，畫面左側會針對每個設定檔顯示一個方塊。 您可以使用這些設定檔來預覽您的內容並傳送校樣。

## 使用自訂設定檔預覽您的內容 {#preview}

若要使用其中一個設定檔預覽您的內容，請選取相關方塊，以使用為此設定檔輸入的資訊更新右側區段中的內容預覽。

您可以隨時使用右上角的省略符號按鈕並選取&#x200B;**[!UICONTROL 移除]**&#x200B;來移除方塊。 若要編輯設定檔的資訊，請按一下省略符號按鈕，然後選取&#x200B;**[!UICONTROL 編輯]**。

![](assets/simulate-custom-boxes.png)

## 發送校訂 {#proofs}

Journey Optimizer可讓您將校樣傳送至電子郵件地址，同時模擬您在模擬畫面中新增的一或多個自訂設定檔。 步驟如下：

1. 確認已新增自訂設定檔以測試您的內容，然後按一下&#x200B;**[!UICONTROL 傳送校樣]**&#x200B;按鈕。

1. 在&#x200B;**[!UICONTROL 收件者]**&#x200B;欄位中，輸入您要傳送證明的電子郵件地址，然後按一下&#x200B;**[!UICONTROL 新增]**。 重複操作，將校樣傳送至其他電子郵件地址。 您最多可以新增10個校訂收件者。

1. 在畫面的底部，選取您要在校樣中模擬的自訂設定檔。 您可以選取多個設定檔，在這種情況下，電子郵件將包含與所選設定檔相同數量的校樣。

   ![](assets/simulate-custom-proofs.png)

1. 按一下&#x200B;**[!UICONTROL 傳送校樣]**&#x200B;按鈕以開始傳送校樣。

您可以隨時按一下模擬內容畫面中的&#x200B;**[!UICONTROL 檢視校樣]**&#x200B;按鈕來追蹤傳送。

![](assets/simulate-custom-sent-proofs.png)
