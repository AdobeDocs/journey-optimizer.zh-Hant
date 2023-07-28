---
title: 開始使用直接郵件
description: 瞭解如何在Journey Optimizer中建立和直接郵件訊息
feature: Overview
topic: Content Management
role: User
level: Beginner
keywords: 直接郵件、訊息、行銷活動
source-git-commit: a445e418dc11f577c609c16894ce119359f2a261
workflow-type: tm+mt
source-wordcount: '205'
ht-degree: 0%

---

# 開始使用直接郵件 {#create-direct}

>[!AVAILABILITY]
>
>目前，直接郵件通道不適用於已購買AdobeHealthcare Shield附加產品的組織。
>

直接郵件是一種離線頻道，可讓您個人化並產生直接郵件供應商傳送郵件給客戶所需的擷取檔案。

建立直接郵件行銷活動時，Journey Optimizer會自動產生一個檔案，其中包含所有目標設定檔和選取的資料，例如郵寄地址和設定檔屬性。 此檔案會傳送至您選擇的伺服器，以便您選擇的直接郵件提供者存取，該提供者將為您處理實際的郵寄程式。

傳送直接郵件訊息的主要步驟如下：

![](assets/dm-creation-process.png)

直接郵件訊息只能在已排程行銷活動的內容中建立。 它們不可用於API觸發的行銷活動或歷程。

>[!IMPORTANT]
>
>在傳送直接郵件訊息之前，請確定您已設定：
>
>1. A [檔案路由設定](../direct-mail/direct-mail-configuration.md#file-routing-configuration) 會指定應該上傳及儲存解壓縮檔案的伺服器，
>1. A [直接郵件訊息表面](../direct-mail/direct-mail-configuration.md#direct-mail-surface) 會參照檔案路由組態。
