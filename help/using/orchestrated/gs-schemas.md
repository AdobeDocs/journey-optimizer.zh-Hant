---
solution: Journey Optimizer
product: journey optimizer
title: 設定步驟
description: 瞭解如何透過上傳DDL在Adobe Experience Platform中建立關聯式結構描述
exl-id: 327597f6-8a53-42dc-966a-baae49b58bb3
source-git-commit: 7fc03d15c63789a2c35e3d517ca0c63f93545d4c
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 3%

---


# 開始使用關聯式結構描述和資料集{#gs-schemas}

本指南會逐步引導您建立關聯式結構、設定用於協調行銷活動的資料集及擷取資料的程式。

![](assets/do-not-localize/schema_admin.png)

1. 使用DDL檔案[手動建立](manual-schema.md)關聯式結構描述[或](file-upload-schema.md)

   定義資料模型的結構，包括表格、屬性和關係。 選擇在使用者介面中手動建置綱要，或上傳DDL檔案以加快設定。

   手動建立結構時，也必須手動建立及啟用資料集。 使用DDL檔案時，資料集的建立和啟用是自動的。

1. [連結結構描述](file-upload-schema.md)

   在您的結構描述之間建立關係，以確保資料一致性並啟用跨實體查詢。 例如，將熟客方案交易連結至收件者，或將獎勵連結至品牌。

1. [擷取資料](ingest-data.md)

   將資料從支援的來源（例如SFTP、雲端儲存空間或資料庫）匯入Adobe Experience Platform。

