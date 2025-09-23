---
solution: Journey Optimizer
product: journey optimizer
title: 開始使用結構描述
description: 了解如何在 Adobe Journey Optimizer 使用 Adobe Experience Platform 結構描述
feature: Data Model, Datasets, Data Management
role: Data Engineer, Data Architect, Admin
level: Experienced
keywords: 結構描述、平台、資料、結構
exl-id: c2a8df2e-ff94-4f9a-a53e-bbf9f663cc81
source-git-commit: c584ce48029bd298b503a342a1e663eeeedbba42
workflow-type: tm+mt
source-wordcount: '394'
ht-degree: 81%

---

# 開始使用結構描述 {#schemas-gs}

[!DNL Adobe Journey Optimizer] 仰賴 **Adobe Experience Platform 結構描述**，以一致且可重複使用的方式描述資料結構。結構描述會提供真實物件 (例如個人) 等抽象定義，還會概述應加入物件的每個執行個體的資料 (例如名字、生日等)。將資料擷取至 Experience Platform 時，其結構一律符合 **XDM 結構描述**。

## 標準和以模型為基礎的結構描述

Adobe Experience Platform 中有兩種結構描述：

* **標準結構描述**&#x200B;是使用類別和欄位群組來擷取記錄或時間序列資料的階層式結構描述

  標準結構描述包括：

   * **類別** (定義資料行為：記錄或時間序列)。
   * 一或多個&#x200B;**欄位群組** (會將特定欄位新增至結構描述)。

  在 Journey Optimizer 中，標準結構描述通常用於表示&#x200B;**個人使用者及其屬性**、擷取&#x200B;**時間序列互動** (例如點選、購買或登入)，以及支援&#x200B;**即時客戶輪廓**&#x200B;以進行細分和個人化。

  ➡️ [觀看這段影片，了解如何建立和設定標準結構描述](#video-schema) (影片)

* **以模型為基礎的結構描述**&#x200B;是不使用類別或欄位群組的平面、非階層式結構描述。 它們用於擷取關聯式實體的記錄資料，主要用於[!DNL Journey Optimizer]&#x200B;**協調行銷活動**。

  關聯式實體的範例包括：
   * 預訂、合約或訂閱
   * 產品或目錄
   * 商店、地點或合作夥伴

  使用以模型為基礎的結構描述時，您可以為每個實體傳送訊息（例如，每個預訂、每個訂閱）、根據實體屬性（例如，產品類別、商店位置）建立區段，並透過聯絡連結至實體的所有聯絡人來改善定址能力。

  以模型為基礎的結構描述如何運作：

   1. **手動建立結構描述或透過 DDL 匯入**
   1. **連結結構描述**&#x200B;以定義實體和人員之間的關係 (例如，連結至成員的忠誠度交易、連結至品牌的獎勵)。
   1. 從支援的來源&#x200B;**將資料擷取到**&#x200B;您的資料集中。

  ➡️ [瞭解如何管理以模型為基礎的結構描述和資料集](../orchestrated/gs-schemas.md)
➡️ [開始使用協調的行銷活動](../orchestrated/gs-schemas.md)

## 作法影片{#video-schema}

了解如何建立標準結構描述、新增欄位群組、建立及設定自訂欄位群組。

>[!VIDEO](https://video.tv.adobe.com/v/334461?quality=12)

>[!MORELIKETHIS]
>
>* [建立結構描述、資料集及擷取資料，即可在 Journey Optimizer 新增測試輪廓](../audience/creating-test-profiles.md)
>* [XDM 系統概觀](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hant){target="_blank"}
>* [資料模式的最佳做法](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/best-practices.html?lang=zh-Hant){target="_blank"}
>* [使用結構描述登錄 API，建立結構描述](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-api.html?lang=zh-Hant){target="_blank"}
>* [使用結構描述編輯器，定義兩種結構描述之間的關係](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/relationship-ui.html?lang=zh-Hant){target="_blank"}
