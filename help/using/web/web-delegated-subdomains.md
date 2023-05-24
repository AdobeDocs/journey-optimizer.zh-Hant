---
solution: Journey Optimizer
product: journey optimizer
title: 設定網路子網域
description: 瞭解如何與Journey Optimizer建立Web子域
role: Admin
level: Intermediate
keywords: web，子域，配置
exl-id: 6503d9e6-6c6c-4a6d-ad3d-1d81eb3b4698
source-git-commit: 40cdcace9788206ad32dc6ae1e5f70c66e684bcb
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

創作Web體驗時，如果添加來自 [Adobe Experience Manager Assets Essentials](../email/assets-essentials.md) 庫，必須設定將用於發佈此內容的子域。

為此，必須從已委託給Adobe的子域清單中進行選擇。 瞭解有關將子域委託給Adobe的詳細資訊 [此部分](../configuration/delegate-subdomain.md)。

>[!CAUTION]
>
>Web子域配置對所有環境都是通用的。 因此：
>
>* 要訪問和編輯Web子域，必須 **[!UICONTROL 管理Web子域]** 在生產沙盒上的權限。
>
> * 對Web子域的任何修改也會影響生產沙盒。


您可以建立多個Web子域，但僅 **預設** 將使用子域。 您可以更改預設的Web子域，但一次只能使用一個子域。

1. 訪問 **[!UICONTROL 管理]** > **[!UICONTROL 頻道]** ，然後選擇 **[!UICONTROL Web配置]** > **[!UICONTROL Web子域]**。

   ![](assets/web-access-subdomains.png)

1. 按一下 **[!UICONTROL 設定子域]**。

1. 從清單中選擇委派的子域。

   ![](assets/web-subdomain-details.png)

   >[!NOTE]
   >
   >不能選擇已用作Web子域的子域。

1. 將自動添加顯示在Web URL中的前置詞。 你不能改變它。

1. 要將此子域設定為預設值，請選擇相應的選項。

   ![](assets/web-subdomain-details-default.png)

   >[!NOTE]
   >
   >僅 **預設** 將使用子域。

1. 按一下&#x200B;**[!UICONTROL 提交]**. 子域獲取 **[!UICONTROL 成功]** 狀態。 它已準備好用於您的Web體驗。

   >[!NOTE]
   >
   >在極少的情況下，子域設定可能會失敗。 在這種情況下，您可以刪除 **[!UICONTROL 失敗]** 使用 **[!UICONTROL 刪除]** 按鈕 **[!UICONTROL 更多操作]** 表徵圖

1. 的 **[!UICONTROL 預設]** 標籤顯示在當前用作預設值的子域旁邊。 要更改預設子域，請選擇 **[!UICONTROL 設定為預設值]** 從 **[!UICONTROL 更多操作]** 按鈕。

   ![](assets/web-subdomain-default.png)

   >[!NOTE]
   >
   >您可以更改預設的Web子域，但一次只能使用一個子域。

   <!--Only a subdomain with the **[!UICONTROL Success]** status can be set as default.

    You cannot delete a subdomain with the **[!UICONTROL Processing]** status.-->
