---
title: 請求核准
description: 瞭解在發佈您的歷程與行銷活動之前，如何請求核准。
role: User
level: Beginner
feature: Approval
exl-id: 75dafecd-805d-4aa2-86c6-99e6da4d378b
TQID: https://experienceleague.adobe.com/UQ-5ddCbDJsF6muK1Am74fpx4ptRvHvB5VKwiIxd9d4
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: []
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
subfeature_v2:
  - id: bf7a266e-e483-42c6-b5bc-09ca6e49900c
source-git-commit: ad8f6662e1f2358071ae923d88630d5f34d9ccf3
workflow-type: tm+mt
source-wordcount: 476
ht-degree: 0%

---

# 請求核准 {#request-approval}

>[!BEGINSHADEBOX]

**在此頁面上：**&#x200B;將您的歷程或行銷活動傳送給正確的檢閱者，充滿信心地上線，並在檢閱期間保持控制 — 視需要取消、編輯和重新提交，因此只有經過核准的品牌內內容才能觸及您的客戶。

>[!ENDSHADEBOX]

存取核准工作流程取決於您的特定使用案例：

* **沒有使用中的核准原則**

   * **行銷活動**：如果沙箱中的行銷活動物件沒有有效的核准原則，行銷活動將會顯示&#x200B;**[!UICONTROL 啟用]**&#x200B;按鈕，可讓您在不需要核准的情況下啟用它們。

   * **歷程**：如果歷程物件沒有有效的核准原則，歷程會顯示&#x200B;**[!UICONTROL 發佈]**&#x200B;按鈕，讓您直接發佈。

* **存在使用中的核准原則**

   * **行銷活動**：如果沙箱中的Campaign物件存在一或多個作用中核准原則，則所述沙箱中的所有行銷活動都會顯示&#x200B;**[!UICONTROL 要求核准]**&#x200B;按鈕。
如果按一下&#x200B;**[!UICONTROL 請求核准]**&#x200B;按鈕時沒有核准原則套用至選取的物件，則會觸發自動核准工作流程。

   * **歷程**：如果沙箱中的Journey物件存在一或多個使用中的核准原則，則所有歷程都會顯示&#x200B;**[!UICONTROL 要求核准]**&#x200B;按鈕。
如果按一下&#x200B;**[!UICONTROL 請求核准]**&#x200B;按鈕時沒有核准原則套用至選取的物件，則會觸發自動核准工作流程。

## 傳送核准請求

建立行銷活動或歷程後，按一下&#x200B;**[!UICONTROL 要求核准]**&#x200B;按鈕。 這將檢查您的沙箱中是否有適用於行銷活動或歷程的有效核准原則。

* 如果找到適用的核准原則，則會傳送您的行銷活動或歷程以供檢閱。

* 如果按一下&#x200B;**[!UICONTROL 請求核准]**&#x200B;按鈕後，沒有任何核准原則適用於行銷活動或歷程，則行銷活動或歷程將會自動核准並啟動或發佈。

**[!UICONTROL 要求核准]**&#x200B;窗格開啟。 視需要提供訊息給核准者，然後按一下[傳送]&#x200B;**[!UICONTROL 以提交您的要求。]**

![核准要求對話方塊](assets/approval-request.png)

當行銷活動或歷程為&#x200B;**[!UICONTROL 稽核]**&#x200B;狀態時，您可以選擇取消核准請求。 按一下&#x200B;**[!UICONTROL 取消請求]**&#x200B;按鈕後，行銷活動或歷程將返回草稿階段，並傳送通知給稽核者，通知他們請求已取消。 然後，您可以進行必要的編輯，並重新提交行銷活動或歷程以進行核准。

![取消核准要求按鈕](assets/approval-cancel.png)

## 管理核准請求

將核准要求傳送給核准者後，他們便可以檢閱該要求，並啟動歷程/行銷活動使其上線，或視需要請求變更。 [瞭解如何檢閱及核准請求](review-approve-request.md)

如果核准者要求變更，系統會透過電子郵件和Journey Optimizer警示通知您；按一下畫面右上角的鈴鐺圖示，即可在&#x200B;**[!UICONTROL 要求]**&#x200B;索引標籤中存取該警示。

![已要求變更通知](assets/changes-requested.png)

若要處理變更請求，請從電子郵件或警報中將其開啟，以存取歷程或促銷活動，並進行請求的變更。 當您的歷程/行銷活動準備好再次接受檢閱時，請使用&#x200B;**[!UICONTROL 請求核准]**&#x200B;按鈕傳送新的核准請求。
