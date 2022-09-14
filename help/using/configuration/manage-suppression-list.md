---
title: 管理隱藏清單
description: 了解如何存取及管理Journey Optimizer隱藏清單
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 430a2cd4-781d-4d37-a75d-405f5ed82377
source-git-commit: e81e21f714a3c5450defa1129e1e2b9969dc1de7
workflow-type: tm+mt
source-wordcount: '1212'
ht-degree: 1%

---

# 管理隱藏清單 {#manage-suppression-list}

使用 [!DNL Journey Optimizer]，您可以監控自動排除而無法傳送歷程的所有電子郵件地址，例如：

* 無效的地址（硬跳出）。
* 持續軟跳出的位址，如果您繼續將其納入傳送中，可能會對您的電子郵件信譽造成負面影響。
* 對您的其中一封電子郵件發出某種垃圾郵件投訴的收件人。

這些電子郵件地址會自動收集到Journey Optimizer **隱藏清單**. 進一步了解隱藏清單概念和在 [本節](../reports/suppression-list.md).

您也可以 [**手動** 添加地址或域](#add-addresses-and-domains) 到隱藏清單。

>[!NOTE]
>
>需要0到60分鐘才能 [!DNL Journey Optimizer] 考慮傳出電子郵件中隱藏的地址。

## 訪問隱藏清單 {#access-suppression-list}

若要存取排除的電子郵件地址的詳細清單，請前往 **[!UICONTROL 管理]** > **[!UICONTROL 管道]** > **[!UICONTROL 電子郵件設定]**，然後選取 **[!UICONTROL 隱藏清單]**.

>[!CAUTION]
>
>查看、導出和管理隱藏清單的權限限制為 [歷程管理員](../administration/ootb-product-profiles.md#journey-administrator). 深入了解管理 [!DNL Journey Optimizer] 中的使用者存取權限 [本節](../administration/permissions-overview.md).

![](assets/suppression-list-access.png)

篩選器可協助您瀏覽清單。

![](assets/suppression-list-filters.png)

您可以篩選 **[!UICONTROL 隱藏類別]**, **[!UICONTROL 地址類型]**，或 **[!UICONTROL 原因]**. 為每個條件選取您選取的選項。 選取後，您就可以清除每個篩選器，或清單頂端顯示的所有篩選器。

![](assets/suppression-list-filtering-example.png)

如果您手動錯誤新增電子郵件地址或網域， **[!UICONTROL 刪除]** 按鈕可以刪除該條目。

>[!CAUTION]
>
>絕不使用 **[!UICONTROL 刪除]** 按鈕，移除隱藏的電子郵件地址或網域。

![](assets/suppression-list-delete.png)

從隱藏清單中刪除電子郵件地址或網域，表示您將重新開始傳送至此地址或網域。 因此，這可能會對您的傳遞能力和IP信譽造成嚴重影響，最終可能導致您的IP位址或傳送網域遭到封鎖。 進一步了解維護隱藏清單在 [本節](../reports/suppression-list.md).

>[!NOTE]
>
>考慮刪除任何電子郵件地址或網域時，請格外小心。 如有疑問，請聯絡傳遞能力專家。

從 **[!UICONTROL 隱藏清單]** 視圖中，也可以編輯隱藏規則。 [了解更多](retries.md)

要將隱藏清單導出為CSV檔案，請選擇 **[!UICONTROL 下載CSV]** 按鈕。

![](assets/suppression-list-download-csv.png)

## 隱藏類別和原因 {#suppression-categories-and-reasons}

當郵件無法傳遞至電子郵件地址時， [!DNL Journey Optimizer] 判斷傳送失敗的原因，並將其與 **[!UICONTROL 隱藏類別]**.

隱藏類別如下：

* **硬**:會立即將電子郵件地址發送到隱藏清單。

   >[!NOTE]
   >
   >當錯誤是垃圾郵件投訴的結果時，它也會落入 **硬** 類別。 發出投訴的收件人的電子郵件地址會立即發送到壓制清單。

* **軟**:一旦錯誤計數器達到限制臨界值，軟錯誤就會將地址發送到隱藏清單。 [重試時了解更多](retries.md)

* **手動**:您也可以手動將電子郵件地址或網域新增至隱藏清單。 [了解更多](#add-addresses-and-domains)

>[!NOTE]
>
>進一步了解軟退信和硬退信，位於 [傳送失敗類型](../reports/suppression-list.md#delivery-failures) 區段。

對於所列的每個電子郵件地址，您也可以檢查 **[!UICONTROL 類型]** （電子郵件或網域）, **[!UICONTROL 原因]** 排除、新增者，以及新增至隱藏清單的日期/時間。

![](assets/suppression-list.png)

傳送失敗的可能原因有：

| 原因 | 說明 | 隱藏類別 |
| --- | --- | --- |
| **[!UICONTROL 收件者無效]** | 收件者無效或不存在。 | 硬 |
| **[!UICONTROL 軟跳出]** | 消息軟退信的原因不是此表中列出的軟錯誤，例如當發送超過ISP建議的允許速率時。 | 軟 |
| **[!UICONTROL DNS失敗]** | 由於DNS失敗而退信。 | 軟 |
| **[!UICONTROL 郵箱已滿]** | 由於收件者的信箱已滿而無法接受更多訊息，訊息已退信。 | 軟 |
| **[!UICONTROL 拒絕中繼]** | 由於不允許中繼，因此接收器阻止了該消息。 | 軟 |
| **[!UICONTROL 挑戰 — 響應]** | 該消息是挑戰 — 響應探測。 | 軟 |
| **[!UICONTROL 垃圾郵件投訴]** | 由於收件者將郵件標示為垃圾訊息，因此已封鎖訊息。 | 硬 |

>[!NOTE]
>
>取消訂閱的使用者不會收到來自 [!DNL Journey Optimizer]，因此其電子郵件地址無法傳送至隱藏清單。 其選項會在Experience Platform層級處理。 [進一步了解選擇退出](../messages/consent.md)

## 手動新增地址和網域 {#add-addresses-and-domains}

>[!CONTEXTUALHELP]
>id="ajo_admin_suppression_list_header"
>title="將電子郵件或網域新增至隱藏清單"
>abstract="您可以手動填入Journey Optimizer隱藏清單，從您的傳送中排除特定的電子郵件地址和/或網域。"

>[!CONTEXTUALHELP]
>id="ajo_admin_suppression_list"
>title="將電子郵件或網域新增至隱藏清單"
>abstract="若要填入Journey Optimizer隱藏清單，您可以手動新增電子郵件地址或網域 — 一次新增一個，或透過CSV檔案上傳以大量模式新增。 您的傳送將排除這些特定電子郵件地址和/或網域。"

當郵件無法傳遞至電子郵件地址時，系統會根據定義的隱藏規則或退信計數，自動將此地址新增至隱藏清單。

不過，您也可以手動填入 [!DNL Journey Optimizer] 隱藏清單，從您的傳送中排除特定的電子郵件地址和/或網域。

您可以新增電子郵件地址或網域 [一次一個](#add-one-address-or-domain)，或 [在大量模式中](#upload-csv-file) 透過CSV檔案上傳。

若要這麼做，請選取 **[!UICONTROL 新增電子郵件或網域]** 按鈕，然後遵循以下方法之一。

![](assets/suppression-list-add-email.png)

### 添加一個地址或域 {#add-one-address-or-domain}

>[!CONTEXTUALHELP]
>id="ajo_admin_suppression_list_address"
>title="將一個項添加到隱藏清單"
>abstract="您可以逐一新增電子郵件地址和/或網域，以填入隱藏清單。"

1. 選取 **[!UICONTROL 逐一]** 選項。

   ![](assets/suppression-list-add-email-address.png)

1. 選擇地址類型： **[!UICONTROL 電子郵件地址]** 或 **[!UICONTROL 網域位址]**.

1. 輸入要從傳送中排除的電子郵件地址或網域。

   >[!NOTE]
   >
   >請務必輸入有效的電子郵件地址(如abc@company.com)或網域（如abc.company.com）。

1. 視需要指定原因。

   >[!NOTE]
   >
   >在 **[!UICONTROL 原因]** 欄位。 您可以在 [本頁](https://en.wikipedia.org/wiki/Wikipedia:ASCII#ASCII_printable_characters)例如{target=&quot;_blank&quot;}。

1. 按一下&#x200B;**[!UICONTROL 提交]**。

### 上傳CSV檔案 {#upload-csv-file}

>[!CONTEXTUALHELP]
>id="ajo_admin_suppression_list_csv"
>title="上傳CSV以新增項目至隱藏清單"
>abstract="您可以上傳填入您要排除的電子郵件地址/網域的CSV檔案，以填入隱藏清單。"

1. 選取 **[!UICONTROL 上傳CSV]** 選項。

   ![](assets/suppression-list-upload-csv.png)

1. 下載要使用的CSV範本，其中包含下列欄和格式：

   ```
   TYPE,VALUE,COMMENT
   EMAIL,abc@somedomain.com,Comment
   DOMAIN,somedomain.com,Comment
   ```
   >[!NOTE]
   >
   >在 **註解** 欄。 您可以在 [本頁](https://en.wikipedia.org/wiki/Wikipedia:ASCII#ASCII_printable_characters)例如{target=&quot;_blank&quot;}。

   您也可以從 **[!UICONTROL 隱藏清單]** 主檢視。

   >[!CAUTION]
   >
   >請勿變更CSV範本中的欄名稱。
   >
   >檔案大小不應超過1 MB。

1. 在CSV範本中填入您要新增至隱藏清單的電子郵件地址和/或網域。

1. 完成後，拖放CSV檔案，然後按一下 **[!UICONTROL 提交]**.

   ![](assets/suppression-list-upload-csv-submit.png)

>[!NOTE]
>
>上傳完成後，請從介面檢查狀態，以確定上傳成功。 [了解如何](#recent-uploads)

### 檢查最近的上載狀態 {#recent-uploads}

您可以檢查您上傳的最新CSV檔案清單。

若要這麼做，請從 **[!UICONTROL 隱藏清單]** 檢視，按一下 **[!UICONTROL 最近上載]** 按鈕。

![](assets/suppression-list-recent-uploads-button.png)

系統會顯示您提交的最新上傳內容及其對應狀態。

如果錯誤報告與檔案相關聯，您可以下載該報告以檢查遇到的錯誤。

![](assets/suppression-list-recent-uploads-error.png)

以下是可在錯誤報表中找到的項目類型範例：

```
type,value,comments,failureReason
Email,examplemail.com,MANUAL,Invalid format for value: examplemail.com
Email,examplemail,MANUAL,Invalid format for value: examplemail
Email,example@mail,MANUAL,Invalid format for value: example@mail
Domain,example,MANUAL,Invalid format for value: example
Domain,example.!com,MANUAL,Invalid format for value: example.!com
Domain,!examplecom,MANUAL,Invalid format for value: !examplecom
```
