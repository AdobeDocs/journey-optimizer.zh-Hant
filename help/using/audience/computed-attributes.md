---
solution: Journey Optimizer
product: journey optimizer
title: 使用計算屬性
description: 瞭解如何使用計算屬性。
feature: Audiences, Profiles
role: User
level: Intermediate
exl-id: 5402a179-263f-46a7-bddf-5b7017cf0f82
TQID: https://experienceleague.adobe.com/bH8UDdjWsh1Kle1ltVP2ltgXcNJDfVIdTuFdGWSZv6Y
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: baecb07f-ce89-4ebb-9cd9-0f7c053f944f
subfeature_v2: id: f42b4d14-fe8a-428b-b62e-e7995eaab1b3id: b32bb433-f8c6-4931-8e52-e657230a3bf2id: e95b6013-acbe-46e9-a3b5-b80e14088d7d
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: e0eb8757-182f-49f3-94a4-1587d16f5094id: fd2e3797-f2ea-4b36-a9af-52acf5e90513
source-git-commit: a51edc00631334874d111d8350ee7b0eb8e81aa5
workflow-type: tm+mt
source-wordcount: 956
ht-degree: 1%

---

# 使用計算屬性 {#computed-attributes}

>[!BEGINSHADEBOX]

**在此頁面上：**&#x200B;瞭解如何建立計算屬性，將行為事件彙總至設定檔屬性，並在Adobe Journey Optimizer中將其用於分段、個人化和歷程邏輯。

>[!ENDSHADEBOX]

計算屬性將個別行為事件彙總到Adobe Experience Platform上可用的計算設定檔屬性中。 這些屬性以擷取至Adobe Experience Platform的已啟用設定檔體驗事件資料集為基礎，並當做儲存在客戶設定檔中的彙總資料點。

每個運算屬性都是設定檔屬性，可運用於歷程及行銷活動中的細分、個人化和啟動。 這項簡化能增強您為客戶提供及時且有意義的個人化體驗的能力。


![](../rn/assets/do-not-localize/computed-attributes.gif)


>[!NOTE]
>
>若要存取計算屬性，請確定您具有適當的許可權（**檢視計算屬性**&#x200B;和&#x200B;**管理計算屬性**）。

## 建立計算屬性 {#manage}

若要建立計算屬性，請瀏覽至左側的&#x200B;**[!UICONTROL 設定檔]**&#x200B;功能表中的&#x200B;**[!UICONTROL 計算屬性]**&#x200B;索引標籤。

在此畫面中，您可以建置規則來建構計算屬性，這些規則會結合事件屬性、彙總函式以及指定的回顧期間。 例如，您可以計算過去三個月中進行的購買總數、識別上週未購買的設定檔所檢視的最新專案，或統計每個設定檔累積的總獎勵點。

![](assets/computed-attributes.png)

規則準備就緒後，請發佈計算屬性以供其他下游服務（包括Journey Optimizer）使用。

