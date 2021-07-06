---
title: 沙盒管理
description: 了解如何管理沙箱
feature: 控制組
topic: 管理
role: Administrator
level: Intermediate
source-git-commit: b07970ff11f1ba7c4e6db30dc2eca1252a579ca4
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 69%

---

# 沙盒管理 {#sandboxes}

## 使用沙箱 {#using-sandbox}

[!DNL Journey Optimizer] 可讓您將執行個體分割到名為沙箱的個別虛擬環境中。會透過 Admin Console 中的產品設定檔指派沙箱。[瞭解如何指派 sandbox](permissions.md#create-product-profile)。

[!DNL Journey Optimizer] 反映針對指定組織建立的 Adobe Experience Platform sandbox。
可從 Adobe Experience Platform 執行個體建立或重設 Adobe Experience Platform sandbox。[請參閱沙箱使用手冊](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/user-guide.html?lang=zh-Hant){target=&quot;_blank&quot;}以了解更多資訊。

您可在螢幕左上方找到沙箱切換器控制項。若要從一個沙箱切換至另一個沙箱，請按一下切換器中目前作用中的沙箱，然後從下拉式清單中選取另一個沙箱。

## 指派沙箱 {#assign-sandboxes}

>[!IMPORTANT]
>
> 沙箱管理只能由&#x200B;**[!UICONTROL Product]**&#x200B;或&#x200B;**[!UICONTROL System]**&#x200B;管理員執行。 如需詳細資訊，請參閱[管理控制台檔案](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/admin-roles.ug.html){target=&quot;_blank&quot;}。

您可以選擇將不同的沙箱指派給現成可用或自訂&#x200B;**[!UICONTROL Product profiles]**。

若要指派沙箱：

1. 在[!DNL Admin Console]中，從&#x200B;**[!UICONTROL Products]**&#x200B;標籤中，選擇&#x200B;**[!UICONTROL Adobe Experience Platform Apps]**&#x200B;產品。

1. 選取 **[!UICONTROL Product profile]**。

   ![](../assets/sandbox_1.png)

1. 選取 **[!UICONTROL Permissions]** 索引標籤。

1. 選擇&#x200B;**[!UICONTROL Sandboxes]**&#x200B;功能。

   ![](../assets/sandbox_2.png)

1. 在 **[!UICONTROL Available Permissions Items]** 下方，按一下加號 (+) 圖示，將沙箱指派給您的設定檔。[深入了解沙箱](https://experienceleague.adobe.com/docs/experience-platform/sandbox/home.html?lang=zh-Hant){target=&quot;_blank&quot;}。

   ![](../assets/sandbox_3.png)

1. 如有需要，請在&#x200B;**[!UICONTROL Included Permission Items]**&#x200B;下，按一下旁邊的X圖示，移除存取您&#x200B;**[!UICONTROL Product profile]**&#x200B;的沙箱。

   ![](../assets/sandbox_4.png)

1. 按一下「**[!UICONTROL Save]**」。

## 存取內容 {#content-access}

若要設定內容協助功能，您必須將內容共用資料夾指派給每個 sandbox。 您可以在[!DNL Admin Console]中顯示的&#x200B;**[!UICONTROL Storage]**&#x200B;標籤中為管理員建立和設定共用資料夾。 如果您以系統管理員的身份可以存取[!DNL Admin Console]，則可以建立共用資料夾，並將具有不同存取等級的指派新增到共用資料夾。

![](../assets/do-not-localize/content_access.png)

請注意，若要讓內容與正確的 sandbox 同步，您必須遵循與 sandbox 相同的語法，例如，如果您的 sandbox 被稱為開發，您的共用資料夾應具有相同的名稱。

[了解如何管理共用資料夾](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-adobe-storage.ug.html){target=&quot;_blank&quot;}。
