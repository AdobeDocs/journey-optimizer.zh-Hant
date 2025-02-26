---
solution: Journey Optimizer
product: journey optimizer
title: 使用範例輸入資料 (測試版) 來測試內容
description: 瞭解如何使用CSV或JSON檔案的範例輸入資料或手動新增，來預覽內容並傳送電子郵件校樣。
feature: Email, Email Rendering, Personalization, Preview, Proofs
topic: Content Management
role: User
level: Intermediate
badge: label="Beta" type="Informative"
exl-id: 8462c75e-4f4b-4c4f-8734-19efbbc70c7a
source-git-commit: f41426bd41078b98a26c32ce259a848ab49d724c
workflow-type: tm+mt
source-wordcount: '932'
ht-degree: 5%

---

# 使用範例輸入資料測試您的內容{#custom-profiles}

>[!CONTEXTUALHELP]
>id="ajo_simulate_sample_profiles"
>title="使用範例輸入進行模擬"
>abstract="在這個畫面中，您可以透過 CSV 或 JSON 範本為個人化欄位提供值，或手動輸入值來測試內容的不同變體。"

>[!AVAILABILITY]
>
>此功能目前以公開測試版的形式提供給所有客戶。

Journey Optimizer可讓您預覽內容，並使用從CSV或JSON檔案上傳或手動新增的範例輸入資料傳送校樣，以測試內容的不同變體。 系統會自動偵測您在內容中用於個人化的所有設定檔屬性，這些屬性可用於測試，以建立多個變體。 變體是指具有不同屬性值的內容版本。

>[!NOTE]
>
>目前，模擬內容變數僅適用於電子郵件、簡訊和推播通知頻道。

若要存取此體驗，請按一下[模擬內容]按鈕&#x200B;]**，然後選擇[模擬內容變化(Beta)]]**。**[!UICONTROL **[!UICONTROL 

![](assets/simulate-sample.png)

測試內容的主要步驟如下：

1. 透過上傳檔案或手動新增資料，使用範例輸入資料新增最多30個變體。 [瞭解如何新增變體](#profiles)
1. 使用不同的變體來檢查內容的預覽。 [瞭解如何預覽您的內容](#preview)
1. 針對電子郵件內容，使用不同變體向電子郵件地址傳送最多10個校樣。 [瞭解如何傳送校樣](#proofs)


## 護欄和限制 {#limitations}

開始使用範例輸入資料來測試內容之前，請考量下列護欄和先決條件。

* 截至目前，使用範例輸入資料進行的測試僅適用於電子郵件、簡訊和推播通知頻道。 無法從電子郵件Designer中的「模擬內容」按鈕存取體驗。
* 目前體驗中不提供下列功能：收件匣轉譯、垃圾郵件報告、多語言內容和內容實驗。 若要使用這些功能，請從您的內容中選取&#x200B;**[!UICONTROL 模擬內容]**&#x200B;按鈕，以存取先前的使用者介面。
* 目前僅支援設定檔屬性。 如果在您的內容中使用內容屬性進行個人化，您將無法使用這些屬性測試您的內容。
* 為您的變體輸入資料時，僅支援下列資料型別：數字（整數與小數）、字串、布林值和日期型別。 任何其他資料型別都會顯示錯誤。

## 新增變體 {#profiles}

您可以使用檔案或手動新增最多30種變體來測試您的內容。

>[!NOTE]
>
>新增的變體僅會作為您目前內容的測試用途。 不會儲存在Adobe Experience Platform中，而是儲存在您的使用者瀏覽器工作階段中，這表示在登出或從其他裝置工作時，不會顯示這些檔案。

### 使用檔案新增變體 {#file}

若要從檔案新增變體，請遵循下列步驟：

1. 按一下&#x200B;**[!UICONTROL 下載範例]**&#x200B;連結以擷取檔案範本，然後選擇您要使用的檔案格式（CSV、JSON或JSONLINES）。
1. 按一下&#x200B;**[!UICONTROL 下載]**，然後將範本儲存在所需的位置。
1. 開啟檔案，然後填寫範本以符合您的需求。 此範本包含用於內容中個人化之每個設定檔屬性的欄。

   +++檔案範例

   ```
   {
   "profile": {
       "attributes": {
       "person": {
           "name": {
               "lastName": "Doe",
               "firstName": "John"
               }
           }
       }
   }
   }
   ```

+++

1. 當您的檔案準備就緒時，請按一下&#x200B;**[!UICONTROL 上傳輸入資料]**&#x200B;以載入它以測試您的內容。
1. 上傳檔案後，會在左窗格中為檔案的每一行新增一個方塊。 每個方塊都包含內容中用於個人化的所有設定檔屬性。 您現在可以使用變體在右窗格中預覽您的內容並傳送校樣。

   ![](assets/simulate-custom-variants.png)

### 手動新增變體 {#manual}

若要手動新增變體，請按照以下步驟操作：

1. 按一下&#x200B;**[!UICONTROL 建立範例輸入]**&#x200B;按鈕。

   左側窗格中會新增一個方塊，其中包含您的內容中用於個人化的所有設定檔屬性。

1. 填寫變體的範例輸入資料，然後按一下&#x200B;**[!UICONTROL 儲存]**。

   ![](assets/simulate-custom-add.png)

1. 新增變體後，您就可以使用這些變體在右窗格中預覽您的內容並傳送校樣。

## 預覽您的內容變體 {#preview}

若要使用其中一個變體預覽您的內容，請選取相關方塊，以使用為此變體輸入的資訊更新右側區段中的內容預覽。

在以下範例中，我們已為電子郵件主旨行新增兩種變體：

| 變體1選擇 | 變體2選擇 |
|----------|-------------|
| ![](assets/simulate-custom-boxes.png) | ![](assets/simulate-custom-boxes2.png) |

您可以使用右上角的省略符號按鈕並選取&#x200B;**[!UICONTROL 移除]**，隨時移除變體。 若要編輯變體的資訊，請按一下省略符號按鈕，然後選取&#x200B;**[!UICONTROL 編輯]**。

## 發送校訂 {#proofs}

Journey Optimizer可讓您傳送校樣到電子郵件地址，同時模擬您在模擬畫面中新增的一或多個變體。 步驟如下：

1. 確認已新增變體以測試您的內容，然後按一下&#x200B;**[!UICONTROL 傳送校樣]**&#x200B;按鈕。

1. 在&#x200B;**[!UICONTROL 收件者]**&#x200B;欄位中，輸入您要傳送證明的電子郵件地址，然後按一下&#x200B;**[!UICONTROL 新增]**。 重複操作，將校樣傳送至其他電子郵件地址。 您最多可以新增10個校訂收件者。

1. 在熒幕的底部，選取您要在校樣中使用的變體。 您可以選取多個變體，在這種情況下，電子郵件將包含與所選變體相同數量的校樣。

   如需變體的詳細資訊，請選取&#x200B;**[!UICONTROL 檢視設定檔詳細資料]**&#x200B;連結。 這可讓您顯示在先前畫面中針對不同變體輸入的資訊。

   ![](assets/simulate-custom-proofs.png)

1. 按一下&#x200B;**[!UICONTROL 傳送校樣]**&#x200B;按鈕以開始傳送校樣。

1. 若要追蹤校訂傳送，請按一下模擬內容畫面中的&#x200B;**[!UICONTROL 檢視校訂]**&#x200B;按鈕。

![](assets/simulate-custom-sent-proofs.png)
