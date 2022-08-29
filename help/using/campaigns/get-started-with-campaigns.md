---
title: 開始使用行銷活動
description: 瞭解有關中的市場活動的更多資訊 [!DNL Journey Optimizer]
feature: Overview
topic: Content Management
role: User
level: Intermediate
exl-id: e2506a43-e4f5-48af-bd14-ab76c54b7c90
source-git-commit: b73d4495a231a40d833f4fee4dc094b808d659bd
workflow-type: tm+mt
source-wordcount: '488'
ht-degree: 4%

---

# 開始使用行銷活動 {#get-started-campaigns}

>[!CONTEXTUALHELP]
>id="campaigns_list"
>title="Campaigns"
>abstract="建立活動，跨各種渠道將一次性內容交付到特定領域。 在建立市場活動之前，請確保您有一個頻道表面（即消息預設）和一個Adobe Experience Platform段可供使用。"

使用Journey Optimizer市場活動，通過各種渠道將一次性內容交付到特定市場。 使用行程時，按順序執行動作。 對於市場活動，活動可以同時執行，也可以立即執行，或者根據指定的時間表執行。

建立市場活動，以發送簡單的臨時批通信，以用於市場營銷用例，如促銷優惠、接洽活動、公告、法律通知或策略更新。

➡️ [在影片中探索此功能](#video)

<!--You can create two types of campaigns:

* **Scheduled campaigns** allow for simple ad-hoc batch communications for marketing use cases like promotional offers, engagement campaigns, announcements, legal notices, or policy updates.
* **API Triggered Campaigns** allow for simple transactional/operational messages with REST APIs (password reset, card abandonment, etc.), where the need may involve personalization using profile attributes and contextual data from payload.-->

## 開始之前 {#campaign-prerequisites}

在開始在Journey Optimizer建立第一個市場活動之前，請檢查以下先決條件：

1. **您需要適當的權限**。 市場活動僅對有權訪問與市場活動相關的用戶可用 **[!UICONTROL Product profile]** 例如市場活動管理員、市場活動批准者、市場活動經理和/或市場活動查看者。

   如果無法訪問市場活動，則必須擴展您的權限。 如果您有權訪問 [Adobe Admin Console](https://adminconsole.adobe.com/){target=&quot;_blank&quot;}，請執行以下步驟。 否則，請與您的Journey Optimizer管理員聯繫。

   +++瞭解如何分配市場活動權限

   分配相應 **[!UICONTROL Product profile]** 到用戶：

   1. 從 [!DNL Admin console]，選擇 [!DNL Adobe Experience Platform] 產品。

   1. 從 **[!UICONTROL Product profile]** 頁籤，選擇與市場活動相關的內置市場活動之一 **[!UICONTROL Product profile]**:市場活動管理員、市場活動批准者、市場活動經理或市場活動查看者。

      有關Journey Optimizer活動的詳細資訊 **[!UICONTROL Product profiles]** 和 **[!UICONTROL Permissions]**。 [請參閱此頁](../administration/ootb-product-profiles.md)。

      ![](assets/do-not-localize/admin_1.png)

   1. 按一下 **[!UICONTROL Add user]** 分配給所選用戶 **[!UICONTROL Product profile]**。

      ![](assets/do-not-localize/admin_2.png)

   1. 鍵入用戶的名稱、組或電子郵件地址，然後按一下 **[!UICONTROL Save]**。
   您的用戶現在將能夠訪問 **[!UICONTROL Campaigns]**。

+++

1. **你需要一個觀眾**。 在建立市場活動之前，需要提供受眾群。 瞭解有關受眾建立的更多資訊 [此頁](../segment/about-segments.md)。
1. **你需要一個通道表面**。 要能夠選擇通道，必須建立並可用相應的通道曲面（即預設）。 瞭解有關通道曲面的詳細資訊 [此頁](../configuration/channel-surfaces.md)

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
* **[!UICONTROL Completed]**:市場活動已完成。 在激活市場活動3天後，或在市場活動結束日期（如果市場活動已定期執行）自動分配此狀態。
* **[!UICONTROL Archived]**:市場活動已存檔。

>[!NOTE]
>
>「開啟草稿版本」表徵圖 **[!UICONTROL Live]** 或 **[!UICONTROL Scheduled]** 狀態表示已建立市場活動的新版本，但尚未激活(請參閱 [修改市場活動](modify-stop-campaign.md#modify))。

## How-to視頻 {#video}

瞭解如何建立您的第一個市場活動。

>[!VIDEO](https://video.tv.adobe.com/v/346680?quality=12)
