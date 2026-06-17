---
solution: Journey Optimizer
product: journey optimizer
title: 在協調的行銷活動中新增個人化
description: 瞭解如何使用設定檔屬性、工作表中的目標屬性及擴充收集陣列，個人化協調的行銷活動訊息。
exl-id: c4a91e2b-6f08-4d1a-9e3b-2f8f5a0d1c62
version: Campaign Orchestration
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d556b755-390a-43f0-be32-a08cf6236126id: fe338112-e2ce-4876-8989-fc4d497613f1
topic_v2: id: e0eb8757-182f-49f3-94a4-1587d16f5094id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: e0a12bd7971c778378f9905cf93653792f38509d
workflow-type: tm+mt
source-wordcount: 477
ht-degree: 0%

---

# 在協調的行銷活動中新增個人化 {#add-personalization}

在您[在畫布上協調活動](orchestrate-activities.md)並新增頻道活動後，您即可在電子郵件、簡訊或其他頻道編輯器中個人化訊息內容。

「已協調」行銷活動中的Personalization與其他[!DNL Journey Optimizer]行銷活動或歷程的運作方式類似，差異與&#x200B;**工作表**&#x200B;相關：透過在畫布上定位和擴充活動所計算的屬性，而不僅僅是來自設定檔存放區的資料。

## 存取個人化編輯器 {#access}

1. 開啟您的「已協調的行銷活動」並新增管道活動。 [瞭解如何新增管道活動](activities/channels.md#add)

1. 設定頻道活動，然後開啟&#x200B;**[!UICONTROL 內容]**&#x200B;索引標籤並編輯訊息。

1. 在訊息編輯器中，使用個人化編輯器將屬性插入內容中。

若要預覽和測試頻道活動的個人化內容，請參閱[檢查並測試您的內容](activities/channels.md#simulate-content-test-profiles)。

## 設定檔和目標屬性 {#attributes}

開啟個人化編輯器時，有兩個主要資料夾包含可用於個人化的屬性：

* **[!UICONTROL 輪廓屬性]**

  來自[!DNL Adobe Experience Platform]的設定檔相關資料：名稱、電子郵件地址、位置以及使用者設定檔中擷取的其他特徵。

* **[!UICONTROL Target屬性]** （僅限協調的行銷活動）

  在促銷活動畫布上從工作表中計算的屬性。 此資料夾有兩個子資料夾：

   * **`<Targeting dimension>`** （例如，收件者或購買） — 與您在行銷活動中定位的維度相關的屬性。

   * **`Enrichment`** — 透過&#x200B;**[!UICONTROL 擴充]**&#x200B;活動新增的資料（關聯式連結、收集的行、彙總）。 在1:N **[!UICONTROL 收集資料]**&#x200B;擴充後，您會同時取得編號行和集合陣列。 [瞭解如何使用擴充集合資料](#enrichment-collections)

如需[!DNL Journey Optimizer]的個人化編輯器的詳細總覽，請參閱[開始使用個人化](../personalization/personalize.md)。

## 使用擴充集合資料 {#enrichment-collections}

當您設定具有1:N連結和&#x200B;**[!UICONTROL 收集資料]**&#x200B;的&#x200B;**[!UICONTROL 擴充]**&#x200B;活動時，擴充屬性可在&#x200B;**[!UICONTROL 目標屬性] > [!UICONTROL 擴充]**&#x200B;下使用兩種形式：

* **平面化行** — 每個擷取的行有一個欄位（例如，**Purchase 1**、**Purchase 2**、**Purchase 3**），每個欄位都有您在連結上選取的屬性（例如價格或產品）。 當您需要個別的固定位置（例如`target.enrichment.purchase1.price`）時，請使用這些選項。

* **集合陣列** — 所有已收集行的一個陣列，從連結標籤命名（例如，**購買**）。 當您需要處理完整的記錄集時，請使用此選項 — 使用[陣列函式](#array-functions)。

![](assets/enrichment-target-attributes-picker.png)

若要識別集合陣列中的旗標線，請在運算式編輯器中插入屬性，並讀取產生的路徑。 集合陣列是路徑為&#x200B;**plural** （例如`purchases`）且有&#x200B;**無行號** （`purchase1`、`purchase2`等）的專案。

| 您需要的專案 | 運算式編輯器中的路徑 |
| --- | --- |
| **已收集一行** | **已編號** — 例如`target.enrichment.purchase1.price` |
| **完整集合** | **Plural與未編號** — 例如`target.enrichment.purchases.price` |

您可以將[!DNL Journey Optimizer]中其他位置使用的相同[陣列和清單函式](../personalization/functions/arrays-list.md)套用至擴充集合，參考`target.enrichment.<label>`。

例如，在主旨列中，您可能會顯示有多少已收集的購買存在，以及第一個專案的價格：

```sql
Hello number of Items: {%= count(target.enrichment.purchases.price) %} , Name of first item: {%= head(target.enrichment.purchases.product) %}
```

➡️ [瞭解如何在畫布上設定集合擴充](activities/enrichment.md#collection-personalization)
