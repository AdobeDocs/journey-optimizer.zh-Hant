---
title: 移轉至歷程內嵌撰寫的步驟
description: 移轉至歷程內嵌撰寫的步驟
exl-id: 8412a0bd-674c-4d6a-aa5b-443655d2943a
source-git-commit: 1ab038e8b2f0582ad947400c7d070a70e1a84b9b
workflow-type: tm+mt
source-wordcount: '1048'
ht-degree: 3%

---

# 內嵌編寫移轉步驟{#migration-steps}

以下說明在Adobe Journey Optimizer中製作內容的新程式： [頁面](../rn/inline-messages.md). 將為您執行自動轉換歷程。 話雖如此，我們需要你協助幾個步驟。 

>[!VIDEO](https://video.tv.adobe.com/v/344699)

以下是主要階段和步驟：

**[移轉前](../rn/inline-messages-steps.md#migration-step-1)**

1. 在非生產沙箱上，停止所有即時和關閉的歷程。 [閱讀全文](../rn/inline-messages-steps.md#migration-step-1-1)
1. 在生產沙箱中，停止所有尚未保留設定檔的即時臨機歷程。 [閱讀全文](../rn/inline-messages-steps.md#migration-step-1-2)

**[在第一次迭代後](../rn/inline-messages-steps.md#migration-step-2)**

1. 檢查您移轉的即時歷程上是否有任何錯誤。 [閱讀全文](../rn/inline-messages-steps.md#migration-step-2-1)
1. 列出由移轉建立的所有新版本。 [閱讀全文](../rn/inline-messages-steps.md#migration-step-2-2)
1. 逐一測試並發佈。 [閱讀全文](../rn/inline-messages-steps.md#migration-step-2-3)
1. 列出所有即時版本。 [閱讀全文](../rn/inline-messages-steps.md#migration-step-2-4)
1. 檢查移轉的草稿版本是否有錯誤。 [閱讀全文](../rn/inline-messages-steps.md#migration-step-2-5)

**[第二次迭代後](../rn/inline-messages-steps.md#migration-step-3)**

1. 檢查兩個移轉階段。 [閱讀全文](../rn/inline-messages-steps.md#migration-step-3-1)
1. 停止舊版。 [閱讀全文](../rn/inline-messages-steps.md#migration-step-3-2)

**[在第三次和上次迭代之前](../rn/inline-messages-steps.md#migration-step-4)**

在淘汰前驗證所有項目皆已移轉。

<br>

## 移轉前（7月25日）{#migration-step-1}

### 1.停止所有即時和已關閉的歷程{#migration-step-1-1}

開啟 **非生產沙箱**，停止所有即時和已關閉的歷程。 這可讓自動移轉程式從這些沙箱移轉所有歷程，而您無需採取任何動作。 移轉後，您將能複製停止的歷程版本並加以使用。

### 2.停止所有尚未設定檔仍處於中的即時臨機歷程{#migration-step-1-2}

在 **生產沙箱**，停止所有不再包含設定檔的即時臨機歷程。

+++如何尋找這些歷程？

若要尋找這些歷程，請導覽至 **歷程** ，並篩選「狀態=即時」和「類型=讀取區段」的清單。 您也可以從最早到最新「已發佈」日期按時間順序排序歷程。

![](assets/inline-migration-steps1.png)

從上到下開啟。

* 檢查歷程是否有訊息。
* 檢查它們是否不是重複的歷程。 這些不是隨選的。 你最想讓他們活下來。 例如，這是一個經常性的歷程（非隨選）:

   ![](assets/inline-migration-steps2.png)

* 如果您在這些歷程中使用了等待或事件接聽程式，設定檔可能仍會在內。 查看歷程執行日期，並新增您在等待或事件接聽程式中定義的任何小時/天，以推斷當中沒有任何設定檔時的實際日期。 如果日期已過去，您可以停止歷程。 否則，此歷程會在歷程執行日期後30天自動移至「已完成」狀態。

+++

**重要備註**

* 請避免在移轉日期（7月25日）前關閉歷程。 知道移轉指令碼不會移轉即時或已關閉的歷程，限制生產沙箱中已關閉的歷程數量，將限制移轉後所需的手動動作數量。

* 如果您的即時歷程不是最新版本，表示您在草稿中建立了另一個歷程版本、發佈或刪除它。

* 如果您有未用於歷程且想保留的訊息，請將其儲存為範本。 請參閱 [頁面](../design/email-templates.md#save-as-template). 請注意，在淘汰之前，您仍可以存取這些參數。

## 移轉第一次迭代後（7月25日）{#migration-step-2}

移轉程式會分兩個階段排序：自動化階段（7月25日至7月26日）和手動階段（7月26日起），需要採取行動。

有關自動化階段，請參閱 [頁面](../rn/inline-messages.md#process). 在手動階段中，以下是要在 **生產沙箱**:

<!--
_On non-production sandboxes:_

**1. Check the migration status report for any error**

Click the **Check status** button in the top banner and check that there has been no error during the automatic migration and that there is nothing left to migrate. 

![](assets/inline-migration-steps3.png)

Look for the "ERROR" status. 

![](assets/inline-migration-steps4.png)

* If there is no error, you are good to go.
* If there are errors, look for the error by searching "errorMessage". The following error is expected as migration of multi-channel messages is not supported: "Migration of multi-channel messages is not supported". You will have to rebuild this journey.

    ![](assets/inline-migration-steps5.png)

_On the production sandbox:_

-->

### 1.檢查您移轉的即時歷程上是否有任何錯誤{#migration-step-2-1}

在狀態報表中，檢查自動移轉的即時歷程上是否有任何錯誤([了解更多](../rn/inline-messages.md#status). 按一下 **檢查狀態** 按鈕。

![](assets/inline-migration-steps3.png)

查找「ERROR_NEW_VERSION_CREATION」：

![](assets/inline-migration-steps6.png)

* 如果沒有錯誤，表示已處理所有需要移轉的即時歷程版本，且已自動建立新的移轉草稿版本。

* 如果您看到錯誤，可以搜尋「errorMessage」並檢查記錄檔中的錯誤訊息。 不會移轉多通道訊息。 您必須建立另一個歷程。

   ![](assets/inline-migration-steps5.png)

* 如有其他錯誤，請連絡您的CSM或任何Adobe代表以取得指引。

### 2.列出由移轉建立的所有新版本{#migration-step-2-2}

它們會標示為 [已移轉] 在歷程標籤中會更新建立日期。

![](assets/inline-migration-steps7.png)

### 3.逐一測試並發佈{#migration-step-2-3}

請確定歷程仍需在生產環境中執行。 若 [移轉前準備](../rn/inline-messages-steps.md#migration-step-1) 無法正確執行，您可能會針對不再需要的單次觀看歷程建立新版本。

測試您的歷程草稿版本，現在包含內嵌管道動作。

發佈您的新歷程版本。 之前的即時版本接著會移至「已關閉」狀態。

### 4.列出所有即時版本{#migration-step-2-4}

應將所有項目標示為最新。 如果沒有，請尋找較新版本，測試並發佈。

![](assets/inline-migration-steps8.png)

### 5.檢查移轉的草稿版本是否有錯誤 {#migration-step-2-5}

按一下 **檢查狀態** 按鈕([了解更多](../rn/inline-messages.md#status) 並檢查自動移轉期間是否沒有錯誤，以及沒有任何可移轉的項目。 請注意，任何有錯誤的歷程（含訊息）將在9月5日後淘汰（所有沙箱上）。

![](assets/inline-migration-steps11.png)

查找「ERROR」狀態。

![](assets/inline-migration-steps9.png)

* 如果沒有錯誤，你就可以走了。

* 如果有錯誤，請搜索&quot;errorMessage&quot;以查找錯誤。 由於不支援多通道訊息的移轉，預期會出現下列錯誤：「不支援多通道訊息的移轉」。 你必須重建這個歷程。

![](assets/inline-migration-steps5.png)

## 第二次迭代後（8月1日）{#migration-step-3}

第二次迭代發生在8月1日到8月2日的夜間。

<!--
_On non-production sandboxes:_

**1. Check at the status report**

Click the **Check status** button in the top banner and check that all journeys have been migrated and there's nothing left to migrate. If there is an error or something left to migrate, please reach out to your CSM or Adobe representative for guidance.

-->

如果已及時執行所有先前步驟，則除了已關閉步驟和有錯誤的步驟外，所有歷程都已移轉。 以下是後續步驟 **生產沙箱**:

### 1.檢查兩個遷移階段{#migration-step-3-1}

如果沒有錯誤，您應該沒有「toMigrate」和「createNewVersion」下的「apilityStatus」歷程。 在以下示例中，有一個「ERROR」和一個「ERROR_NEW_VERSION_CREATION」。

![](assets/inline-migration-steps10.png)

### 2.停止舊版{#migration-step-3-2}

如果您尚未發佈較新的歷程版本(請參閱 [節](../rn/inline-messages-steps.md#migration-step-2-3))（在時間上）(在第2版（8月1日）之前)，然後發佈較新版本。

>[!NOTE]
>
>停止舊版，否則您會失去舊版及其相關報表。

## 第三次迭代和上次迭代之前（9月5日）{#migration-step-4}

8月1日到9月5日之間，您需要驗證所有項目皆已移轉，且沒有任何歷程剩餘仍在使用訊息，否則將於9月5日淘汰。
