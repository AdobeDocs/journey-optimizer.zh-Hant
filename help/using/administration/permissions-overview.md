---
solution: Journey Optimizer
product: journey optimizer
title: 使用者管理概觀
description: 瞭解如何定義和管理許可權
feature: Access Management
topic: Administration
role: Admin, Architect
level: Intermediate
keywords: 許可權，許可權，限制，存取，沙箱
exl-id: b8e266b1-d8eb-4c77-9341-9761b82609b0
source-git-commit: 0ec43a204f5fcf0bddf38cfd381f0ea496c7de70
workflow-type: tm+mt
source-wordcount: '436'
ht-degree: 8%

---

# 開始使用存取控制 {#permissions-overview}

[!DNL Journey Optimizer]可讓您定義並管理指派給不同使用者的許可權。 許可權是授權或拒絕存取產品內功能的一組許可權和限制。

透過Adobe Experience Cloud中的[!DNL Journey Optimizer]許可權&#x200B;**提供**&#x200B;的存取控制。 此功能利用角色和原則，將使用者與許可權和沙箱連結。

若要設定Journey Optimizer的存取控制，您必須擁有組織的系統或產品管理員許可權。 可授予或撤銷許可權的最低角色為產品管理員。 可以管理許可權的其他管理員角色是系統管理員（無限制）。 如需詳細資訊，請參閱有關管理角色的[Adobe說明中心文章](https://helpx.adobe.com/tw/enterprise/using/admin-roles.html){target="_blank"}。

<!-- A high-level workflow for gaining and assigning access permissions can be summarized as follows:

* After licensing [!DNL Journey Optimizer], an email is sent to the administrator specified during licensing.
* The administrator logs in to Adobe Admin Console and selects [!DNL Journey Optimizer] from the list of products on the overview page.
* To grant access to [!DNL Journey Optimizer], it is recommended that the administrator add users to the default product profile
* In Experience Platform Permissions, the administrator can create new roles or edit the permissions and users for any existing roles.
* When creating or editing a role, the administrator adds users to the role using the users tab, and grants permissions to these users (such as "Read Datasets" or "Manage Schemas") by editing the role's permissions. Similarly, the administrator can assign access to sandboxes using the same editing option.
* When users log in to the Journey Optimizer user interface, their access to capabilities is driven by the permissions that have been granted to them from the previous step. For example, if a user does not have the View Datasets permission, the Datasets tab in the side menu will not be visible to that user.-->


[!DNL Journey Optimizer]中的使用者管理是以這些重要概念為基礎：

* **[!UICONTROL 角色]**：角色是指共用相同許可權和沙箱的使用者集合。 這些角色可讓您輕鬆管理組織內不同使用者群組的存取和許可權。 角色具有一組統一許可權（許可權），可讓使用者存取介面中的特定功能或物件。
透過[!DNL Journey Optimizer]，您可以從預先存在的&#x200B;**[!UICONTROL 角色]**&#x200B;範圍中進行選擇，每個角色都有不同的許可權層級，以指派給您的使用者。 深入瞭解&#x200B;**此頁面**&#x200B;上可用的[內建角色](ootb-product-profiles.md)。

* **[!UICONTROL 許可權]**：許可權是統一許可權，可讓您定義指派給&#x200B;**[!UICONTROL 角色]**&#x200B;的授權。 每個許可權都集中在資源（例如歷程或優惠）下，代表[!DNL Journey Optimizer]中的不同功能或物件。 在[權限層級](high-low-permissions.md)一節中了解更多 。

  ![](assets/do-not-localize/permissions_2.png)

* **[!UICONTROL 沙箱]**：虛擬沙箱會將執行個體分割成個別的獨立虛擬環境。 沙箱是透過許可權中的角色指派。 深入瞭解[使用沙箱](sandboxes.md)。

* **物件型存取控制**：限制物件存取的標籤。 這個方法能保護敏感的數位資產，避免未經授權的使用者存取，並確保進一步保護個人資料。深入瞭解[物件式存取管理](object-based-access.md)。

* **以屬性為基礎的存取控制**：管理特定團隊或使用者群組資料存取的授權。 以屬性為基礎的存取控制可讓管理員根據屬性控制對特定物件和/或權能的存取。 屬性可以是新增至物件的中繼資料，例如新增至結構欄位或區段的標籤。 管理員定義存取原則，其中包含管理使用者存取許可權的屬性。 深入瞭解[以屬性為基礎的存取管理](attribute-based-access.md)。


## 一起來深入探討

現在您已瞭解&#x200B;**[!DNL Journey Optimizer]**&#x200B;中的存取控制概念，您可以更深入探討這些檔案區段，以開始設定許可權。


<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="permissions.md">
<img alt="權限" src="assets/do-not-localize/role.jpg">
</a>
<div>
<a href="permissions.md"><strong>授與存取權</strong></a>
</div>
<p>
</td>
<td>
<a href="ootb-permissions.md">
<img alt="內建權限" src="assets/do-not-localize/select.jpg">
</a>
<div>
<a href="ootb-permissions.md"><strong>內建許可權</strong></a>
</div>
<p>
</td>
<td>
<a href="sandboxes.md">
<img alt="管理沙箱" src="assets/do-not-localize/sandboxes.jpg">
</a>
<div>
<a href="sandboxes.md"><strong>管理沙箱</strong></a>
</div>
<p></td>
<td>
<a href="attribute-based-access.md">
<img alt="屬性型存取控制" src="assets/do-not-localize/data-access.jpeg">
</a>
<div>
<a href="attribute-based-access.md"><strong>以屬性為基礎的存取控制</strong></a>
</div>
<p>
</td>
</tr></table>