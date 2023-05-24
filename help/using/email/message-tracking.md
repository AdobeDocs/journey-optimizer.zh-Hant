---
solution: Journey Optimizer
product: journey optimizer
title: 追蹤您的訊息
description: 了解如何新增連結和追蹤已傳送的訊息
feature: Monitoring
topic: Content Management
role: User
level: Intermediate
keywords: 連結、跟蹤、監視、電子郵件
exl-id: 689e630a-00ca-4893-8bf5-6d1ec60c52e7
source-git-commit: 9592e9c1b0e9c8a1c606a9a187501542e496eddb
workflow-type: tm+mt
source-wordcount: '885'
ht-degree: 38%

---

# 新增連結及追蹤訊息 {#tracking}

使用 [!DNL Journey Optimizer] 添加內容連結並跟蹤發送的郵件以監視收件人的行為。

## 啟用跟蹤 {#enable-tracking}

您可以通過檢查 **[!UICONTROL 開啟電子郵件]** 和/或 **[!UICONTROL 按一下電子郵件]** 在行程或市場活動中建立消息時的選項。

>[!BEGINTABS]

>[!TAB 啟用行程跟蹤]

![](assets/message-tracking-journey.png)

>[!TAB 在市場活動中啟用跟蹤]

![](assets/message-tracking-campaign.png)

>[!ENDTABS]

>[!NOTE]
>
>預設情況下，兩個選項都處於啟用狀態。

這將允許您通過以下方式跟蹤收件人的行為：

* **[!UICONTROL 開啟電子郵件]**:已開啟的郵件。
* **[!UICONTROL 按一下電子郵件]**:按一下電子郵件中的連結。

## 插入連結 {#insert-links}

設計訊息，您可以新增連結到您的內容。

