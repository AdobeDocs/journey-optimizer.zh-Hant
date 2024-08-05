---
title: 開始使用體驗決策
description: 深入了解體驗決策
feature: Experience Decisioning
topic: Integrations
role: User
level: Intermediate
badge: label="有限可用性"
exl-id: 4c57dbf9-b2a4-42da-8aa3-5a1b3a475a32
source-git-commit: 1d8ea66425b21ec831542bb36bb283c23760e94f
workflow-type: tm+mt
source-wordcount: '420'
ht-degree: 32%

---

# 開始使用體驗決策 {#get-started-experience-decisioning}

>[!AVAILABILITY]
>
>體驗決策目前僅可適用於一組組織 (可用性限制)。 若要取得存取權，請和您的 Adobe 代表聯絡。
>
>目前，已購買 Adobe Systems **Healthcare Shield** 和 **Privacy and Security Shield** 附加產品的客戶無法使用該功能。

## 什麼是體驗決策 {#about}

體驗決策透過提供稱為「決策項目」的集中行銷優惠目錄與複雜的決策引擎來簡化個人化。 此引擎運用規則與排名標準來選取並呈現最相關的決定項目給每個人。

這些決策項通過新的基於代碼的體驗 通道](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/code-based-experience/get-started-code-based)無縫[集成到各種入站介面中，現在可以在 Journey Optimizer 廣告系列中訪問。Experience Decisioning 決策原則僅可用於程式碼型的體驗活動。

## 體驗決策的關鍵步驟 {#steps}

使用體驗決策的主要步驟如下：

1. **分配適當的許可權**。 體驗決策僅適用於有權訪問體驗決策相關 **[!UICONTROL 角色]** 的使用者，例如決策管理員。 如果您無法訪問 Experience Decisioning，則必須擴展您的許可權。

   +++瞭解如何分配決策管理器角色

   1. 若要將角色分配給產品中的 [!DNL Permissions] 用戶，請導航到 **[!UICONTROL 角色]** 標籤 並選擇 決策經理。

      ![](assets/decision_permission_1.png)

   1. 在&#x200B;**[!UICONTROL 使用者]**&#x200B;標籤中，按一下&#x200B;**[!UICONTROL 新增使用者]**。

      ![](assets/decision_permission_2.png)

   1. 輸入您的使用者名稱或電子郵件地址，或從清單中選擇使用者，然後按一下&#x200B;**[!UICONTROL 儲存]**。

      如果之前未建立使用者，請參閱[新增使用者文件](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/access-control/ui/users)。

      ![](assets/decision_permission_3.png)

   接著，使用者應會收到一封電子郵件，並重新導向至您的執行個體。

+++

1. **配置自定義屬性**：通過將自定義屬性設置為目錄綱要，根據您的特定要求定製物料目錄。

1. **建立決策項目** 以顯示給目標對象。

1. **使用集合**&#x200B;進行組織：使用集合根據基於屬性的規則對決策項進行分類。 將集合合併到您的選擇策略中，以確定應考慮哪些集合決策項。

1. **建立決策規則**：決策規則用於決策項和/或選擇策略，以確定可以向誰顯示決策項。

1. **實現排名方法**：建立 排名方法並將其應用於決策策略中，以確定選擇決策項的優先順序順序。

1. **建立選擇策略**：構建選擇策略，善用集合、決策規則和排名方法，以確定適合向配置文件顯示的決策項。

1. **將決策原則嵌入到基於代碼的行銷活動**&#x200B;中：決策策略結合了多種選擇策略，以確定要向目標對象顯示的合格決策項。
