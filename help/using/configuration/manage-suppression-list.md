---
title: 管理禁止顯示清單
description: 瞭解如何訪問和管理Journey Optimizer禁止清單
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 430a2cd4-781d-4d37-a75d-405f5ed82377
source-git-commit: 0ca491315e214e3c12bec11a93da1a2b98b493b6
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 管理禁止顯示清單 {#manage-suppression-list}

與 [!DNL Journey Optimizer]，您可以監視在行程中自動排除發送的所有電子郵件地址，例如：

* 無效的地址（硬邊界）。
* 始終軟彈跳的地址，如果繼續將其包括在交貨中，可能會對您的電子郵件聲譽產生負面影響。
* 對您的電子郵件發出某種垃圾郵件投訴的收件人。

這些電子郵件地址自動收集到Journey Optimizer **隱藏清單**。 瞭解有關禁止顯示清單概念和中使用的詳細資訊 [此部分](../reports/suppression-list.md)。

您也可以 [**手動** 添加地址或域](#add-addresses-and-domains) 到禁止清單。

>[!NOTE]
>
>需要0到60分鐘 [!DNL Journey Optimizer] 考慮傳出電子郵件中隱藏的地址。

## 訪問禁止顯示清單 {#access-suppression-list}

要訪問排除的電子郵件地址的詳細清單，請轉到 **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Email configuration]**，然後選擇 **[!UICONTROL Suppression list]**。

>[!CAUTION]
>
>查看、導出和管理禁止顯示清單的權限限制為 [旅程管理員](../administration/ootb-product-profiles.md#journey-administrator)。 瞭解有關管理的更多資訊 [!DNL Journey Optimizer] 用戶在 [此部分](../administration/permissions-overview.md)。

![](assets/suppression-list-access.png)

篩選器可幫助您瀏覽清單。

![](assets/suppression-list-filters.png)

可以在 **[!UICONTROL Suppression category]**。 **[!UICONTROL Address type]**&#x200B;或 **[!UICONTROL Reason]**。 為每個條件選擇所選選項。 選中後，可以清除清單頂部顯示的每個篩選器或所有篩選器。

![](assets/suppression-list-filtering-example.png)

如果您手動添加電子郵件地址或域時出錯， **[!UICONTROL Delete]** 按鈕可以刪除該條目。

>[!CAUTION]
>
>從不使用 **[!UICONTROL Delete]** 按鈕以刪除隱藏的電子郵件地址或域。

![](assets/suppression-list-delete.png)

從禁止顯示清單中刪除電子郵件地址或域意味著您將再次開始傳送到此地址或域。 因此，這會對您的可交付性和IP信譽造成嚴重影響，最終可能導致您的IP地址或發送域被阻止。 瞭解有關在中維護禁止顯示清單的重要性的更多資訊 [此部分](../reports/suppression-list.md)。

>[!NOTE]
>
>考慮刪除任何電子郵件地址或域時，請格外小心。 如有任何疑問，請與交付能力專家聯繫。

從 **[!UICONTROL Suppression list]** 視圖，您也可以編輯隱藏規則。 [了解更多](retries.md)

要將禁止顯示清單導出為CSV檔案，請選擇 **[!UICONTROL Download CSV]** 按鈕

![](assets/suppression-list-download-csv.png)

## 隱藏類別和原因 {#suppression-categories-and-reasons}

當郵件無法傳遞到電子郵件地址時， [!DNL Journey Optimizer] 確定交貨失敗的原因，並將其與 **[!UICONTROL Suppression category]**。

隱藏類別如下：

* **硬**:電子郵件地址會立即發送到禁止使用清單。

   >[!NOTE]
   >
   >當錯誤是垃圾郵件投訴的結果時，它也會 **硬** 的子菜單。 發出投訴的收件人的電子郵件地址立即發送到禁止清單。

* **軟**:一旦錯誤計數器達到限制閾值，軟錯誤就會向抑制清單發送地址。 [重試時瞭解更多資訊](retries.md)

* **手動**:您也可以手動將電子郵件地址或域添加到禁止顯示清單。 [了解更多](#add-addresses-and-domains)

>[!NOTE]
>
>瞭解有關中軟邊界和硬邊界的更多資訊 [傳遞失敗類型](../reports/suppression-list.md#delivery-failures) 的子菜單。

對於列出的每個電子郵件地址，您還可以檢查 **[!UICONTROL Type]** （電子郵件或域）, **[!UICONTROL Reason]** 用於排除它、添加者以及將其添加到禁止清單的日期/時間。

![](assets/suppression-list.png)

傳送失敗的可能原因有：

| 原因 | 說明 | 抑制類別 |
| --- | --- | --- |
| **[!UICONTROL Invalid Recipient]** | 收件人無效或不存在。 | 硬 |
| **[!UICONTROL Soft Bounce]** | 消息軟性反彈的原因不是此表中列出的軟錯誤，例如當發送超過ISP建議的允許速率時。 | 軟 |
| **[!UICONTROL DNS Failure]** | 消息因DNS故障而彈回。 | 軟 |
| **[!UICONTROL Mailbox Full]** | 由於收件人的郵箱已滿，無法接受更多郵件，郵件已彈回。 | 軟 |
| **[!UICONTROL Relaying Denied]** | 接收方阻止了該消息，因為不允許中繼。 | 軟 |
| **[!UICONTROL Challenge-Response]** | 消息是質詢 — 響應探測。 | 軟 |
| **[!UICONTROL Spam Complaint]** | 郵件被阻止，因為收件人將其標籤為垃圾郵件。 | 硬 |

>[!NOTE]
>
>未訂閱的用戶未接收來自 [!DNL Journey Optimizer]，因此無法將其電子郵件地址發送到禁止顯示清單。 他們的選擇在Experience Platform級別處理。 [瞭解有關退出選擇的更多資訊](../messages/consent.md)

## 手動添加地址和域 {#add-addresses-and-domains}

>[!CONTEXTUALHELP]
>id="ajo_admin_suppression_list"
>title="將電子郵件或域添加到禁止顯示清單"
>abstract="您可以手動填充Journey Optimizer禁止清單，以將特定電子郵件地址和/或域從您的發送中排除。"

當消息無法傳遞到電子郵件地址時，此地址將根據定義的抑制規則或彈出計數自動添加到抑制清單中。

但是，您也可以手動填充 [!DNL Journey Optimizer] 禁止顯示清單，以將特定電子郵件地址和/或域從您的發送中排除。

您可以添加電子郵件地址或域 [一次一個](#add-one-address-or-domain)或 [在批量模式下](#upload-csv-file) 通過CSV檔案上載。

要執行此操作，請選擇 **[!UICONTROL Add email or domain]** 按鈕，然後按照下面的方法之一操作。

![](assets/suppression-list-add-email.png)

### 添加一個地址或域 {#add-one-address-or-domain}

>[!CONTEXTUALHELP]
>id="ajo_admin_suppression_list_address"
>title="向取消清單添加一項"
>abstract="可以逐個添加電子郵件地址和/或域來填充隱藏清單。"

1. 選取 **[!UICONTROL One by one]** 選項。

   ![](assets/suppression-list-add-email-address.png)

1. 選擇地址類型： **[!UICONTROL Email address]** 或 **[!UICONTROL Domain address]**。

1. 輸入要從發送中排除的電子郵件地址或域。

   >[!NOTE]
   >
   >請確保輸入有效的電子郵件地址(如abc@company)或域（如abc.company.com）。

1. 根據需要指定原因。

   >[!NOTE]
   >
   >中允許包含32到126之間的所有ASCII字元 **[!UICONTROL Reason]** 的子菜單。 完整清單可在 [此頁](https://en.wikipedia.org/wiki/Wikipedia:ASCII#ASCII_printable_characters)例如{target=&quot;_blank&quot;}。

1. 按一下「**[!UICONTROL Submit]**」。

### 上載CSV檔案 {#upload-csv-file}

>[!CONTEXTUALHELP]
>id="ajo_admin_suppression_list_csv"
>title="上載CSV以將項添加到禁止顯示清單"
>abstract="可以通過上載一個填入了要排除的電子郵件地址/域的CSV檔案來填充隱藏清單。"

1. 選取 **[!UICONTROL Upload CSV]** 選項。

   ![](assets/suppression-list-upload-csv.png)

1. 下載要使用的CSV模板，其中包括以下列和格式：

   ```
   TYPE,VALUE,COMMENT
   EMAIL,abc@somedomain.com,Comment
   DOMAIN,somedomain.com,Comment
   ```
   >[!NOTE]
   >
   >中允許包含32到126之間的所有ASCII字元 **注釋** 的雙曲餘切值。 完整清單可在 [此頁](https://en.wikipedia.org/wiki/Wikipedia:ASCII#ASCII_printable_characters)例如{target=&quot;_blank&quot;}。

   您也可以從 **[!UICONTROL Suppression list]** 的子菜單。

   >[!CAUTION]
   >
   >不要更改CSV模板中列的名稱。
   >
   >檔案大小不應超過1 MB。

1. 使用要添加到禁止顯示清單的電子郵件地址和/或域填充CSV模板。

1. 完成後，拖放CSV檔案，然後按一下 **[!UICONTROL Upload file]**。

   ![](assets/suppression-list-upload-file-button.png)

1. 按一下「**[!UICONTROL Submit]**」。

>[!NOTE]
>
>上載完成後，請通過從介面檢查其狀態來確保上載成功。 [瞭解如何](#recent-uploads)

### 檢查最近上載狀態 {#recent-uploads}

您可以檢查您上載的最新CSV檔案清單。

要執行此操作，請 **[!UICONTROL Suppression list]** 的 **[!UICONTROL Recent uploads]** 按鈕

![](assets/suppression-list-recent-uploads-button.png)

將顯示您提交的最新上載及其相應狀態。

如果錯誤報告與檔案關聯，則可以下載它以檢查遇到的錯誤。

![](assets/suppression-list-recent-uploads-error.png)

下面是您可以在錯誤報告中找到的條目類型示例：

```
type,value,comments,failureReason
Email,examplemail.com,MANUAL,Invalid format for value: examplemail.com
Email,examplemail,MANUAL,Invalid format for value: examplemail
Email,example@mail,MANUAL,Invalid format for value: example@mail
Domain,example,MANUAL,Invalid format for value: example
Domain,example.!com,MANUAL,Invalid format for value: example.!com
Domain,!examplecom,MANUAL,Invalid format for value: !examplecom
```
