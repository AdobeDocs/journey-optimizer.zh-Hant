---
solution: Journey Optimizer
product: journey optimizer
title: 熟客資料與資料集
description: 瞭解忠誠度挑戰需要哪些Adobe Experience Platform設定檔資料和資料集，以及資料集存留時間(TTL)如何影響保留。
feature: Journeys
topic: Content Management
role: Admin, Developer
level: Intermediate
hide: true
badge: label="私人測試版" type="Informative"
mini-toc-levels: 1
exl-id: a7c4e1b2-8f3d-4a6c-9e0b-1d2e3f4a5b6c
feature_v2: []
subfeature_v2: []
source-git-commit: 2e01cd1880b8527911376d94188d0204f7649541
workflow-type: tm+mt
source-wordcount: 538
ht-degree: 5%

---

# 熟客資料與資料集 {#loyalty-data-and-datasets}

>[!BEGINSHADEBOX]

**目錄**

[開始應對忠誠度挑戰](get-started.md)

<table style="table-layout:fixed">
<tr style="border: 0;">
<td style="vertical-align:top;">

**建立和管理挑戰**

* [存取及管理挑戰與工作](access-loyalty-challenges.md)
* [創造挑戰](create-challenges.md)
* [建立任務](create-tasks.md)
* [監視忠誠度挑戰績效](loyalty-reporting.md)

</td>
<td style="vertical-align:top;">

**設定並整合**

* [設定忠誠度挑戰](loyalty-admin.md)
* **忠誠度資料和資料集** ◀︎ **您在這裡**
* [忠誠度挑戰API參考](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges){target="_blank"}

</td>
</tr>
</table>

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>此功能目前在&#x200B;**私人測試版**&#x200B;中。 如需發行週期與可用性階段的完整詳細資訊，請參閱 [Journey Optimizer 發行週期](../rn/releases.md)。

## 概觀 {#overview}

忠誠度挑戰仰賴Adobe Experience Platform的身分、設定檔屬性、體驗事件和受眾。 使用此頁面瞭解要準備哪些資料、涉及哪些資料集，以及&#x200B;**存留時間(TTL)**&#x200B;在您編寫挑戰或使用忠誠度挑戰API之前如何影響保留率。

請連絡您的Adobe管理員，以設定Journey Optimizer方案，或在&#x200B;**[!UICONTROL 忠誠度管理員]**&#x200B;功能表中設定獎勵履行和事件對應。 [瞭解如何設定忠誠度挑戰](loyalty-admin.md)。 如需REST端點與驗證的相關資訊，請參閱[忠誠度挑戰API參考](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges){target="_blank"}。

## Adobe Experience Platform資料 {#aep-data}

### 輪廓屬性 {#profile-attributes}

在&#x200B;**[!DNL XDM Individual Profile]**&#x200B;類別中挑戰對象、個人化和報告使用設定檔。 將您用於忠誠度挑戰的身分識別[名稱空間](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/identity/features/namespaces){target="_blank"}與設定檔資料中的成員識別方式以及在&#x200B;**[!UICONTROL 忠誠度管理員]**&#x200B;功能表的&#x200B;**[!UICONTROL 全域設定]**&#x200B;中選取的名稱空間對齊。

對於設定檔上的標準熟客屬性（點、層級、方案、狀態和相關欄位），請使用Experience Platform **[熟客詳細資料](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/xdm/field-groups/profile/loyalty-details){target="_blank"}**&#x200B;結構描述欄位群組。 該欄位群組定義`loyalty`物件及其屬性（例如`points`、`tier`、`program`和`status`）。

➡️ [熟客方案詳細資料結構描述欄位群組](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/xdm/field-groups/profile/loyalty-details){target="_blank"}

### 體驗事件 {#experience-events}

**[!UICONTROL 購買]**、**[!UICONTROL 支出]**&#x200B;和&#x200B;**[!UICONTROL 自訂事件]**&#x200B;任務取決於內嵌到Adobe Experience Platform中的體驗事件。 針對&#x200B;**[!UICONTROL 自訂事件]**&#x200B;任務，必須在&#x200B;**[!UICONTROL 忠誠度管理員]**&#x200B;功能表中設定相符的事件定義（識別碼路徑、選用的XDM結構描述ID、結構描述及轉換器），行銷人員才能在任務產生器中輸入自訂事件值。 [瞭解如何設定事件定義](loyalty-admin.md#event-definitions)

確保事件裝載使用與您的忠誠度挑戰設定相同的身分名稱空間，好讓進度可歸因於正確的設定檔。

### 受眾與報表 {#audiences-reporting}

行銷人員在設定挑戰資格時選取平台[對象](../audience/about-audiences.md)。 熟客報告儀表板使用Adobe Customer Journey Analytics。 [瞭解如何監視忠誠度挑戰績效](loyalty-reporting.md)

## 資料集存留時間(TTL) {#dataset-ttl}

忠誠度挑戰會將操作和報表資料儲存在Adobe Experience Platform資料集中（包括為您的方案建立的事件和個人化相關資料集）。 資料集&#x200B;**存留時間(TTL)**&#x200B;會控制資料在資料湖中保留的時間長度，以及在適用時，在設定檔存放區中保留的時間長度。

Journey Optimizer將TTL護欄套用至許多系統產生的資料集。 忠誠度相關資料集會遵循與沙箱相同的平台保留模式。

在Journey Optimizer中➡️ [資料集存留時間(TTL)護欄](../data/datasets-ttl.md)

>[!NOTE]
>
>組織層級的熟客方案設定可包含透過熟客方案中繼資料服務管理的封存和保留設定（例如封存期間）。 如果您需要調整私人測試環境的保留率，請洽詢Adobe管理員。
