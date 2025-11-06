---
title: 檢查並傳送直接郵件訊息
description: 瞭解如何在Journey Optimizer中檢查並傳送直接郵件訊息
feature: Direct Mail, Test Profiles, Preview
topic: Content Management
role: User
level: Beginner
keyword: direct, mail, configuration, direct-mail, provider
exl-id: 69a19190-d2e2-4858-a1df-ffd008226e2b
source-git-commit: c314d2e7a48f8eab1f32950e0e4e9056d11fd58b
workflow-type: tm+mt
source-wordcount: '460'
ht-degree: 7%

---

# 檢查並傳送直接郵件訊息 {#direct-mail-test-send}

## 預覽解壓縮檔案 {#preview-dm}

定義解壓縮檔案的內容後，您就可以使用測試設定檔來預覽。 如果您已插入個人化內容，您可以使用測試設定檔資料檢查此內容在訊息中的顯示方式。

若要這麼做，請按一下&#x200B;**[!UICONTROL 模擬內容]**，然後新增測試設定檔，以使用測試設定檔資料檢查擷取檔案的呈現方式。

![](assets/direct-mail-simulate.png){width="800" align="center"}

有關如何選取測試設定檔及預覽內容的詳細資訊，請參閱[內容管理](../content-management/preview-test.md)區段。

一旦檔案內容已準備好傳送，請關閉模擬熒幕，然後按一下&#x200B;**[!UICONTROL 檢閱以啟動]**&#x200B;按鈕。

## 驗證並啟用直接郵件行銷活動 {#dm-validate}

>[!IMPORTANT]
>
> 如果您的行銷活動受核准政策的約束，您將需要請求核准才能傳送您的直接郵件行銷活動。 [了解更多](../test-approve/gs-approval.md)

在啟用直接郵件行銷活動之前，請確定已正確設定行銷活動和擷取檔案。 若要這麼做，請檢查編輯器上半區段的警示。 其中一些是簡單的警告，但其他警告可能會阻止您傳送訊息。 可能會發生兩種型別的警報：警告和錯誤。

* **警告**&#x200B;參考建議和最佳實務。 例如，如果SMS訊息為空，則會顯示警告訊息。

* **錯誤**&#x200B;只要尚未解決，您就無法發佈行銷活動。 例如，當主旨行遺失時，錯誤訊息會警告您。

![](assets/direct-mail-review.png){width="800" align="center"}

當您的直接郵件行銷活動準備就緒時，請按一下&#x200B;**[!UICONTROL 啟動]**&#x200B;按鈕。 當行銷活動開始時，擷取檔案會自動產生，並匯出至[檔案路由設定](../direct-mail/direct-mail-configuration.md)中指定的伺服器。

>[!NOTE]
>
>匯出的檔案預設以換行結束。 這可確保與標準資料處理工具的相容性。


傳送後，您可以在行銷活動報表中測量直接郵件行銷活動的影響。 如需直接郵件報告的詳細資訊，請參閱[本節](../reports/campaign-global-report-cja-direct.md)。

## 管理直接郵件的同意 {#dm-consent-management}

請在 [!DNL Journey Optimizer] 中，同意交由體驗平台 [ 同意結構描述 ](https://experienceleague.adobe.com/docs/experience-platform/xdm/field-groups/profile/consents.html?lang=zh-Hant){target="_blank"} 處理。依預設，同意欄位的值是空的，並視為同意接收您的通訊。

如果設定檔已選擇不接收直接郵件，則在對應的Experience Platform設定檔屬性中，`consents.marketing.postalMail.val`的值將為`n`，且對應的設定檔將從後續傳遞中排除。

若要再次啟用，設定檔屬性必須變更回`consents.marketing.postalMail.val` ： `y`。

若要管理設定檔的屬性，請前往Experience Platform ，並透過選取身分名稱空間和對應的身分值來存取設定檔。 進一步瞭解 [Experience Platform 文件](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html?lang=zh-Hant#getting-started){target="_blank"}。

在[本節](../privacy/opt-out.md)中進一步瞭解如何在Journey Optimizer中管理選擇退出。
