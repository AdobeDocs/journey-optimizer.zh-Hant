---
title: 建立測試設定檔
description: 了解如何建立測試設定檔
feature: Journeys
topic: 內容管理
role: User
level: Intermediate
source-git-commit: 8f77802fcaa23790f9de4e8f15e593643b13fb1e
workflow-type: tm+mt
source-wordcount: '1318'
ht-degree: 1%

---

# 建立測試設定檔{#create-test-profiles}

使用測試模式時需要測試設定檔了解如何在歷程中使用[測試模式](../building-journeys/testing-the-journey.md)，以及[預覽和測試您的訊息](../preview.md)。

建立測試設定檔的可用方法詳述如下：

* 您可以將[現有的設定檔](#turning-profile-into-test)轉換為測試設定檔

* 您可以上傳[csv檔案](#create-test-profiles-csv)或使用[API呼叫](#create-test-profiles-api)來建立測試設定檔。 除了這兩種方法以外，Adobe Journey Optimizer還隨附特定的[產品內使用案例](#use-case-1)以利建立測試設定檔。

* 您也可以上傳資料集中的JSON檔案。 如需詳細資訊，請參閱[資料擷取檔案](https://experienceleague.adobe.com/docs/experience-platform/ingestion/tutorials/ingest-batch-data.html#add-data-to-dataset)。

請注意，建立測試設定檔與在Adobe Experience Platform中建立一般設定檔類似。 如需詳細資訊，請參閱[即時客戶設定檔檔案](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html)。

## 先決條件 {#test-profile-prerequisites}

若要建立設定檔，您必須先在[!DNL Journey Optimizer]Adobe中建立結構和資料集。

首先，您需要&#x200B;**建立架構**。 請依照下列步驟操作：

1. 在「資料管理」菜單部分，按一下&#x200B;**[!UICONTROL Schemas]**。
   ![](../assets/test-profiles-0.png)
1. 按一下右上方的&#x200B;**[!UICONTROL Create schema]**，然後選取架構類型，例如&#x200B;**XDM個別設定檔**。
   ![](../assets/test-profiles-1.png)
1. 選擇適當的欄位組。 請務必新增&#x200B;**設定檔測試詳細資料**欄位群組。
   ![](../assets/test-profiles-1-ter.png)
完成後，按一下 **[!UICONTROL Add field groups]**:欄位組清單將顯示在架構概述螢幕上。
   ![](../assets/test-profiles-2.png)

   >[!NOTE]
   >
   >* 按一下架構的名稱以變更並更新其屬性。
      >
      >
   * 按一下「欄位組」部分中的&#x200B;**[!UICONTROL Add]**&#x200B;按鈕，選擇要添加到架構中的其他欄位組


1. 在欄位清單中，按一下您要定義為主要身分的欄位。
   ![](../assets/test-profiles-3.png)
1. 在&#x200B;**[!UICONTROL Field properties]**&#x200B;右窗格中，檢查&#x200B;**[!UICONTROL Identity]**&#x200B;和&#x200B;**[!UICONTROL Primary Identity]**&#x200B;選項並選擇命名空間。 如果您希望主要身分成為電子郵件地址，請選擇&#x200B;**[!UICONTROL Email]**&#x200B;命名空間。 按一下「**[!UICONTROL Apply]**」。
   ![](../assets/test-profiles-4bis.png)
1. 選擇架構並在&#x200B;**[!UICONTROL Schema properties]**&#x200B;窗格中啟用&#x200B;**[!UICONTROL Profile]**選項。
   ![](../assets/test-profiles-5.png)
1. 按一下「**儲存**」。

>[!NOTE]
>
>有關架構建立的詳細資訊，請參閱[XDM檔案](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/resources/schemas.html#prerequisites)。

然後，您需要&#x200B;**建立要匯入設定檔的資料集**。 請依照下列步驟操作：

1. 瀏覽至&#x200B;**[!UICONTROL Datasets]**，然後按一下&#x200B;**[!UICONTROL Create dataset]**。
   ![](../assets/test-profiles-6.png)
1. 選擇&#x200B;**[!UICONTROL Create dataset from schema]**。
   ![](../assets/test-profiles-7.png)
1. 選取先前建立的架構，然後按一下&#x200B;**[!UICONTROL Next]**。
   ![](../assets/test-profiles-8.png)
1. 選擇名稱，然後按一下&#x200B;**[!UICONTROL Finish]**。
   ![](../assets/test-profiles-9.png)
1. 啟用&#x200B;**[!UICONTROL Profile]**選項。
   ![](../assets/test-profiles-10.png)

>[!NOTE]
>
> 如需資料集建立的詳細資訊，請參閱[目錄服務檔案](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html#getting-started)。

## 產品內使用案例{#use-case-1}

從Adobe Journey Optimizer首頁，您可以運用產品中的測試設定檔使用案例。 此使用案例有助於建立測試設定檔，以在發佈前測試歷程。

![](../assets/use-cases-home.png)

按一下&#x200B;**[!UICONTROL Begin]**&#x200B;按鈕以開始使用案例。

需要下列資訊：

1. **身分命名空間**:用來 [唯一](https://experienceleague.adobe.com/docs/experience-platform/identity/namespaces.html) 識別測試設定檔的身分名稱。例如，如果使用電子郵件來識別測試設定檔，則應選取身分命名空間&#x200B;**Email**。 如果唯一識別碼是電話號碼，則應選取身分命名空間&#x200B;**Phone**。

2. **CSV檔案**:以逗號分隔的檔案，包含要建立的測試設定檔清單。使用案例需要CSV檔案的預先定義格式，其中包含要建立的測試設定檔清單。 檔案中的每一列都應以下列正確順序包含下列欄位：

   1. **人員Id**:測試設定檔的唯一識別碼。此欄位的值應反映所選取的身分命名空間。 (例如，如果為身分命名空間選取了&#x200B;**Phone**，則此欄位的值應為電話號碼。 同樣地，如果選取&#x200B;**Email**，則此欄位的值應為電子郵件)
   1. **電子郵件**:測試設定檔電子郵件地址。（如果選取&#x200B;**Email**&#x200B;作為身分命名空間，**人員ID**&#x200B;欄位和&#x200B;**電子郵件**&#x200B;欄位可能會包含相同的值）
   1. **名字**:測試設定檔名。
   1. **姓氏**:測試設定檔的姓氏。
   1. **城市**:測試配置檔案居住城市
   1. **國家**:測試設定檔居住國
   1. **性別**:測試設定檔性別。可用值為&#x200B;**male**、**femole**&#x200B;和&#x200B;**non_specified**

選取身分命名空間並根據上述格式提供CSV檔案後，按一下右上角的&#x200B;**[!UICONTROL Run]**&#x200B;按鈕。 使用案例可能需要幾分鐘的時間才能完成。 使用案例完成處理並建立測試設定檔後，系統會傳送通知以通知使用者。

>[!NOTE]
>
>測試設定檔可能會覆寫現有設定檔。 執行使用案例之前，請確定CSV僅包含測試設定檔，並針對正確的沙箱執行。

## 將設定檔轉換為測試設定檔{#turning-profile-into-test}

您可以將現有設定檔轉換為測試設定檔：您可以使用建立設定檔時的相同方式更新設定檔屬性。

最簡單的方法是在歷程中使用&#x200B;**[!UICONTROL Update Profile]**&#x200B;動作活動，並將testProfile布林欄位從false變更為true。

您的歷程將由&#x200B;**[!UICONTROL Read Segment]**&#x200B;和&#x200B;**[!UICONTROL Update Profile]**&#x200B;活動組成。 您首先需要建立以您要轉換成測試設定檔的設定檔為目標的區段。

>[!NOTE]
>
> 由於您將更新&#x200B;**testProfile**&#x200B;欄位，所選設定檔必須包含此欄位。 相關架構必須具有&#x200B;**設定檔測試詳細資料**&#x200B;欄位群組。 請參閱[本節](../building-journeys/creating-test-profiles.md#test-profiles-prerequisites)。

1. 瀏覽至右上方的&#x200B;**區段**，然後瀏覽&#x200B;**建立區段**。
   ![](../assets/test-profiles-22.png)
1. 定義區段名稱並建立區段：選擇欄位和值，以定位您想要的設定檔。
   ![](../assets/test-profiles-23.png)
1. 按一下&#x200B;**儲存**並檢查設定檔是否已由區段正確定位。
   ![](../assets/test-profiles-24.png)

   >[!NOTE]
   >
   > 區段計算可能需要一些時間。 進一步了解[此區段](../segment/about-segments.md)中的區段。

1. 現在，請建立新的歷程，並從&#x200B;**[!UICONTROL Read Segment]**&#x200B;協調活動開始。
1. 選擇先前建立的區段以及您的設定檔使用的命名空間。
   ![](../assets/test-profiles-25.png)
1. 新增&#x200B;**[!UICONTROL Update Profile]**&#x200B;動作活動。
1. 選取結構、**testProfiles**&#x200B;欄位、資料集，並將值設為&#x200B;**True**。 要執行此操作，請在&#x200B;**[!UICONTROL VALUE]**&#x200B;欄位中按一下右側的&#x200B;**Pen**&#x200B;表徵圖，選擇&#x200B;**[!UICONTROL Advanced mode]**&#x200B;並輸入&#x200B;**true**。
   ![](../assets/test-profiles-26.png)
1. 新增&#x200B;**End**&#x200B;活動，然後按一下&#x200B;**[!UICONTROL Publish]**。
1. 在&#x200B;**[!UICONTROL Segments]**區段中，檢查設定檔是否已正確更新。
   ![](../assets/test-profiles-28.png)

   >[!NOTE]
   >
   > 有關&#x200B;**[!UICONTROL Update Profile]**&#x200B;活動的詳細資訊，請參閱[此部分](../building-journeys/update-profiles.md)。

## 使用csv檔案{#create-test-profiles-csv}建立測試設定檔

在Adobe Experience Platform中，您可以將包含不同設定檔欄位的csv檔案上傳至資料集，以建立設定檔。 這是最簡單的方法。

1. 使用試算表軟體建立簡單的csv檔案。
1. 為每個需要的欄位新增一欄。 請務必新增主要身分欄位（上述範例中為「personID」），以及設為「true」的「testProfile」欄位。
   ![](../assets/test-profiles-11.png)
1. 為每個設定檔新增一行，並填入每個欄位的值。
   ![](../assets/test-profiles-12.png)
1. 將試算表儲存為CSV檔案。 請確定逗號是分隔符號。
1. 瀏覽至Adobe Experience Platform **Workflows**。
   ![](../assets/test-profiles-14.png)
1. 選擇「**將CSV對應至XDM架構」**，然後按一下「**Launch**」。
   ![](../assets/test-profiles-16.png)
1. 選取您要將設定檔匯入的資料集。 按&#x200B;**「下一步」**。
   ![](../assets/test-profiles-17.png)
1. 按一下「**選擇檔案**」並選取您的csv檔案。 上傳檔案時，按一下&#x200B;**Next**。
   ![](../assets/test-profiles-18.png)
1. 將源csv欄位映射到架構欄位，然後按一下&#x200B;**完成**。
   ![](../assets/test-profiles-19.png)
1. 資料匯入開始。 狀態會從&#x200B;**Processing**&#x200B;移至&#x200B;**Success**。 按一下右上方的&#x200B;**預覽資料集** 。
   ![](../assets/test-profiles-20.png)
1. 檢查測試設定檔是否已正確新增。
   ![](../assets/test-profiles-21.png)

系統會新增您的測試設定檔，現在可用於測試歷程。 請參閱[本節](../building-journeys/testing-the-journey.md)。
>[!NOTE]
>
> 如需csv匯入的詳細資訊，請參閱[資料擷取檔案](https://experienceleague.adobe.com/docs/experience-platform/ingestion/tutorials/map-a-csv-file.html#tutorials)。

## 使用API呼叫{#create-test-profiles-api}建立測試設定檔

您也可以透過API呼叫建立測試設定檔。 了解更多資訊，請參閱此[page](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html)。

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
