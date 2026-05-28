---
solution: Journey Optimizer
product: journey optimizer
title: 檢查並傳送直接郵件訊息
description: 瞭解如何在Journey Optimizer中檢查並傳送直接郵件訊息
feature: Direct Mail, Test Profiles, Preview
topic: Content Management
role: User
level: Beginner
keyword: direct, mail, configuration, direct-mail, provider
exl-id: 69a19190-d2e2-4858-a1df-ffd008226e2b
TQID: https://experienceleague.adobe.com/4GZKFKOx-D-RT1mssiV5vpmZQSJGVbGMro8Q-suhtPE
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2:
  - id: b3a93754-a8b8-46eb-9421-7eccaeeb3dff
  - id: f8d2e9f0-69c9-40cd-890f-71336c8dfff7
  - id: cb1f1586-9fb4-4de2-8332-02cebb88d42d
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 582
ht-degree: 15%

---

# 檢查並傳送直接郵件訊息 {#direct-mail-test-send}

瞭解如何在Journey Optimizer中預覽解壓縮檔案、驗證及啟用直接郵件行銷活動或歷程，以及管理郵遞區段同意。

## 開始之前 {#before-you-start}

在您測試並傳送直接郵件訊息之前，[請先建立訊息並設定解壓縮檔案](create-direct-mail.md)。 請確定您也已完成[直接郵件通道設定](direct-mail-configuration.md)。

## 預覽解壓縮檔案 {#preview-dm}

定義解壓縮檔案的內容後，您就可以使用測試設定檔來預覽。 如果您已插入個人化內容，您可以使用測試設定檔資料檢查此內容在訊息中的顯示方式。

若要這麼做，請按一下&#x200B;**[!UICONTROL 模擬內容]**，然後新增測試設定檔，以使用測試設定檔資料檢查擷取檔案的呈現方式。

![模擬直接郵件擷取檔案的內容預覽](assets/direct-mail-simulate.png){width="800" align="center"}

有關如何選取測試設定檔及預覽內容的詳細資訊，請參閱[內容管理](../content-management/preview-test.md)區段。

一旦檔案內容已準備好傳送，請關閉模擬熒幕，然後按一下&#x200B;**[!UICONTROL 檢閱以啟動]**&#x200B;按鈕。

## 驗證並啟用直接郵件行銷活動 {#dm-validate}

>[!IMPORTANT]
>
> 如果您的行銷活動受核准政策的約束，您將需要請求核准才能傳送您的直接郵件行銷活動。 [了解更多](../test-approve/gs-approval.md)

在啟用直接郵件行銷活動之前，請確定已正確設定行銷活動或歷程以及擷取檔案。 若要這麼做，請檢查編輯器上半區段的警示。 其中一些是簡單的警告，但其他警告可能會阻止您傳送訊息。 可能會發生兩種型別的警報：警告和錯誤。

* **警告**&#x200B;參考建議和最佳實務。 例如，如果SMS訊息為空，則會顯示警告訊息。

* **錯誤**&#x200B;只要尚未解決，您就無法發佈行銷活動。 例如，當主旨行遺失時，錯誤訊息會警告您。

![檢閱並啟動顯示直接郵件行銷活動驗證警示的畫面](assets/direct-mail-review.png){width="800" align="center"}

當您的直接郵件行銷活動準備就緒時，請完成您的[歷程](../building-journeys/journey-gs.md)或[行銷活動](../campaigns/create-campaign.md)的設定以進行傳送。

>[!NOTE]
>
>匯出的檔案預設以換行結束。 這可確保與標準資料處理工具的相容性。

傳送後，您可以在報告中測量直接郵件行銷活動或歷程的影響。 如需直接郵件報告的詳細資訊，請參閱下列章節：
* [直接郵件行銷活動報告](../reports/campaign-global-report-cja-direct.md)
* [直接郵件歷程報告](../reports/journey-global-report-cja-direct.md)

## 管理直接郵件的同意 {#dm-consent-management}

請在 [!DNL Journey Optimizer] 中，同意交由體驗平台 [&#x200B; 同意結構描述 &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/xdm/field-groups/profile/consents.html?lang=zh-Hant){target="_blank"} 處理。 預設情況下，如「同意」欄位值為空，則視為同意接受通訊。

如果設定檔已選擇不接收直接郵件，則在對應的Experience Platform設定檔屬性中，`consents.marketing.postalMail.val`的值將為`n`，且對應的設定檔將從後續傳遞中排除。

若要再次啟用，設定檔屬性必須變更回`consents.marketing.postalMail.val` ： `y`。

若要管理設定檔的屬性，請前往Experience Platform ，並透過選取身分名稱空間和對應的身分值來存取設定檔。 進一步瞭解 [Experience Platform 文件](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html?lang=zh-Hant#getting-started){target="_blank"}。

在[本節](../privacy/opt-out.md)中進一步瞭解如何在Journey Optimizer中管理選擇退出。

## 相關主題 {#related-topics}

* [開始使用直接郵件](get-started-direct-mail.md)
* [建立新的直接郵件訊息](create-direct-mail.md)
* [設定直接郵件頻道](direct-mail-configuration.md)
* [預覽和測試內容](../content-management/preview-test.md)

如需直接郵件的常見問題，請參閱[開始使用直接郵件](get-started-direct-mail.md)。
