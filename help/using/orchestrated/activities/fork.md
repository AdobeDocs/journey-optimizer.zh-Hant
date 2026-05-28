---
solution: Journey Optimizer
product: journey optimizer
title: 使用 [分支] 活動
description: 瞭解如何在協調的行銷活動中使用分叉活動
exl-id: 52e8057b-dac1-45f5-9dd0-1b28a59adde9
version: Campaign Orchestration
TQID: https://experienceleague.adobe.com/b0FyVaM0LcSz1DLGd-UEhHqBqXMWcb0rbimJA6E7WOM
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: b423a773-0a58-4a77-b65d-3dd4ae6ef841
subfeature_v2:
  - id: b5e335a9-0e5f-4dda-8845-c4ac5dca2be4
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 256
ht-degree: 47%

---

# 分支 {#fork}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_fork"
>title="分支活動"
>abstract="**分支**&#x200B;活動可讓您建立傳出轉變，以同時啟動多個活動。"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_fork_transitions"
>title="分支活動轉變"
>abstract="依預設，透過&#x200B;**分支**&#x200B;活動建立二個轉變。 按一下&#x200B;**新增轉變**&#x200B;按鈕以定義額外的傳出轉變，並輸入其標籤。"

**[!UICONTROL 分支]**&#x200B;活動是&#x200B;**[!UICONTROL 控制流量]**&#x200B;元件，讓可以您建立多個輸出轉變，並行執行多個活動。

## 設定分支活動{#fork-configuration}

請按照以下步驟設定「**[!UICONTROL 分支]**」活動：

![](../assets/workflow-fork.png)

1. 將&#x200B;**[!UICONTROL 分支]**&#x200B;活動新增至您的協調行銷活動。

1. 定義&#x200B;**[!UICONTROL 標籤]**。

1. 為每個傳出轉變指派標籤。 預設情況下，會提供兩種轉變。

1. 若想移除轉變，請按一下 ![](../assets/do-not-localize/Smock_Delete_18_N.svg) 圖示。

1. 如有需要，請按一下&#x200B;**[!UICONTROL 新增轉變]**，以便新增額外的輸出轉變。

## 範例 {#fork-examples}

以下是&#x200B;**[!UICONTROL 分支]**&#x200B;活動的典型用法：使用兩個不同的電子郵件管道（一個行銷和一個異動）來鎖定相同的對象，以比較傳送行為。

在&#x200B;**[!UICONTROL 建立對象]**&#x200B;活動選取目標母體後，**[!UICONTROL 分支]**&#x200B;會建立兩個平行分支：

* **分支1**&#x200B;連線至行銷電子郵件通道活動。 訊息會遵循標準商業規則，並僅傳送至選擇加入的設定檔。
* **分支2**&#x200B;連線到異動電子郵件通道活動。 訊息會繞過商業規則，並傳遞至所有設定檔，無論選擇加入狀態為何。

![](../assets/workflow-fork.png)

此模式有助於瞭解管道類別設定如何影響傳送行為，以及在單一行銷活動執行中傳送不同訊息型別給相同對象。
