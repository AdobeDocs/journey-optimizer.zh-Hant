---
title: 開始使用決策
description: 進一步了解決策
feature: Experience Decisioning
topic: Integrations
role: User
level: Intermediate
badge: label="有限可用性"
exl-id: 4c57dbf9-b2a4-42da-8aa3-5a1b3a475a32
source-git-commit: ac8ccb52bd16a26c14dea148f989256e28170765
workflow-type: tm+mt
source-wordcount: '408'
ht-degree: 19%

---

# 開始使用決策 {#get-started-experience-decisioning}

>[!AVAILABILITY]
>
>決策目前僅適用於一組組織（可用性限制）。 若要取得存取權，請和您的 Adobe 代表聯絡。
>
>目前，此功能無法供已購買Adobe **Healthcare Shield**&#x200B;和&#x200B;**Privacy and Security Shield**&#x200B;附加產品的客戶使用。

## 什麼是決策 {#about}

Decisioning透過提供稱為「決策專案」的行銷優惠集中目錄和複雜的決策引擎，簡化了個人化。 此引擎運用規則與排名標準來選取並呈現最相關的決定項目給每個人。

這些決定專案會透過[新的程式碼型體驗管道](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/code-based-experience/get-started-code-based) (現在可在Journey Optimizer促銷活動中存取)，順暢地整合至廣泛的傳入介面。 決策決策政策僅適用於程式碼型體驗行銷活動。


## 決策關鍵步驟 {#steps}

使用決策的主要步驟如下：

1. **指派適當的許可權**。 決策僅適用於具有決策相關&#x200B;**[!UICONTROL 角色]**&#x200B;存取權的使用者，例如決策管理員。 如果您無法存取決策，則必須擴充您的許可權。

   +++瞭解如何指派決策管理員角色

   1. 若要在[!DNL Permissions]產品中將角色指派給使用者，請瀏覽至&#x200B;**[!UICONTROL 角色]**&#x200B;標籤，並選取決策管理員。

      ![](assets/decision_permission_1.png)

   1. 在&#x200B;**[!UICONTROL 使用者]**&#x200B;標籤中，按一下&#x200B;**[!UICONTROL 新增使用者]**。

      ![](assets/decision_permission_2.png)

   1. 輸入您的使用者名稱或電子郵件地址，或從清單中選擇使用者，然後按一下&#x200B;**[!UICONTROL 儲存]**。

      如果之前未建立使用者，請參閱[新增使用者文件](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/access-control/ui/users)。

      ![](assets/decision_permission_3.png)

   接著，使用者應會收到一封電子郵件，並重新導向至您的執行個體。

+++

1. **設定自訂屬性**：將自訂屬性設定到目錄的結構描述中，根據您的特定需求量身打造專案目錄。

1. **建立決策專案**&#x200B;以向您的目標對象顯示。

1. **使用集合組織**：使用集合根據屬性型規則將決定專案分類。 將集合併入您的選擇策略，以決定應考慮的決定專案集合。

1. **建立決定規則**：決定專案和/或選擇策略中會使用決定規則來決定決定可以向誰顯示決定專案。

1. **實作排名方法**：建立排名方法，並在決定策略中套用這些方法，以決定選取決定專案的優先順序。

1. **建立選擇策略**：建置使用集合、決定規則和排名方法的選擇策略，以識別適合顯示給設定檔的決定專案。

1. **將決定原則內嵌至您的程式碼型行銷活動**：決定原則會結合多個選取原則，以決定要顯示給目標對象的合格決定專案。
