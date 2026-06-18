---
solution: Journey Optimizer
product: journey optimizer
title: 檢視SMS使用量度
description: 瞭解如何在Journey Optimizer中產生SMS使用報告，以便協調訊息數量與供應商帳單。
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
source-git-commit: b519bcd5489c441e7f22cb47783d8b99a58c2442
workflow-type: tm+mt
source-wordcount: '500'
ht-degree: 1%

---

# 產生SMS使用報告 {#sms-usage-report}

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_usage_metrics"
>title="簡訊使用量度"
>abstract="產生SMS使用報告，以協調傳訊量與供應商帳單。 報表會按天彙總每個簡短代碼或電話號碼的行動終止(MT)和行動產生(MO)計數。"

>[!BEGINSHADEBOX]

**在此頁面上：**&#x200B;在Adobe Journey Optimizer中產生SMS使用報告，以使用Sinch MMS API認證和可下載的CSV輸出，調解行動終止(MT)和行動來源(MO)的磁碟區，以及廠商帳單。

>[!ENDSHADEBOX]

透過Adobe Journey Optimizer購買簡訊時，可以使用簡訊使用量度。 報表摘要過去&#x200B;**90天**&#x200B;以短代碼或電話號碼傳送及接收流量（依日累計）。

若要檢視使用狀況測量結果，管理員必須：

1. [建立Sinch MMS API認證](mobile-configuration-sinch.md#sinch-mms)，此認證僅用於擷取Sinch的使用量資料。

   使用報告需要將&#x200B;**[!UICONTROL SMS廠商]**&#x200B;設定為&#x200B;**Sinch MMS**&#x200B;的API認證。 此認證會將Journey Optimizer連線至Sinch，以便擷取使用資料。 它不同於用來傳送SMS或MMS訊息的Sinch認證，不過欄位值來自相同的Sinch專案。

1. [設定並擷取SMS使用報告](#configure-sms-usage-report)。

這些步驟需要&#x200B;**[!UICONTROL 管理簡訊設定]**&#x200B;許可權。 [深入了解權限](../administration/high-low-permissions.md#administration-permissions)。

## 設定和檢視SMS使用報告 {#configure-sms-usage-report}

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_usage_report_name"
>title="報告名稱"
>abstract="輸入有助於您稍後在清單中識別此報告的標籤，例如2026年5月的計費檢閱。"

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_usage_credential"
>title="簡訊認證"
>abstract="選取Sinch API認證，其傳送與接收流量應會顯示在此報表中。 若要新增或更新認證，請移至&#x200B;**管理** > **管道** > **API認證**，然後選擇&#x200B;**SMS供應商** > **Sinch MMS**。"

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_usage_start_date"
>title="開始日期"
>abstract="要納入報表之日期範圍的第一天。 使用情況資料僅供過去90天使用。"

SMS使用報告透過短程式碼呈現行動來源(MO)和行動終止(MT)的磁碟區，以支援Journey Optimizer中供應商帳單和訊息活動之間的調解。

1. 在左側邊欄中，瀏覽至&#x200B;**[!UICONTROL 管理]** > **[!UICONTROL 管道]** > **[!UICONTROL 簡訊設定]**。

1. 存取&#x200B;**[!UICONTROL 檢視簡訊使用量度]**&#x200B;功能表，然後按一下&#x200B;**[!UICONTROL 設定新報表]**。

   ![](assets/usage_report_1.png)

1. 設定報表：

   * **[!UICONTROL 報表名稱]**：輸入有助於您辨識報表的標籤。
   * **[!UICONTROL SMS認證]**：選取您先前為您的SMS使用報告建立的&#x200B;**Sinch MMS** API認證。
   * **[!UICONTROL 開始日期]**&#x200B;和&#x200B;**[!UICONTROL 結束日期]**：設定報表的日期範圍。 使用情況資料僅供過去90天使用。

     ![](assets/usage_report_2.png)

1. 按一下&#x200B;**[!UICONTROL 設定報表]**&#x200B;以提交請求。

1. 在&#x200B;**[!UICONTROL 已提交的報告]**&#x200B;清單中，找到您設定的報告，然後按一下&#x200B;**[!UICONTROL 擷取報告]**。

   報告產生時，狀態變更為&#x200B;**擱置中**。

1. 一旦您的報告狀態更新為&#x200B;**[!UICONTROL 就緒]**，請按一下&#x200B;**[!UICONTROL 檢視]**&#x200B;以開啟報告。 報表包含：

   * **使用摘要**：所選日期的行動來源(MO)與行動終止(MT)訊息總數，以簡短代碼劃分。

   * **每日SMS音量**：依每日的SMS音量，依短程式碼劃分。

     ![](assets/usage_report_3.png)

1. 若要匯出報表，請按一下&#x200B;**[!UICONTROL 下載CSV]**。 Journey Optimizer會下載您檢視之報表的CSV檔案。
