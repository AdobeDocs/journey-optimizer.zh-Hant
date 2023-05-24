---
solution: Journey Optimizer
product: journey optimizer
title: PTR記錄
description: 瞭解如何管理PTR記錄
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
keywords: 子域， PTR，記錄， DNS，域，郵件
exl-id: 4c930792-0677-4ad5-a46c-8d40fc3c4d3a
source-git-commit: b8065a68ed73102cb2c9da2c2d2675ce8e5fbaad
workflow-type: tm+mt
source-wordcount: '785'
ht-degree: 9%

---

# PTR記錄 {#ptr-records}

>[!CONTEXTUALHELP]
>id="ajo_admin_ptr_record"
>title="子網域的 PTR 記錄"
>abstract="指標記錄 (PTR) 是一種 DNS 記錄，會提供連結至 IP 位址的域名，可協助接收郵件伺服器驗證寄件者的 IP 位址。只有在和您的傳遞能力專家完成適當考量和討論後，才能編輯 PTR 記錄。"

>[!CONTEXTUALHELP]
>id="ajo_admin_ptr_record_header"
>title="子網域的 PTR 記錄"
>abstract="在 Journey Optimizer 中將子網域委派給 Adobe 後，會自動建立 PTR 記錄並將其和此子網域建立關聯。"

## 關於PTR記錄 {#about-ptr-records}

指針記錄(PTR)是域名系統(DNS)記錄的類型，它提供連結到IP地址的域名。

使用PTR記錄，接收郵件伺服器可以通過確定其IP地址是否與伺服器所連接的名稱相對應來檢查發送郵件伺服器的真實性。

## 訪問子域的PTR記錄 {#access-ptr-records}

一次 [子域被委派](delegate-subdomain.md) 在Adobe Journey Optimizer，自動建立PTR記錄並與此子域關聯。 您可以從 **[!UICONTROL 管理]** > **[!UICONTROL 頻道]** > **[!UICONTROL 電子郵件配置]** > **[!UICONTROL PTR記錄]** 的子菜單。

![](assets/ptr-records.png)

該清單顯示為每個委派子域生成的PTR記錄，使用以下語法：

* 記錄&quot;r&quot;
* IP地址的最後兩個數字是&quot;xx&quot;
* 子域名。

可以從清單中開啟PTR記錄以顯示關聯的子域名和IP地址。

## 編輯PTR記錄 {#edit-ptr-record}

您可以修改PTR記錄以編輯與IP地址關聯的子域。

>[!CAUTION]
>
>PTR記錄對所有環境都是通用的。 因此，對PTR記錄的任何修改也會影響生產沙盒。
>
>編輯PTR記錄時請格外小心。 如有任何疑問，請與交付能力專家聯繫。

### 完全委託的子域 {#fully-delegated-subdomains}

編輯具有子域的PTR記錄 [全權](delegate-subdomain.md#full-subdomain-delegation) 要Adobe，請執行以下步驟。

1. 在清單中，按一下PTR記錄名以將其開啟。

   ![](assets/ptr-record-select.png)

1. 選擇子域 [全權](delegate-subdomain.md#full-subdomain-delegation) 到Adobe。

   ![](assets/ptr-record-subdomain.png)

1. 按一下 **[!UICONTROL 保存]** 確認更改。

>[!NOTE]
>
>無法修改 **[!UICONTROL IP]** 和 **[!UICONTROL PTR記錄]** 的子菜單。

### 使用CNAME方法的委派子域 {#edit-ptr-subdomains-cname}

使用委託給Adobe的子域編輯PTR記錄 [CNAME方法](delegate-subdomain.md#cname-subdomain-delegation)，請執行以下步驟。

1. 在清單中，按一下PTR記錄名以將其開啟。

   ![](assets/ptr-record-select-cname.png)

1. 使用 [CNAME方法](delegate-subdomain.md#cname-subdomain-delegation) 清單中。

   ![](assets/ptr-record-subdomain-cname.png)

1. 您需要在托管平台上建立新的轉發DNS記錄。 為此，請複製由Adobe生成的記錄。 完成後，選中「I confirm...」（我確認……）框。

   ![](assets/ptr-record-subdomain-confirm.png)

   >[!NOTE]
   >
   >如果您收到以下消息：「請先建立轉發DNS，然後重試」，請執行以下步驟：
   >   * 如果已成功建立轉發DNS記錄，請檢查DNS提供程式。
   >   * 跨DNS的記錄可能無法立即同步。 請等待幾分鐘，然後重試。


1. 按一下 **[!UICONTROL 保存]** 確認更改。

>[!NOTE]
>
>無法修改 **[!UICONTROL IP]** 和 **[!UICONTROL PTR記錄]** 的子菜單。

## 檢查PTR記錄更新詳細資訊 {#check-ptr-record-update}

確認PTR記錄編輯後， **[!UICONTROL 處理]** 表徵圖顯示在清單中PTR記錄的名稱旁邊。

![](assets/ptr-record-updating.png)

>[!NOTE]
>
>的 [更新處理](#processing) 最多需要3小時。

要檢查PTR記錄更新詳細資訊，請按一下其旁邊的表徵圖。 瞭解有關與中的不同表徵圖關聯的狀態的詳細資訊 [此部分](#ptr-record-update-statuses)。

![](assets/ptr-record-recent-update.png)

您可以查看更新狀態和請求的更改等資訊。

![](assets/ptr-record-updates.png)

## PTR記錄更新狀態 {#ptr-record-update-statuses}

PTR記錄更新可以具有以下狀態：

* ![](assets/do-not-localize/ptr-record-processing.png) **[!UICONTROL 處理]**:已提交PTR記錄更新，並正在進行驗證過程。
* ![](assets/do-not-localize/ptr-record-success.png) **[!UICONTROL 成功]**:已驗證更新的PTR記錄，新子域現在與IP地址關聯。
* ![](assets/do-not-localize/ptr-record-failed.png) **[!UICONTROL 失敗]**:在PTR記錄更新驗證期間，一個或多個檢查失敗。

### 正在處理 {#processing}

將執行若干可傳送性檢查，以驗證要與IP地址關聯的新子域是否有效。 這最多需要3小時。

>[!NOTE]
>
>更新正在進行時，無法修改PTR記錄。 您仍然可以按一下其名稱，但 **[!UICONTROL 子域]** 欄位呈灰色。 在更新成功之前，不會反映更改。

在驗證過程中，舊子域仍與IP地址關聯。

### 成功 {#success}

驗證過程成功後，新子域將自動與IP地址關聯。

### 已失敗 {#failes}

如果驗證過程失敗，則顯示較舊的PTR記錄。 以前與IP地址關聯的有效子域保持不變。

可能的更新錯誤類型如下：
* 無法為PTR記錄建立新的轉發DNS
* 無法更新記錄
* 無法重新裝載連接

更新失敗時，PTR記錄將再次變為可編輯。 您可以按一下其名稱並再次更新子域。
