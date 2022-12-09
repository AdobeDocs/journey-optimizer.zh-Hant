---
solution: Journey Optimizer
product: journey optimizer
title: 建立測試設定檔
description: 了解如何建立測試設定檔
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: bd5e053a-69eb-463b-add3-8b9168c8e280
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '1290'
ht-degree: 0%

---

# 建立測試設定檔 {#create-test-profiles}

使用 [測試模式](../building-journeys/testing-the-journey.md) 在歷程中 [預覽和測試內容](../email/preview.md).

有數種方式可建立測試設定檔。 您可以在此頁面的詳細資訊中找到：

* 將 [現有設定檔](#turning-profile-into-test) 填入測試設定檔

* 上傳 [csv檔案](#create-test-profiles-csv) 或使用 [API呼叫](#create-test-profiles-api).

   除了這兩種方法外，Adobe Journey Optimizer還隨附特定 [產品內使用案例](#use-case-1) 以方便建立測試設定檔。

您也可以上傳現有資料集中的JSON檔案。 有關詳細資訊，請參閱 [資料擷取檔案](https://experienceleague.adobe.com/docs/experience-platform/ingestion/tutorials/ingest-batch-data.html#add-data-to-dataset){target=&quot;_blank&quot;}。

請注意，建立測試設定檔與在Adobe Experience Platform中建立一般設定檔類似。 如需詳細資訊，請參閱 [即時客戶個人檔案檔案檔案](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html){target=&quot;_blank&quot;}。

➡️ [了解如何在此影片中建立測試設定檔](#video)

## 必要條件 {#test-profile-prerequisites}

若要建立設定檔，您必須先在Adobe中建立結構和資料集 [!DNL Journey Optimizer].

結束日期 **建立結構**，請遵循下列步驟：

1. 在「資料管理」功能表區段中，按一下 **[!UICONTROL Schemas]**.
   ![](assets/test-profiles-0.png)
1. 按一下 **[!UICONTROL Create schema]**，然後選取結構類型，例如 **XDM個別設定檔**.
   ![](assets/test-profiles-1.png)
1. 選擇適當的欄位組。 請務必新增 **設定檔測試詳細資訊** 欄位群組。
   ![](assets/test-profiles-1-ter.png)
完成後，按一下 **[!UICONTROL Add field groups]**:欄位組清單將顯示在架構概述螢幕上。
   ![](assets/test-profiles-2.png)

   >[!NOTE]
   >
   >* 按一下架構的名稱以變更並更新其屬性。
   >
   >* 按一下 **[!UICONTROL Add]** 按鈕（在「欄位組」部分中）以選擇要添加到架構中的其他欄位組


1. 在欄位清單中，按一下您要定義為主要身分的欄位。
   ![](assets/test-profiles-3.png)
1. 在 **[!UICONTROL Field properties]** 右窗格，檢查 **[!UICONTROL Identity]** 和 **[!UICONTROL Primary Identity]** 選項並選取命名空間。 如果您希望主要身分成為電子郵件地址，請選擇 **[!UICONTROL Email]** 命名空間。 按一下 **[!UICONTROL Apply]**.
   ![](assets/test-profiles-4bis.png)
1. 選擇架構並啟用 **[!UICONTROL Profile]** 選項 **[!UICONTROL Schema properties]** 框。
   ![](assets/test-profiles-5.png)
1. 按一下 **儲存**.

>[!NOTE]
>
>有關架構建立的詳細資訊，請參閱 [XDM檔案](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/resources/schemas.html#prerequisites){target=&quot;_blank&quot;}。

那你需要 **建立資料集** 中匯入設定檔。 請依照下列步驟操作：

1. 瀏覽至 **[!UICONTROL Datasets]**，然後按一下 **[!UICONTROL Create dataset]**.
   ![](assets/test-profiles-6.png)
1. 選擇 **[!UICONTROL Create dataset from schema]**.
   ![](assets/test-profiles-7.png)
1. 選取先前建立的架構，然後按一下 **[!UICONTROL Next]**.
   ![](assets/test-profiles-8.png)
1. 選擇名稱，然後按一下 **[!UICONTROL Finish]**.
   ![](assets/test-profiles-9.png)
1. 啟用 **[!UICONTROL Profile]** 選項。
   ![](assets/test-profiles-10.png)

>[!NOTE]
>
> 如需建立資料集的詳細資訊，請參閱 [目錄服務檔案](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html#getting-started){target=&quot;_blank&quot;}。

## 產品內使用案例{#use-case-1}

從Adobe Journey Optimizer首頁，您可以運用產品中的測試設定檔使用案例。 此使用案例有助於建立測試設定檔，以在發佈前測試歷程。

![](assets/use-cases-home.png)

按一下 **[!UICONTROL Begin]** 按鈕以開始使用案例。

需要下列資訊：

1. **身分命名空間**:此 [身分命名空間](../segment/get-started-identity.md) 用來唯一識別測試設定檔。 例如，如果使用電子郵件來識別測試設定檔，則會是身分命名空間 **電子郵件** 中指定的URL。 如果唯一識別碼是電話號碼，則是身分命名空間 **電話** 中指定的URL。

2. **CSV檔案**:以逗號分隔的檔案，包含要建立的測試設定檔清單。 使用案例需要CSV檔案的預先定義格式，其中包含要建立的測試設定檔清單。 檔案中的每一列都應以下列正確順序包含下列欄位：

   1. **人員Id**:測試設定檔的唯一識別碼。 此欄位的值應反映所選取的身分命名空間。 (例如，若 **電話** 會針對身分命名空間選取，則此欄位的值應為電話號碼。 同樣地，如果 **電子郵件** ，則此欄位的值應為電子郵件)
   1. **電子郵件地址**:測試設定檔電子郵件地址。 ( **人員Id** 欄位和 **電子郵件地址** 如果 **電子郵件** 被選為身份命名空間)
   1. **名字**:測試設定檔名。
   1. **姓氏**:測試設定檔的姓氏。
   1. **城市**:測試配置檔案居住城市
   1. **國家/地區**:測試設定檔居住國
   1. **性別**:測試設定檔性別。 可用值包括 **男**, **女性** 和 **non_specified**

選取身分命名空間並根據上述格式提供CSV檔案後，請按一下 **[!UICONTROL Run]** 按鈕。 使用案例可能需要幾分鐘的時間才能完成。 使用案例完成處理並建立測試設定檔後，系統會傳送通知以通知使用者。

>[!NOTE]
>
>測試設定檔可能會覆寫現有設定檔。 執行使用案例之前，請確定CSV僅包含測試設定檔，並針對正確的沙箱執行。

## 將設定檔轉換為測試設定檔{#turning-profile-into-test}

您可以將現有設定檔轉換為測試設定檔：您可以使用建立設定檔時的相同方式更新設定檔屬性。

最簡單的方法是使用 **[!UICONTROL Update Profile]** 歷程中的動作活動並變更 **testProfile** 從false到true的布林欄位。

您的歷程將由 **[!UICONTROL Read Segment]** 和 **[!UICONTROL Update Profile]** 活動。 您首先需要建立以您要轉換成測試設定檔的設定檔為目標的區段。

>[!NOTE]
>
> 由於您將更新 **testProfile** 欄位中，選取的設定檔必須包含此欄位。 相關架構必須具有 **設定檔測試詳細資訊** 欄位群組。 請參閱 [本節](../segment/creating-test-profiles.md#test-profiles-prerequisites).

1. 瀏覽至 **區段**，然後 **建立區段**，位於右上角。
   ![](assets/test-profiles-22.png)
1. 定義區段名稱並建立區段：選擇欄位和值，以定位您想要的設定檔。
   ![](assets/test-profiles-23.png)
1. 按一下 **儲存** 及檢查設定檔是否已由區段正確定位。
   ![](assets/test-profiles-24.png)

   >[!NOTE]
   >
   > 區段計算可能需要一些時間。 進一步了解 [本節](../segment/about-segments.md).

1. 現在，請建立新的歷程，並從 **[!UICONTROL Read Segment]** 協調活動。
1. 選擇先前建立的區段以及您的設定檔使用的命名空間。
   ![](assets/test-profiles-25.png)
1. 新增 **[!UICONTROL Update Profile]** 動作活動。
1. 選取架構， **testProfiles** 欄位、資料集，並將值設為 **True**. 若要執行此作業，請在 **[!UICONTROL VALUE]** 欄位，按一下 **筆** 表徵圖，選擇 **[!UICONTROL Advanced mode]** 輸入 **true**.
   ![](assets/test-profiles-26.png)
1. 按一下 **[!UICONTROL Publish]**.
1. 在 **[!UICONTROL Segments]** 區段，檢查設定檔是否已正確更新。
   ![](assets/test-profiles-28.png)

   >[!NOTE]
   >
   > 如需 **[!UICONTROL Update Profile]** 活動，請參閱 [本節](../building-journeys/update-profiles.md).

## 使用csv檔案建立測試設定檔{#create-test-profiles-csv}

在Adobe Experience Platform中，您可以將包含不同設定檔欄位的csv檔案上傳至資料集，借此建立設定檔。 這是最簡單的方法。

1. 使用試算表軟體建立簡單的csv檔案。
1. 為每個需要的欄位新增一欄。 請務必新增主要身分欄位（上述範例中為「personID」），以及設為「true」的「testProfile」欄位。
   ![](assets/test-profiles-11.png)
1. 為每個設定檔新增一行，並填入每個欄位的值。
   ![](assets/test-profiles-12.png)
1. 將試算表儲存為CSV檔案。 請確定逗號是分隔符號。
1. 瀏覽至Adobe Experience Platform **工作流程**.
   ![](assets/test-profiles-14.png)
1. 選擇 **將CSV對應至XDM結構**，然後按一下 **Launch**.
   ![](assets/test-profiles-16.png)
1. 選取您要將設定檔匯入的資料集。 按一下 **下一個**.
   ![](assets/test-profiles-17.png)
1. 按一下 **選擇檔案** 並選取您的csv檔案。 上傳檔案時，按一下 **下一個**.
   ![](assets/test-profiles-18.png)
1. 將來源csv欄位對應至結構欄位，然後按一下 **完成**.
   ![](assets/test-profiles-19.png)
1. 資料匯入開始。 狀態會從 **處理** to **成功**. 按一下 **預覽資料集**，位於右上角。
   ![](assets/test-profiles-20.png)
1. 檢查測試設定檔是否已正確新增。
   ![](assets/test-profiles-21.png)

系統會新增您的測試設定檔，現在可用於測試歷程。 請參閱 [本節](../building-journeys/testing-the-journey.md).
>[!NOTE]
>
> 如需csv匯入的詳細資訊，請參閱 [資料擷取檔案](https://experienceleague.adobe.com/docs/experience-platform/ingestion/tutorials/map-a-csv-file.html#tutorials){target=&quot;_blank&quot;}。

## 使用API呼叫建立測試設定檔{#create-test-profiles-api}

您也可以透過API呼叫建立測試設定檔。 深入了解 [Adobe Experience Platform檔案](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html){target=&quot;_blank&quot;}。

您必須使用包含「設定檔測試詳細資料」欄位群組的設定檔結構。 testProfile標幟是此欄位群組的一部分。
建立設定檔時，請務必傳遞值：testProfile = true。

請注意，您也可以更新現有的設定檔，將其testProfile標幟變更為「true」。

以下是建立測試設定檔的API呼叫範例：

```
curl -X POST \
'https://dcs.adobedc.net/collection/xxxxxxxxxxxxxx' \
-H 'Cache-Control: no-cache' \
-H 'Content-Type: application/json' \
-H 'Postman-Token: xxxxx' \
-H 'cache-control: no-cache' \
-H 'x-api-key: xxxxx' \
-H 'x-gw-ims-org-id: xxxxx' \
-d '{
"header": {
"msgType": "xdmEntityCreate",
"msgId": "xxxxx",
"msgVersion": "xxxxx",
"xactionid":"xxxxx",
"datasetId": "xxxxx",
"imsOrgId": "xxxxx",
"source": {
"name": "Postman"
},
"schemaRef": {
"id": "https://example.adobe.com/mobile/schemas/xxxxx",
"contentType": "application/vnd.adobe.xed-full+json;version=1"
}
},
"body": {
"xdmMeta": {
"schemaRef": {
"contentType": "application/vnd.adobe.xed-full+json;version=1"
}
},
"xdmEntity": {
"_id": "xxxxx",
"_mobile":{
"ECID": "xxxxx"
},
"testProfile":true
}
}
}'
```

## 作法影片 {#video}

了解如何建立測試設定檔。

>[!VIDEO](https://video.tv.adobe.com/v/334236?quality=12)
