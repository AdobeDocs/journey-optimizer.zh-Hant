---
title: 沙箱管理
description: 了解如何管理沙箱
page-status-flag: never-activated
uuid: null
contentOwner: null
products: null
audience: administrators
content-type: reference
topic-tags: null
discoiquuid: null
internal: n
snippet: y
exl-id: null
source-git-commit: e4f69cd209665e7f13a0c21e92453cd5cdce45a1
workflow-type: tm+mt
source-wordcount: '324'
ht-degree: 27%

---

# 沙箱管理 {#sandboxes}

![](../assets/do-not-localize/badge.png)

## 使用沙箱{#using-sandbox}

[!DNL Journey Optimizer] 可讓您將執行個體分割到名為沙箱的個別虛擬環境中。會透過 Admin Console 中的產品設定檔指派沙箱。[了解如何指派沙箱](permissions.md#create-product-profile)。

[!DNL Journey Optimizer] 會反映針對指定組織建立的Adobe Experience Platform沙箱。可從 Adobe Experience Platform 執行個體建立或重設 Adobe Experience Platform 沙箱。[進一步了解沙箱使用手冊](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/user-guide.html)。

您可在螢幕左上方找到沙箱切換器控制項。若要從一個沙箱切換至另一個沙箱，請按一下切換器中目前作用中的沙箱，然後從下拉式清單中選取另一個沙箱。

## 指派沙箱{#assign-sandboxes}

>[!IMPORTANT]
>
> 沙箱管理只能由&#x200B;**[!UICONTROL Product]**&#x200B;或&#x200B;**[!UICONTROL System]**&#x200B;管理員執行。 如需詳細資訊，請參閱[管理控制台檔案](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/admin-roles.ug.html)。

您可以選擇將不同的沙箱指派給現成可用或自訂&#x200B;**[!UICONTROL Product profiles]**。

若要指派沙箱：

1. 在[!DNL Admin Console]中，從&#x200B;**[!UICONTROL Products]**&#x200B;標籤中，選擇&#x200B;**[!UICONTROL Adobe Experience Platform Apps]**&#x200B;產品。

1. 選取 **[!UICONTROL Product profile]**。

1. 選取 **[!UICONTROL Permissions]** 索引標籤。

1. 選擇&#x200B;**[!UICONTROL Sandbox access]**&#x200B;功能。

1. 在 **[!UICONTROL Available Permissions Items]** 下方，按一下加號 (+) 圖示，將沙箱指派給您的設定檔。[深入了解沙箱](https://experienceleague.adobe.com/docs/experience-platform/sandbox/home.html)。

1. 如有需要，請在&#x200B;**[!UICONTROL Included Permission Items]**&#x200B;下，按一下旁邊的X圖示，移除存取您&#x200B;**[!UICONTROL Product profile]**&#x200B;的沙箱。

1. 按一下「**[!UICONTROL Save]**」。

## 內容存取{#content-access}

若要設定內容協助工具，您需要將內容共用資料夾指派給每個沙箱。 您可以在[!DNL Admin Console]中顯示的&#x200B;**[!UICONTROL Storage]**&#x200B;標籤中，為管理員建立和配置共用資料夾。 如果您以系統管理員的身份可以訪問[!DNL Admin Console]，則可以建立共用資料夾，並將具有不同訪問級別的委派添加到共用資料夾。

![](../assets/do-not-localize/content_access.png)

請注意，若要讓內容與正確的沙箱同步，您必須遵循與沙箱相同的語法，例如，如果您的沙箱稱為開發，您的共用資料夾應具有相同名稱。

[了解如何管理共用資料夾](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-adobe-storage.ug.html)。
