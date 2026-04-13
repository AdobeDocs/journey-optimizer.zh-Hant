---
solution: Journey Optimizer
product: journey optimizer
title: 更新設定檔
description: 瞭解如何在歷程中使用更新設定檔活動
feature: Journeys, Profiles, Activities
topic: Content Management
role: User
level: Intermediate
keywords: 設定檔，更新，歷程，活動
exl-id: 8b2b2d1e-9bd1-439d-a15e-acdbab387c4b
version: Journey Orchestration
source-git-commit: 5383e0af430188dadd3e9ee259253115f7f1992d
workflow-type: tm+mt
source-wordcount: '862'
ht-degree: 4%

---

# 更新設定檔 {#update-profile}

>[!CONTEXTUALHELP]
>id="ajo_journey_update_profiles"
>title="更新設定檔活動"
>abstract="更新輪廓的動作活動可讓您利用來自事件的資訊、資料源或使用特定值來更新現有的 [!DNL Adobe Experience Platform] 輪廓。"

當客戶進行歷程時，請使用&#x200B;**[!UICONTROL 更新設定檔]**&#x200B;動作活動來擴充或修正現有的[!DNL Adobe Experience Platform]設定檔。 您可以設定來源為歷程事件、已設定資料來源或靜態值的欄位值，讓您在不離開歷程畫布的情況下保持設定檔資料的正確和可操作。 在設定此活動之前，請先檢閱適用的[護欄和限制](#guardrails)。

## 資料集選取範圍 {#dataset-selection}

**[!UICONTROL 更新設定檔]**&#x200B;活動需要專用的資料集來儲存更新。 由於此活動只會更新[設定檔存放區](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=zh-Hant#profile-data-store){target="_blank"} （而非Datalake），所有更新應該儲存在專為[更新設定檔](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/catalog/datasets/user-guide#enable-profile){target="_blank"}動作指定的&#x200B;**[!UICONTROL 設定檔啟用資料集]**&#x200B;中。

>[!CAUTION]
>
>請勿使用也用於批次或串流擷取的資料集。 其他內嵌執行將會覆寫&#x200B;**[!UICONTROL 更新設定檔]**&#x200B;動作所做的變更，導致設定檔屬性消失或回覆成先前的值。 如果您觀察到此行為，請在Adobe Experience Platform中確認沒有其他擷取將寫入相同的資料集。 如需疑難排解步驟，請參閱[解決Adobe Journey Optimizer中的設定檔更新失敗](https://experienceleague.adobe.com/zh-hant/docs/experience-cloud-kcs/kbarticles/ka-26352){target="_blank"}。

此外，**[!UICONTROL 更新設定檔]**&#x200B;活動設定不需要[身分名稱空間](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/identity/features/namespaces){target="_blank"}。 因此，請確定選取的資料集使用啟動歷程的動作所使用的相同&#x200B;**[!UICONTROL 身分名稱空間]**，因為這是這些更新將使用的名稱空間。 身分對應也可以由選取的資料集使用。 若未選取具有正確識別名稱空間或使用識別對應的資料集，將導致&#x200B;**[!UICONTROL 更新設定檔]**&#x200B;活動失敗。

## 設定更新設定檔活動 {#use-profile-update}

請依照下列步驟，在您的歷程中設定&#x200B;**[!UICONTROL 更新設定檔]**&#x200B;活動。

1. 開始設計您的歷程。 深入瞭解[建立您的第一個歷程](../building-journeys/journey-gs.md)。

1. 在調色盤的&#x200B;**[!UICONTROL 動作]**&#x200B;區段中，將&#x200B;**[!UICONTROL 更新設定檔]**&#x200B;活動拖放到畫布中。

   ![更新歷程浮動視窗中動作](assets/profileupdate0.png)下的設定檔活動

1. 從清單中選取結構描述。

   >[!NOTE]
   >
   >只有已存在於所選XDM設定檔結構描述中的欄位才可供選取。 如果您需要的欄位未列出，請先將其新增到Adobe Experience Platform中的結構描述。

