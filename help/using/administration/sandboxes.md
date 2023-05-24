---
solution: Journey Optimizer
product: journey optimizer
title: 沙盒管理
description: 瞭解如何管理沙箱
feature: Sandboxes
topic: Administration
role: Admin, Architect, Developer
level: Experienced
keywords: 箱、虛擬、環境、組織、平台
exl-id: 14f80d5d-0840-4b79-9922-6d557a7e1247
source-git-commit: 16738786e4ebeef3417fd0f6e5be741b348c2744
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 54%

---

# 沙盒管理 {#sandboxes}

## 使用沙箱 {#using-sandbox}

[!DNL Journey Optimizer] 可讓您將執行個體分割到名為沙箱的個別虛擬環境中。會透過 Admin Console 中的產品設定檔指派沙箱。[瞭解如何指派 sandbox](permissions.md#create-product-profile)。

[!DNL Journey Optimizer] 反映針對指定組織建立的 Adobe Experience Platform sandbox。
可從 Adobe Experience Platform 執行個體建立或重設 Adobe Experience Platform sandbox。[在「沙盒」使用手冊中瞭解更多資訊](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/user-guide.html?lang=zh-Hant){target="_blank"}。

您可以在您的組織名稱旁的螢幕右上角找到沙盒切換器控制項。 若要從一個沙箱切換至另一個沙箱，請按一下切換器中目前作用中的沙箱，然後從下拉式清單中選取另一個沙箱。

![](assets/sandbox_5.png)

➡️ [瞭解有關此視頻中沙盒的詳細資訊](#video)

## 分配沙箱 {#assign-sandboxes}

>[!IMPORTANT]
>
> 沙箱管理只能由 **[!UICONTROL 產品]** 或 **[!UICONTROL 系統]** 管理員。 有關此項的詳細資訊，請參閱 [管理控制台文檔](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/admin-roles.ug.html){target="_blank"}。

您可以選擇將不同的沙箱分配給出廠設定或自定義 **[!UICONTROL 產品配置檔案]**。

要分配沙箱：

1. 在 [!DNL Admin Console]，也請參見Wiki頁。 **[!UICONTROL 產品]** 頁籤 **[!UICONTROL Adobe Experience Platform應用]** 產品。

1. 選擇 **[!UICONTROL 產品配置檔案]**。

   ![](assets/sandbox_1.png)

1. 選擇 **[!UICONTROL 權限]** 頁籤。

1. 選擇 **[!UICONTROL 沙箱]** 功能。

   ![](assets/sandbox_2.png)

1. 下 **[!UICONTROL 可用權限項]**，按一下加號(+)表徵圖將沙箱指定給您的配置檔案。 [瞭解有關沙箱的詳細資訊](https://experienceleague.adobe.com/docs/experience-platform/sandbox/home.html?lang=zh-Hant){target="_blank"}。

   ![](assets/sandbox_3.png)

1. 如果需要，在 **[!UICONTROL 包括的權限項]**，按一下「X」表徵圖，刪除對 **[!UICONTROL 產品配置檔案]**。

   ![](assets/sandbox_4.png)

1. 按一下&#x200B;**[!UICONTROL 儲存]**。

## 存取內容 {#content-access}

若要設定內容協助功能，您必須將內容共用資料夾指派給每個 sandbox。 您可以在 **[!UICONTROL 儲存]** 頁籤 [!DNL Admin Console] 為管理員。 如果您以系統管理員的身份可以存取[!DNL Admin Console]，則可以建立共用資料夾，並將具有不同存取等級的指派新增到共用資料夾。

![](assets/do-not-localize/content_access.png)

請注意，若要讓內容與正確的 sandbox 同步，您必須遵循與 sandbox 相同的語法，例如，如果您的 sandbox 被稱為開發，您的共用資料夾應具有相同的名稱。

[瞭解如何管理共用資料夾](https://helpx.adobe.com/tw/enterprise/admin-guide.html/enterprise/using/manage-adobe-storage.ug.html){target="_blank"}。

## 操作說明影片{#video}

瞭解何謂沙箱，以及如何區分開發沙箱和生產沙箱。 瞭解如何建立、重設和刪除沙箱。

>[!VIDEO](https://video.tv.adobe.com/v/334355?quality=12)