有關建立和管理計算屬性的詳細資訊，請參閱[計算屬性檔案](https://experienceleague.adobe.com/docs/experience-platform/profile/computed-attributes/overview.html?lang=zh-Hant)

## 將計算屬性新增至Adobe Experience Platform資料來源 {#source}

若要在Journey Optimizer中運用計算屬性，請將它們新增至Journey Optimizer **Experience Platform**&#x200B;資料來源。

Adobe Experience Platform資料來源會定義與Adobe即時客戶個人檔案的連線。 此資料來源會從即時客戶個人檔案服務中擷取個人檔案資料和體驗事件資料。

若要將計算屬性新增至資料來源，請遵循下列步驟：

1. 瀏覽至左側的&#x200B;**[!UICONTROL 組態]**&#x200B;功能表，然後按一下&#x200B;**[!UICONTROL 資料來源]**&#x200B;卡片。

1. 選取&#x200B;**[!UICONTROL Experience Platform]**&#x200B;資料來源。

   ![](assets/computed-attributes-add.png)

1. 新增包含所有已建立計算屬性的&#x200B;**[!UICONTROL SystemComputedAttributes]**&#x200B;欄位群組。

   ![](assets/computed-attributes-fieldgroup.png)

計算屬性現在可以在Journey Optimizer中使用。 [瞭解如何在Journey Optimizer中使用運算屬性](#use)

有關新增欄位群組至Adobe Experience Platform資料來源的詳細資訊，請參閱[本節](../datasource/adobe-experience-platform-data-source.md)。

## 在Journey Optimizer中使用計算屬性 {#use}

>[!NOTE]
>
>開始之前，請確定您已將運算屬性新增至Adobe Experience Platform資料來源。 [在本節](#source)中瞭解如何進行。

計算屬性可提供Journey Optimizer中的多用途功能。 將其用於各種目的，例如個人化訊息內容、建立新對象，或根據特定計算屬性分割歷程。 例如，在「條件」活動中新增單一計算屬性，根據設定檔過去三週內的購買總數分割歷程路徑。 您也可以顯示每個設定檔最近檢視的專案，以個人化電子郵件。

由於計算屬性是在您的設定檔聯合結構描述上建立的設定檔屬性欄位，請從&#x200B;**SystemComputedAttributes**&#x200B;欄位群組中的個人化編輯器存取它們。 從那裡，將計算屬性新增到運算式中，將它們視為任何其他設定檔屬性來執行所需的操作。

![](assets/computed-attributes-ajo.png)

+++AI助理 — 頁面內容

- **TL；DR：**&#x200B;瞭解如何在Adobe Experience Platform上建立計算屬性，並在Journey Optimizer中運用這些屬性進行細分、個人化和歷程邏輯。

**意圖：**
- 瞭解什麼是計算屬性，以及它們與標準設定檔屬性的差異
- 結合事件屬性、彙總函式和回顧期間來建立計算屬性
- 將SystemComputedAttributes欄位群組新增至AJO中的Experience Platform資料來源
- 在歷程條件、對象建立和訊息個人化中使用計算屬性

**字彙表：**
- **計算屬性**：從彙總行為事件資料衍生的設定檔屬性，儲存在客戶設定檔&#x200B;*（產品特定）*&#x200B;中
- **回顧期間**：計算計算屬性的彙總規則（例如「過去3個月」）時所套用的時間範圍&#x200B;*（產品特定）*
- **SystemComputedAttributes欄位群組**： Experience Platform資料來源中的欄位群組，會公開所有已發佈的運算屬性，以用於歷程和個人化&#x200B;*（產品特定）*
- **設定檔聯合結構描述**：合併特定身分的所有設定檔片段的合併結構描述，其中儲存計算屬性

**護欄：**
- 需要&#x200B;**檢視計算屬性**&#x200B;和&#x200B;**管理計算屬性**&#x200B;許可權才能存取此功能
- 計算屬性必須先在AEP中&#x200B;**發佈**，才能在Journey Optimizer下游使用
- 計算屬性必須先明確新增至AJO中的&#x200B;**Experience Platform資料來源**，才能用於歷程或個人化
- 運算屬性以擷取至Adobe Experience Platform的設定檔已啟用體驗事件資料集為基礎

**術語：**
- 正式名稱：Adobe Journey Optimizer — 縮寫：AJO — 變體：Journey Optimizer、A-JO
- 正式名稱：Adobe Experience Platform — 首字母縮寫：AEP
- 同義字：「computed attributes」=「computed profile attributes」
- 請勿混淆：「計算屬性」（AEP/AJO專屬彙總功能）≠通用「設定檔屬性」

**常見問題集：**
- **問：什麼是計算屬性？**  — 彙總的行為事件資料（例如購買總計、上次檢視的專案）會儲存在AEP上的設定檔屬性，並可在AJO中使用。
- **問：我需要特殊許可權嗎？**  — 是：「檢視計算屬性」和「管理計算屬性」都是必要的。
- **問：如何在Journey Optimizer中使用運算屬性？**  — 將`SystemComputedAttributes`欄位群組新增至[設定] > [資料來源]下的Experience Platform資料來源。
- **問：我可以在哪裡使用AJO的計算屬性？**  — 在「條件」活動（歷程分割）、建立對象和個人化編輯器中。
- **問：什麼是回顧期間？**  — 用來設定彙總規則範圍的時間範圍，例如「過去3週內的購買總和」。
- **問：我可以在即時歷程中使用運算屬性嗎？**  — 是，發佈並新增至資料來源後，即可像存取任何其他設定檔屬性一樣存取它們。

+++