1. 按一下&#x200B;**[!UICONTROL 欄位]**&#x200B;以選取要更新的欄位。

   ![選取要更新的欄位](assets/profileupdate2.png)

1. 從清單中選取資料集。

   >[!NOTE]
   >
   >**[!UICONTROL 更新設定檔]**&#x200B;動作會即時更新設定檔資料，但不會更新資料集。 需要選取資料集，因為設定檔是和資料集相關的記錄。

1. 按一下&#x200B;**[!UICONTROL 值]**&#x200B;欄位以定義您要使用的值：

   * 使用簡單運算式編輯器，您可以從資料來源或傳入事件中選取欄位。

     設定檔屬性更新的![簡單模式欄位選擇器](assets/profileupdate4.png)

   * 若要定義特定值或運用進階函式，請選取[**[!UICONTROL 進階模式]**](expression/expressionadvanced.md)。

     複雜設定檔更新的![進階模式運算式編輯器](assets/profileupdate3.png)

1. 若要更新相同動作中的其他設定檔屬性，請按一下&#x200B;**[!UICONTROL 更新其他欄位]**，然後重複選取欄位和值。 您最多可以在單一&#x200B;**[!UICONTROL 更新設定檔]**&#x200B;動作中新增五個欄位/值組。 請參閱[護欄和限制](#guardrails)。

**[!UICONTROL 更新設定檔]**&#x200B;活動現已設定完成。

![歷程中的設定檔更新活動具有多個欄位設定](assets/profileupdate1.png)


## 測試設定檔更新 {#using-the-test-mode}

請注意，在[測試模式](testing-the-journey.md)中，設定檔更新會立即在測試設定檔上生效，而且不會模擬。

只有測試設定檔才能進入歷程測試模式。 您可以建立新的測試設定檔，或將現有的設定檔轉換為測試設定檔。 在[!DNL Adobe Experience Platform]中，可透過CSV檔案匯入或API呼叫更新設定檔屬性。 更快速的替代方式是在歷程本身中使用&#x200B;**[!UICONTROL 更新設定檔]**&#x200B;活動，將測試設定檔布林欄位設為true。

有關如何將現有設定檔轉換為測試設定檔的詳細資訊，請參閱此[區段](../audience/creating-test-profiles.md#create-test-profiles-csv)。

## 護欄與限制 {#guardrails}

* **[!UICONTROL 更新設定檔]**&#x200B;動作只能用於具有[名稱空間](../event/about-creating.md#select-the-namespace)的歷程。
* 動作只會更新現有欄位，不會建立新的設定檔欄位。
* 動作僅支援簡單欄位型別（字串、數字、布林值）。 不支援定義為分項清單、建議值、物件陣列或複雜集合（例如產品清單）的XDM欄位。
* 您無法使用&#x200B;**[!UICONTROL 更新設定檔]**&#x200B;動作來產生[體驗事件](../event/about-events.md)，例如購買。
* 如同任何其他動作，您可以定義[替代路徑，以防發生錯誤或逾時](using-the-journey-designer.md#paths)。 兩個動作無法並行放置。
* 不保證個人資料更新可立即用於相同歷程的下游。 請避免在寫入欄位的&#x200B;**[!UICONTROL 更新設定檔]**&#x200B;動作之後直接放置讀取欄位的動作，因為更新值可能尚未反映出來。
* **[!UICONTROL 更新設定檔]**&#x200B;活動只會更新[設定檔存放區](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=zh-Hant#profile-data-store){target="_blank"}，不會更新Data Lake。
* 單一&#x200B;**[!UICONTROL 更新設定檔]**&#x200B;動作中最多可更新五個欄位/值組。 使用&#x200B;**[!UICONTROL 更新其他欄位]**&#x200B;按鈕以新增更多配對。
* 為獲得更好的效能，請將多個屬性更新群組為單一&#x200B;**[!UICONTROL 更新設定檔]**&#x200B;動作，而不是為每個屬性使用一個動作。
