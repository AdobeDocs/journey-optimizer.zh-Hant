---
title: 開始使用行銷活動
description: 瞭解有關中的市場活動的更多資訊 [!DNL Journey Optimizer]
feature: Overview
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
source-git-commit: 6177a33edeb3b8381c3eb5609762b4d974dc93e3
workflow-type: tm+mt
source-wordcount: '300'
ht-degree: 8%

---


# 開始使用行銷活動 {#get-started-campaigns}

>[!CONTEXTUALHELP]
>id="campaigns_list"
>title="Campaigns"
>abstract="使用「市場活動」，您可以跨多個渠道將一次性內容交付到特定市場。 在建立新市場活動之前，請確保您已預置了消息，並且已準備好使用Adobe Experience Platform段。"

## 關於市場活動 {#about}

市場活動允許您使用多個渠道將一次性內容交付到特定市場。 與按順序執行活動的行程不同，市場活動可以同時執行活動，或者立即執行，或者按指定的時間表執行。

您可以建立兩種類型的市場活動：

* **計畫的市場活動** 允許針對促銷優惠、接洽活動、公告、法律通知或策略更新等市場營銷用例進行簡單的臨時批通信。
* **API觸發的市場活動** 允許使用REST API（密碼重置、卡放棄等）執行簡單的事務/操作消息，其中需要可能涉及使用配置檔案屬性和負載的上下文資料進行個性化。

瞭解如何處理市場活動：
* [建立行銷活動](create-campaign.md)
* [建立API觸發的市場活動](api-triggered-campaigns.md)
* [修改或停止行銷活動](modify-stop-campaign.md)
* [行銷活動即時報告](campaign-live-report.md)
* [行銷活動全域報告](campaign-global-report.md)

## 存取行銷活動 {#access}

可從 **[!UICONTROL Campaigns]** 的子菜單。

預設情況下，清單顯示所有市場活動 **[!UICONTROL Draft]**。 **[!UICONTROL Scheduled]**, **[!UICONTROL Live]** 狀態。 要顯示已停止、已完成和存檔的市場活動，您需要清除篩選器。

![](assets/create-campaign-list.png)

## 市場活動狀態 {#statuses}

市場活動可以具有多種狀態：

* **[!UICONTROL Draft]**:市場活動正在編輯，尚未激活。
* **[!UICONTROL Activating]**:活動正在激活。
* **[!UICONTROL Live]**:活動已激活。
* **[!UICONTROL Scheduled]**:市場活動已配置為在特定開始日期激活。
* **[!UICONTROL Stopped]**:市場活動已手動停止。 您不能再激活或重新使用它(請參見 [停止市場活動](modify-stop-campaign.md#stop))
* **[!UICONTROL Completed]**:市場活動已完成。
* **[!UICONTROL Archived]**:市場活動已存檔。

>[!NOTE]
>
>「開啟草稿版本」表徵圖 **[!UICONTROL Live]** 或 **[!UICONTROL Scheduled]** 狀態表示已建立市場活動的新版本，但尚未激活(請參閱 [修改市場活動](modify-stop-campaign.md#modify))。
