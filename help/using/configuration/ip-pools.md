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
feature: 應用程式設定
topic: 管理
role: Admin
level: Intermediate
source-git-commit: 63de381ea3a87b9a77bc6f1643272597b50ed575
workflow-type: tm+mt
source-wordcount: '287'
ht-degree: 3%

---


# 建立 IP 池

## 關於IP池

使用Journey Optimizer，您可以建立IP池，將子網域的IP位址分組。

強烈建議建立IP池以實現電子郵件傳遞。 如此一來，您就能防止子網域的信譽影響其他子網域。

例如，一個最佳實務是為行銷訊息建立一個IP池，為交易式訊息另一個IP池。 這樣，如果您的其中一個行銷訊息執行不良，且被客戶宣告為垃圾訊息，則不會影響傳送給同一位客戶的交易式訊息，該客戶仍會收到交易式訊息（購買確認、密碼復原訊息等）。

## 建立IP池

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

要編輯IP池，請開啟它，然後根據需要編輯其屬性。

>[!NOTE]
>
>如果消息預設集已與IP池關聯，則首先需要先將其刪除，然後再編輯IP池。 完成修改後，您可以重新建立訊息預設集的關聯。
