---
title: PTR記錄
description: 了解如何管理PTR記錄
audience: administrators
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 4c930792-0677-4ad5-a46c-8d40fc3c4d3a
source-git-commit: 1e62715f35b50bba639657a1bef37aa61922c715
workflow-type: tm+mt
source-wordcount: '443'
ht-degree: 0%

---

# PTR記錄

## 關於PTR記錄

指針記錄(PTR)是一種域名系統(DNS)記錄，它提供連結到IP地址的域名。

使用PTR記錄，接收郵件伺服器可以通過識別其IP地址是否與伺服器所連接的名稱相對應來檢查發送郵件伺服器的真實性。

## 訪問子網域的PTR記錄

在Adobe Journey Optimizer中委派子網域後，就會自動建立PTR記錄並與此子網域建立關聯。 您可以從 **[!UICONTROL Channels]** > **[!UICONTROL Email configuration]** > **[!UICONTROL PTR records]** 功能表。

![](../assets/ptr-records.png)

該清單使用以下語法顯示為每個委派子域生成的PTR記錄：

* 「r」表示記錄，
* 「xx」表示IP地址的最後兩個數字，
* 子網域名稱。

您可以從清單中開啟PTR記錄，以顯示關聯的子域名和IP地址。

## 編輯PTR記錄 {#edit-ptr-record}

您可以修改PTR記錄以編輯與IP地址關聯的子域。

1. 從清單中，按一下PTR記錄名以開啟它。

   ![](../assets/ptr-record-select.png)

1. 視需要編輯子網域。

   ![](../assets/ptr-record-subdomain.png)

   >[!NOTE]
   >
   >您無法修改 **[!UICONTROL IP]** 和 **[!UICONTROL PTR record]** 欄位。

1. 按一下 **[!UICONTROL SAve]** 確認變更。

安 **[!UICONTROL Updating]** 表徵圖顯示在清單中PTR記錄的名稱旁。

![](../assets/ptr-record-updating.png)

要檢查PTR記錄更新詳細資訊，請按一下 **[!UICONTROL Updating]** 或 **[!UICONTROL Recent updates]** 表徵圖。

![](../assets/ptr-record-recent-update.png)

您可以查看更新狀態和請求的更改等資訊。

![](../assets/ptr-record-updates.png)

## 更新狀態

PTR記錄更新可以具有以下狀態：

* **[!UICONTROL Processing]**:PTR記錄更新已提交，正在進行驗證過程。
* **[!UICONTROL Success]**:已驗證更新的PTR記錄，並且新子域現在與IP地址關聯。
* **[!UICONTROL Failed]**:在PTR記錄更新驗證期間，一個或多個檢查失敗。

### 正在處理

將執行數項傳遞能力檢查，以確認要與IP位址關聯的新子網域是否有效。 <!--The processing time is around **48h-72h**, and can take up to **7-10 days**. Learn more on the checks performed during the validation cycle in [this section](#create-message-preset).-->

>[!NOTE]
>
>在進行更新時無法修改PTR記錄。 您仍可按一下其名稱，但 **[!UICONTROL Subdomain]** 欄位會呈現灰色。 更新成功前，不會反映變更。

在驗證程式期間，舊的子網域仍與IP位址相關聯。

### 成功

驗證程式一旦成功，新子網域就會自動與IP位址相關聯。

### 已失敗

如果驗證過程失敗，則顯示較舊的PTR記錄。 先前與IP位址相關聯的有效子網域維持不變。

可能的更新錯誤類型如下：
* 無法為PTR記錄建立新的轉發DNS
* 無法更新記錄
* 無法重新將相關性上線

更新失敗時，PTR記錄將重新變為可編輯。 您可以按一下其名稱，然後再次更新子網域。
