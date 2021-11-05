---
title: 沙盒管理
description: 了解如何管理沙箱
feature: Control Groups
topic: Administration
role: Admin
level: Intermediate
exl-id: 14f80d5d-0840-4b79-9922-6d557a7e1247
source-git-commit: 0f79d465dd5a63ced107614407de167c7d9dad5a
workflow-type: tm+mt
source-wordcount: '360'
ht-degree: 71%

---

# 沙盒管理 {#sandboxes}

## 使用沙箱 {#using-sandbox}

[!DNL Journey Optimizer] 可讓您將執行個體分割到名為沙箱的個別虛擬環境中。會透過 Admin Console 中的產品設定檔指派沙箱。[瞭解如何指派 sandbox](permissions.md#create-product-profile)。

[!DNL Journey Optimizer] 反映針對指定組織建立的 Adobe Experience Platform sandbox。
可從 Adobe Experience Platform 執行個體建立或重設 Adobe Experience Platform sandbox。[進一步了解沙箱使用手冊](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/user-guide.html?lang=zh-Hant){target=&quot;_blank&quot;}。

您可在螢幕左上方找到沙箱切換器控制項。若要從一個沙箱切換至另一個沙箱，請按一下切換器中目前作用中的沙箱，然後從下拉式清單中選取另一個沙箱。

➡️ [在影片中探索此功能](#video)

## 指派沙箱 {#assign-sandboxes}

>[!IMPORTANT]
>
> 沙箱管理只能由 **[!UICONTROL Product]** 或 **[!UICONTROL System]** 管理員。 如需詳細資訊，請參閱 [Admin Console檔案](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/admin-roles.ug.html){target=&quot;_blank&quot;}。

您可以選擇將不同的沙箱指派給現成可用或自訂 **[!UICONTROL Product profiles]**.

若要指派沙箱：

1. 在 [!DNL Admin Console]，從 **[!UICONTROL Products]** 頁簽，選擇 **[!UICONTROL Adobe Experience Platform Apps]** 產品。

1. 選取 **[!UICONTROL Product profile]**。

   ![](../assets/sandbox_1.png)

1. 選取 **[!UICONTROL Permissions]** 索引標籤。

1. 選取 **[!UICONTROL Sandboxes]** 功能。

   ![](../assets/sandbox_2.png)

1. 在 **[!UICONTROL Available Permissions Items]** 下方，按一下加號 (+) 圖示，將沙箱指派給您的設定檔。[深入了解沙箱](https://experienceleague.adobe.com/docs/experience-platform/sandbox/home.html?lang=zh-Hant){target=&quot;_blank&quot;}。

   ![](../assets/sandbox_3.png)

1. 如有需要，在 **[!UICONTROL Included Permission Items]**，按一下旁邊的X圖示，移除您 **[!UICONTROL Product profile]**.

   ![](../assets/sandbox_4.png)

1. 按一下「**[!UICONTROL Save]**」。

## 存取內容 {#content-access}

若要設定內容協助功能，您必須將內容共用資料夾指派給每個 sandbox。 您可以在[!DNL Admin Console]中顯示的&#x200B;**[!UICONTROL Storage]**&#x200B;標籤中為管理員建立和設定共用資料夾。 如果您以系統管理員的身份可以存取[!DNL Admin Console]，則可以建立共用資料夾，並將具有不同存取等級的指派新增到共用資料夾。

![](../assets/do-not-localize/content_access.png)

請注意，若要讓內容與正確的 sandbox 同步，您必須遵循與 sandbox 相同的語法，例如，如果您的 sandbox 被稱為開發，您的共用資料夾應具有相同的名稱。

[了解如何管理共用資料夾](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-adobe-storage.ug.html){target=&quot;_blank&quot;}。

## 作法影片{#video}

瞭解何謂沙箱，以及如何區分開發沙箱和生產沙箱。 瞭解如何建立、重設和刪除沙箱。

>[!VIDEO](https://video.tv.adobe.com/v/334355?quality=12)