>[!NOTE]
>
>當 [已啟用跟蹤](#enable-tracking)，將跟蹤消息內容中包含的所有連結。

若要將連結插入到電子郵件內容，請依照以下步驟操作：

1. 選取元素，然後從內容關聯式工具列中按一下「**[!UICONTROL 插入連結]**」。

   ![](assets/message-tracking-insert-link.png)

1. 選擇要建立的連結類型：

   * **[!UICONTROL 外部連結]**:插入指向外部URL的連結。

   * **[!UICONTROL 登錄頁]**:插入到登錄頁的連結。 請參閱[本節](../landing-pages/get-started-lp.md)以進一步瞭解

   * **[!UICONTROL 按一下「選擇退出」]**:插入連結，使用戶能夠快速取消訂閱您的通信，而無需確認退出。 請參閱[此章節](../privacy/opt-out.md#one-click-opt-out)深入瞭解。

   * **[!UICONTROL 外部選擇加入/訂閱]**:插入一個連結以接受來自您品牌的通信。

   * **[!UICONTROL 外部選擇退出/取消訂閱]**:插入連結以取消訂閱從您的品牌接收通信。 進一步瞭解[本章節](../privacy/opt-out.md#opt-out-management)中的選擇退出管理。

   * **[!UICONTROL 「鏡像」頁]**:插入連結以在Web瀏覽器中顯示電子郵件內容。 請參閱[此章節](#mirror-page)深入瞭解。

1. 您可以個人化連結。 進一步瞭解[本章節](../personalization/personalization-syntax.md#perso-urls)的個人化 URL。

1. 儲存您的變更。

1. 建立連結後，您仍然可以從右側的「**[!UICONTROL 元件設定]**」窗格中修改。

   * 可以編輯連結並更改其類型。
   * 您可以透過勾選對應的選項來選擇是否為連結加底線。

   ![](assets/message-tracking-link-settings.png)

>[!NOTE]
>
>市場營銷類型的電子郵件必須包括 [選擇退出連結](../privacy/opt-out.md#opt-out-management)，事務性消息不需要。 消息類別(**[!UICONTROL 營銷]** 或 **[!UICONTROL 事務性]**) [通道表面](../configuration/channel-surfaces.md#email-type) 建立消息時。

## 連結到鏡像頁 {#mirror-page}

鏡像頁面是可透過網頁瀏覽器線上存取的 HTML 頁面。其內容與您的電子郵件內容相同。

要在電子郵件中添加鏡像頁的連結， [插入連結](#insert-links) 選擇 **[!UICONTROL 「鏡像」頁]** 作為連結的類型。

![](assets/message-tracking-mirror-page.png)

鏡像頁面會自動建立。

>[!IMPORTANT]
>
>鏡像頁面連結是自動產生的，無法編輯。它們包含轉譯原始電子郵件所需的所有加密的個人化資料。因此，使用具有較大值的個人化屬性可能會產生冗長的鏡像頁面 URL，如果網頁瀏覽器具有最大 URL 長度，將導致連結無法在該網頁瀏覽器中作用。

電子郵件傳送後，當收件者按一下鏡像頁面連結時，電子郵件的內容將顯示在他們的預設網頁瀏覽器中。

>[!NOTE]
>
>在 [證明](preview.md#send-proofs) 發送到test配置檔案時，指向鏡像頁面的連結不處於活動狀態。 它僅在最終訊息中啟用。

鏡像頁的保留期為60天。 延遲後，鏡像頁將不再可用。

## 管理追蹤 {#manage-tracking}

[電子郵件設計工具](content-from-scratch.md) 可讓您管理被追蹤的 URL，例如編輯每個連結的追蹤類型。

1. 按一下 **[!UICONTROL 連結]** 表徵圖，顯示要跟蹤的內容的所有URL的清單。

   此清單可讓您能夠集中檢視並找到電子郵件內容中的每個 URL。

1. 若要編輯連結，按一下對應的鉛筆圖示。

1. 您可以修改&#x200B;**[!UICONTROL 追蹤類型]** (如果需要)：

   ![](assets/message-tracking-edit-a-link.png)

   對於每個被追蹤的 URL，您可以將追蹤模式設定為以下其中一個值：

   * **[!UICONTROL 已追蹤]**：啟動追蹤此 URL。
   * **[!UICONTROL 選擇退出]**：將此 URL 視為選擇退出或取消訂閱 URL。
   * **[!UICONTROL 鏡像頁面]**：將此 URL 視為鏡像頁面 URL。
   * **[!UICONTROL 絕不]**：絕不啟動追蹤此 URL。<!--This information is saved: if the URL appears again in a future message, its tracking is automatically deactivated.-->

有關開放和點擊的報告，請參見 [即時報告](../reports/live-report.md) 在 [全局報告](../reports/global-report.md)。

## URL跟蹤 {#url-tracking}

通常 [URL跟蹤](email-settings.md#url-tracking) 在曲面層管理，但不支援配置檔案屬性。 目前唯一的辦法就是 [個性化URL](../personalization/personalization-syntax.md#perso-urls) 在電子郵件設計器中。

要將個性化URL跟蹤參數添加到連結，請執行以下步驟。

1. 選擇連結並按一下 **[!UICONTROL 插入連結]** 的子菜單。

1. 選擇個性化表徵圖。 它僅可用於以下類型的連結： **外部連結**。 **取消訂閱連結** 和 **選擇退出**。

   ![](assets/message-tracking-insert-link-perso.png)

1. 添加URL跟蹤參數，然後從表達式編輯器中選擇所選配置檔案屬性。

   ![](assets/message-tracking-perso-parameter.png)

1. 儲存您的變更。

1. 對要將此跟蹤參數添加到的每個連結重複上述步驟。

現在，當電子郵件發出時，此參數將自動附加到URL的末尾。 然後，可以在Web分析工具或效能報告中捕獲此參數。

>[!NOTE]
>
>要驗證最終URL，您可以 [發證](preview.md#send-proofs) 收到證明後，按一下電子郵件內容中的連結。 URL應顯示跟蹤參數。 在上例中，最終URL將是：https://luma.enablementadobe.com/content/luma/us/en.html?utm_contact=profile.userAccount.contactDetails.homePhone.number
