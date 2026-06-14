---
solution: Journey Optimizer
product: journey optimizer
title: 檢查並傳送推播通知
description: 瞭解如何在Journey Optimizer中檢查並傳送推播通知
feature: Push
topic: Content Management
role: User
level: Beginner
exl-id: aad4e08a-3369-454d-9e32-974347a3b393
TQID: https://experienceleague.adobe.com/QXJ9G3btsn7ZEwSB2Bm0uGt89gsh8D7SnNZ-Vw2muXM
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2: id: b3a93754-a8b8-46eb-9421-7eccaeeb3dffid: f8d2e9f0-69c9-40cd-890f-71336c8dfff7id: c96d2aa5-76a2-443d-8d23-5de95577c909
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: 28eeed0d2b5dc3054c57004ead01de32151ab743
workflow-type: tm+mt
source-wordcount: 411
ht-degree: 6%

---

# 檢查並傳送推播通知 {#send-push}

>[!BEGINSHADEBOX]

**在此頁面上：**&#x200B;瞭解如何在Adobe Journey Optimizer中預覽、驗證及傳送推播通知。

>[!ENDSHADEBOX]

## 預覽推播通知 {#preview-push}

定義訊息內容後，您可以使用任一模擬方法來預覽其內容：

* 按一下&#x200B;**[!UICONTROL 模擬內容]**&#x200B;以測試內容變數與範例輸入資料或AI自動產生。 [瞭解如何模擬內容變化](../test-approve/simulate-sample-input.md)
* 按一下&#x200B;**[!UICONTROL 模擬內容]**，然後從下拉式清單中選取&#x200B;**[!UICONTROL 模擬內容（AEP設定檔）]**，以使用測試設定檔預覽。 然後，您可以選取要預覽內容的裝置型別： **[!UICONTROL iOS]**、**[!UICONTROL Android]**&#x200B;或&#x200B;**[!UICONTROL 網頁]**。

![](assets/push_preview_3.png)

有關如何預覽及測試內容的詳細資訊，請參閱[內容管理](../content-management/preview-test.md)區段。

## 驗證推播通知 {#push-validate}

您必須檢查編輯器上半區段的警示。 其中一些是簡單的警告，但其他警告可能會阻止您傳送訊息。 可能會發生兩種型別的警報：警告和錯誤。

* **警告**&#x200B;參考建議和最佳實務。

* **錯誤**&#x200B;會阻止您測試或啟用歷程，只要這些錯誤尚未解決，例如：

   * **[!UICONTROL 訊息的推播版本是空的]**：當缺少推播通知本文或標題時，會顯示此錯誤。 瞭解如何在[本節](create-push.md)中定義推播通知內容。

   * **[!UICONTROL 設定不存在]**：如果您選取的設定在建立訊息之後被刪除，則無法使用訊息。 如果發生此錯誤，請在訊息&#x200B;**[!UICONTROL 屬性]**&#x200B;中選取其他設定。 在[本節](../configuration/channel-surfaces.md)中進一步瞭解通道設定。

   * **[!UICONTROL 推播iOS/Android承載已超過4KB的限制]**：推播通知大小不能超過4KB。 為遵守此限制，請嘗試減少使用影像或表情符號。 在[本節](../push/create-push.md)中瞭解如何管理推播通知內容。

  ![](assets/push_alert.png)


>[!NOTE]
>
> 為了提供更好的傳遞能力，您應該一律使用提供者支援格式的電話號碼。 例如，Twilio和Sinch只支援E.164格式的電話號碼。

## 傳送推播通知{#push-send}

>[!IMPORTANT]
>
> 如果您的行銷活動受核准原則的約束，您將需要請求核准才能傳送推播通知。 [了解更多](../test-approve/gs-approval.md)

當您的推送訊息就緒時，請完成您的[歷程](../building-journeys/journey-gs.md)或[行銷活動](../campaigns/create-campaign.md)的設定以傳送。

**相關主題**

* [設定行動裝置的推播頻道](push-configuration.md)
* [設定網頁的推播通道](push-configuration-web.md)
* [推播通知報告](../reports/journey-global-report-cja-push.md)
* [建立推播通知](create-push.md)
* [在歷程中新增訊息](../building-journeys/journey-action.md)
* [在行銷活動中新增訊息](../campaigns/create-campaign.md)

