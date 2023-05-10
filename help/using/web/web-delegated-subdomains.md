---
solution: Journey Optimizer
product: journey optimizer
title: 設定網路子網域
description: 了解如何使用Journey Optimizer設定Web子網域
role: Admin
level: Intermediate
keywords: web，子網域，設定
exl-id: 6503d9e6-6c6c-4a6d-ad3d-1d81eb3b4698
source-git-commit: 66ef57c263d29572ce0377e41bf0a8010e2f22d1
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 27%

---

# 設定網路子網域 {#web-subdomains}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_web_header"
>title="委派網頁子網域"
>abstract="您將設定您的子網域以供網頁管道使用。從已委派給 Adobe 的子網域進行選擇。"

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_web"
>title="委派網頁子網域"
>abstract="如果您將來自 Adobe Experience Manager Assets Essentials 的內容新增到您的網頁體驗中，則必須設定將用來發佈此內容的子網域。在已委派給 Adobe 的子網域中選取。"

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_web_default"
>title="設定網頁子網域"
>abstract="從已委派給 Adobe 的子網域清單中選取一個子網域。您可以將此網頁子網域設定為預設子網域，但一次只能使用一個預設子網域。"

撰寫網頁體驗時，如果您新增來自 [Adobe Experience Manager Assets Essentials](../email/assets-essentials.md) 程式庫，您必須設定將用來發佈此內容的子網域。

若要這麼做，您必須從已委派給Adobe的子網域清單中選擇。 進一步了解如何將子網域委派至Adobe [本節](../configuration/delegate-subdomain.md).

>[!CAUTION]
>
>Web子網域設定是所有環境通用的。 因此：
>
>* 若要存取及編輯Web子網域，您必須具備 **[!UICONTROL 管理Web子網域]** 對生產沙箱的權限。
>
> * 任何對Web子網域的修改也會影響生產沙箱。


您可以建立數個Web子網域，但只能建立 **預設** 會使用子網域。 您可以變更預設的Web子網域，但一次只能使用一個子網域。

1. 存取 **[!UICONTROL 管理]** > **[!UICONTROL 管道]** ，然後選取 **[!UICONTROL Web配置]** > **[!UICONTROL Web子網域]**.

   ![](assets/web-access-subdomains.png)

1. 按一下 **[!UICONTROL 設定子網域]**.

1. 從清單中選取委派的子網域。

   ![](assets/web-subdomain-details.png)

   >[!NOTE]
   >
   >您無法選取已用作Web子網域的子網域。

1. 系統會自動新增將在您的網頁URL中顯示的首碼。 您無法變更。

1. 若要將此子網域設為預設值，請選取對應的選項。

   ![](assets/web-subdomain-details-default.png)

   >[!NOTE]
   >
   >僅 **預設** 會使用子網域。

1. 按一下&#x200B;**[!UICONTROL 提交]**. 子網域會取得 **[!UICONTROL 成功]** 狀態。 它已準備好用於您的網頁體驗。

   >[!NOTE]
   >
   >在極少數的情況下，子網域設定可能會失敗。 在此情況下，您可以刪除 **[!UICONTROL 失敗]** 子網域來清除清單，使用 **[!UICONTROL 刪除]** 按鈕 **[!UICONTROL 更多動作]** 表徵圖。

1. 此 **[!UICONTROL 預設]** 徽章會顯示在目前作為預設的子網域旁。 若要變更預設子網域，請選取 **[!UICONTROL 設為預設值]** 從 **[!UICONTROL 更多動作]** 按鈕（位於所需子網域旁）。

   >[!NOTE]
   >
   >您可以變更預設的Web子網域，但一次只能使用一個子網域。

   ![](assets/web-subdomain-default.png)

   <!--Only a subdomain with the **[!UICONTROL Success]** status can be set as default.

    You cannot delete a subdomain with the **[!UICONTROL Processing]** status.-->
