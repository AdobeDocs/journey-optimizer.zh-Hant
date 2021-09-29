---
title: 建立 IP 池
description: '"了解如何管理ip池"'
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
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 606334c3-e3e6-41c1-a10e-63508a3ed747
source-git-commit: 7d7c1b72530d99b8cceb1067f2576ad66c0052a6
workflow-type: tm+mt
source-wordcount: '471'
ht-degree: 1%

---

# 建立 IP 池

## 關於IP池 {#about-ip-pools}

使用Journey Optimizer，您可以建立IP池，將子網域的IP位址分組。

強烈建議建立IP池以實現電子郵件傳遞。 如此一來，您就能防止子網域的信譽影響其他子網域。

例如，一個最佳實務是為行銷訊息建立一個IP池，為交易式訊息另一個IP池。 這樣，如果您的其中一個行銷訊息執行不良，且被客戶宣告為垃圾訊息，則不會影響傳送給同一位客戶的交易式訊息，該客戶仍會收到交易式訊息（購買確認、密碼復原訊息等）。

## 建立IP池 {#create-ip-pool}

要建立IP池，請執行以下步驟：

1. 訪問&#x200B;**[!UICONTROL Channels]** / **[!UICONTROL IP pools]**&#x200B;菜單，然後按一下&#x200B;**[!UICONTROL Create IP Pool]**。

   ![](../assets/ip-pool-create.png)

1. 提供IP池的名稱和說明（可選）。

   >[!NOTE]
   >
   >子網域的名稱必須以字母(A-Z)開頭，且僅包含英數字元或特殊字元(_、.、-)。

1. 從下拉清單中選擇要包含在池中的IP地址，然後按一下&#x200B;**[!UICONTROL Submit]**。

   ![](../assets/ip-pool-config.png)

   >[!NOTE]
   >
   >清單中會提供與您執行個體布建的所有IP位址。

IP池現在已建立並顯示在清單中。 您可以選取它以存取其屬性並顯示相關的訊息預設集。 有關如何將消息預設集與IP池關聯的詳細資訊，請參閱[此部分](message-presets.md))。

![](../assets/ip-pool-created.png)

## 編輯IP池 {#edit-ip-pool}

要編輯IP池，請執行以下操作：

1. 從清單中，按一下IP池名稱以開啟它。

   ![](../assets/ip-pool-list.png)

1. 視需要編輯其屬性。 您可以修改說明，以及新增或移除IP位址。

   ![](../assets/ip-pool-edit.png)

   >[!CAUTION]
   >
   >考慮刪除IP時請格外小心，因為這會對其他IP造成額外負載，且可能對您的傳送能力造成嚴重影響。 如有疑問，請聯絡傳遞能力專家。

1. 儲存您的變更。

>[!NOTE]
>
>IP池名稱不可編輯。 如果要修改它，則需要刪除IP池，並使用您選擇的名稱建立另一個池。

根據與[消息預設集](message-presets.md)關聯的IP池，更新會立即或非同步地生效：

* 如果在消息預設集中選擇的IP池&#x200B;**未**，則更新為瞬時（**[!UICONTROL Success]**&#x200B;狀態）。
* 如果在消息預設集中選擇了IP池&#x200B;****，則更新最多可能需要7-10個工作天（**[!UICONTROL Processing]**&#x200B;狀態）。

<!--If a message preset has been associated with the IP pool, you first need to remove it before editing the IP pool. Once the your modifications have been done, you can associate the message preset again.-->

要檢查IP池更新狀態，請按一下&#x200B;**[!UICONTROL More actions]**&#x200B;按鈕並選擇&#x200B;**[!UICONTROL Recent updates]**。

![](../assets/ip-pool-recent-update.png)

>[!NOTE]
>
>成功更新IP池後，您可能需要等待：
>* 在被統一消息使用前幾分鐘，
>* 直到IP池的下一批處理在批處理消息中生效。


您也可以使用&#x200B;**[!UICONTROL Delete]**&#x200B;按鈕刪除IP池。 請注意，您無法刪除已與消息預設集關聯的IP池。

