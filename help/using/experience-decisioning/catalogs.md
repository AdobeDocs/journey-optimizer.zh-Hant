---
title: 專案目錄
description: 瞭解如何使用專案目錄
feature: Offers
topic: Integrations
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta"
exl-id: 2d118f5a-32ee-407c-9513-fe0ebe3ce8f0
source-git-commit: c4ab97999d000d969f6f09f4d84be017d1288f94
workflow-type: tm+mt
source-wordcount: '320'
ht-degree: 6%

---

# 專案目錄 {#catalog}

>[!BEGINSHADEBOX]

本文件指南會提供以下內容：

* [開始使用體驗決策](gs-experience-decisioning.md)
* 管理您的決定專案
   * **[設定專案目錄](catalogs.md)**
   * [建立決定專案](items.md)
   * [管理專案集合](collections.md)
* 設定專案的選取範圍
   * [建立決定規則](rules.md)
   * [建立排名方法](ranking.md)
* [建立選取策略](selection-strategies.md)
* [建立決定原則](create-decision.md)

>[!ENDSHADEBOX]

在Experience Decisioning中，目錄可作為中央容器來組織決策專案。 每個目錄都會連結至Adobe Experience Platform結構描述，包含可指派給決定專案的所有屬性。

目前，所有已建立的決定專案都已整合至單一「優惠」目錄中，並可透過以下方式存取： **[!UICONTROL 專案]** 功能表。

![](assets/catalogs-list.png)

若要存取儲存決定專案屬性的目錄結構，請執行下列步驟：

1. 從專案清單中，按一下 **[!UICONTROL 編輯結構描述]** 按鈕位於旁邊 **[!UICONTROL 建立專案]** 按鈕。

1. 目錄的結構會在新標籤中開啟，遵循以下結構：

   * 此 **`_experience`** 節點包含標準決定專案屬性，例如名稱、開始和結束日期以及說明。
   * 此 **`_<imsOrg>`** 節點會存放自訂決策專案屬性。 預設不會設定自訂屬性，但您可以視需要新增更多屬性以符合您的需求。 完成後，自訂屬性會與標準屬性一起出現在決定專案建立畫面中。

   ![](assets/catalogs-schema.png)

1. 若要將自訂屬性新增至結構描述，請展開 **`_<imsOrg>`** 節點，然後按一下結構中所需位置的「+」按鈕。

   ![](assets/catalogs-add.png)

1. 填寫新增屬性的必要欄位，然後按一下 **[!UICONTROL 套用]**.

   >[!CAUTION]
   >
   >目前，Experience Decisioning僅支援下列資料型別。 建立決定專案時，無法使用落在這些資料型別之外的任何欄位。
   >* 字串
   >* 布林值
   >* 數字

   有關如何使用Adobe Experience Platform綱要的詳細資訊，請參閱 [XDM系統檔案](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/overview.html?lang=zh-Hant).

1. 新增您所需的自訂屬性後，請儲存結構。 新欄位現在可在專案決定建立畫面的 **[!UICONTROL 自訂屬性]** 區段。
