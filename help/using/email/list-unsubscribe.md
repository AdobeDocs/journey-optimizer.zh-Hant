---
solution: Journey Optimizer
product: journey optimizer
title: 設定電子郵件設定
description: 瞭解如何在頻道設定層級設定List-Unsubscribe
feature: Email, Surface
topic: Administration
role: Admin
level: Experienced
keywords: 設定、電子郵件、設定
source-git-commit: d782c668b412cebeacd1289c79bbf86ec710786b
workflow-type: tm+mt
source-wordcount: '770'
ht-degree: 38%

---

# 清單取消訂閱{#list-unsubscribe}

<!--Do not modify - Legal Review Done -->

設定新的電子郵件通道組態時，從清單中選取[子網域](email-settings.md#subdomains-and-ip-pools)後，會顯示&#x200B;**[!UICONTROL 啟用List-Unsubscribe]**&#x200B;選項。

![](assets/preset-list-unsubscribe.png)

## 啟用清單取消訂閱 {#enable-list-unsubscribe}

此選項預設為啟用，以在電子郵件標頭加入一鍵取消訂閱 URL，例如：

![](assets/preset-list-unsubscribe-header.png)

>[!NOTE]
>
>如果停用此選項，一鍵取消訂閱 URL 將不會顯示在電子郵件標頭。

List unsubscribe標頭提供兩個選項，除非您取消勾選其中一個或兩者，否則預設會啟用：

![](assets/surface-list-unsubscribe.png){width="80%"}

* **[!UICONTROL Mailto（取消訂閱）]**&#x200B;位址，這是將取消訂閱要求路由至進行自動處理的目標位址。

  在[!DNL Journey Optimizer]中，取消訂閱的電子郵件地址是根據您[選取的子網域](#subdomains-and-ip-pools)，顯示在頻道設定中的預設&#x200B;**[!UICONTROL Mailto （取消訂閱）]**&#x200B;位址。<!--With this method, clicking the Unsubscribe link sends a pre-filled email to the unsubscribe address specified in the email header.-->

* **[!UICONTROL 一鍵取消訂閱URL]**，根據您在通道組態設定中設定和設定的子網域，預設為一鍵選擇退出URL產生的清單取消訂閱標頭。<!--With this method, clicking the Unsubscribe link directly unsubscribes the user, requiring only a single action to unsubscribe.-->

您可以從對應的下拉式清單中選取&#x200B;**[!UICONTROL 同意層級]**。 它可特定於頻道或設定檔身分。根據此設定，當使用者使用電子郵件標題中的清單取消訂閱URL取消訂閱時，同意會在[!DNL Adobe Journey Optimizer]中更新（在頻道層級或識別碼層級）。

**[!UICONTROL Mailto（取消訂閱）]**&#x200B;功能和&#x200B;**[!UICONTROL 一鍵取消訂閱 URL]** 功能是選用功能。

如果您不想使用預設產生的一鍵取消訂閱 URL，可以取消勾選該功能。在&#x200B;**[!UICONTROL 啟用清單取消訂閱]**&#x200B;選項處於開啟狀態且&#x200B;**[!UICONTROL 一鍵取消訂閱 URL]** 功能處於取消勾選的情況下，如果您在使用此設定所建立的訊息中新增[一鍵退出連結](../email/email-opt-out.md#one-click-opt-out)，則清單取消訂閱標頭會獲取您在電子郵件內文插入的一鍵退出連結，並將其用作一鍵取消訂閱 URL 值。

![](assets/preset-list-unsubscribe-opt-out-url.png)

>[!NOTE]
>
>如果您未在訊息內容加入一鍵退出連結，且頻道組態設定中的預設&#x200B;**[!UICONTROL 一鍵取消訂閱 URL]** 已取消勾選，則清單取消訂閱標題的電子郵件標頭不會傳遞任何 URL。

在[本節](../email/email-opt-out.md#unsubscribe-header)中進一步瞭解如何管理訊息中的取消訂閱功能。

## 從外部管理取消訂閱的資料 {#custom-managed}

>[!CONTEXTUALHELP]
>id="ajo_email_config_unsubscribe_custom"
>title="定義如何管理取消訂閱的資料"
>abstract="**Adobe 管理**：同意資料由您在 Adobe 系統內進行管理。<br>**客戶管理**：同意資料由您在外部系統中進行管理，除非由您啟動，否則 Adobe 系統中不會同步更新同意資料。"

>[!AVAILABILITY]
>
>此功能以有限可用性 (LA) 形式向一小部分客戶發布。

如果您是在Adobe外部管理同意，請選取&#x200B;**[!UICONTROL 客戶管理的]**&#x200B;選項，以輸入自訂取消訂閱電子郵件地址和您自己的一鍵取消訂閱URL。

![](assets/surface-list-unsubscribe-custom.png){width="80%"}

>[!WARNING]
>
>如果您使用&#x200B;**[!UICONTROL 客戶管理的]**&#x200B;選項，Adobe不會儲存任何取消訂閱或同意的資料。 使用&#x200B;**[!UICONTROL 客戶受管理]**&#x200B;選項，組織會選擇使用外部系統，並負責在此類外部系統中管理其同意資料。 外部系統與[!DNL Journey Optimizer]之間沒有自動同步同意資料。 同意資料的任何同步作業源自外部系統，以更新[!DNL Journey Optimizer]中的使用者同意資料，必須由組織以資料傳輸方式啟動，以將同意資料推送回[!DNL Journey Optimizer]。

## 設定解密API {#configure-decrypt-api}

選取&#x200B;**[!UICONTROL 客戶受管理]**&#x200B;選項後，如果您輸入自訂端點，並在行銷活動或歷程中使用它們，當您的收件者按一下[取消訂閱]連結時，[!DNL Journey Optimizer]會將一些預設設定檔特定引數附加至同意更新事件<!--sent to the custom endpoint -->。

這些引數會以加密方式傳送至端點。 因此，外部同意系統需要透過[Adobe Developer](https://developer.adobe.com){target="_blank"}實作特定API，以解密Adobe傳送的引數。

擷取這些引數的GET呼叫取決於您正在使用的清單取消訂閱選項 — **[!UICONTROL 按一下取消訂閱URL]**&#x200B;或&#x200B;**[!UICONTROL Mailto （取消訂閱）]**。

<!--To configure the API to send back the information to [!DNL Adobe Journey Optimizer] when a recipient has unsubscribed using the List unsubscribe option with custom endpoints, follow the steps below.-->

+++ 一鍵式取消訂閱URL

使用&#x200B;**[!UICONTROL 一鍵取消訂閱URL]**&#x200B;選項，按一下「取消訂閱」連結即可直接取消訂閱使用者。

GET呼叫如下：

端點：https://platform.adobe.io/journey/imp/consent/decrypt

查詢參數：

* **params**：包含加密的裝載
* **pid**：加密的輪廓 ID

這兩個引數將包含在傳送至自訂端點的同意更新事件中。

頁首需求：

* x-api-key
* x-gw-ims-org-id
* 授權 (來自您技術帳戶的使用者權杖)

+++

+++ Mailto （取消訂閱）

使用&#x200B;**[!UICONTROL Mailto （取消訂閱）]**&#x200B;選項，按一下[取消訂閱]連結會傳送預先填入的電子郵件給指定的取消訂閱地址。

GET呼叫如下。

端點：https://platform.adobe.io/journey/imp/consent/decrypt

查詢參數：

* **emailParams**：包含&#x200B;**params** （加密裝載）和&#x200B;**pid** （加密設定檔ID）引數的字串。

**引數**&#x200B;和&#x200B;**pid**&#x200B;引數將包含在傳送給自訂端點的同意更新事件中。

頁首需求：

* x-api-key
* x-gw-ims-org-id
* 授權 (來自您技術帳戶的使用者權杖)

+++
