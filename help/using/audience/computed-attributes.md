---
solution: Journey Optimizer
product: journey optimizer
title: 使用計算屬性
description: 瞭解如何使用計算屬性。
feature: Audiences, Profiles
role: User
level: Intermediate
exl-id: 5402a179-263f-46a7-bddf-5b7017cf0f82
source-git-commit: d87f33c80cc85b1d1a87150687f6d7c9a268a016
workflow-type: tm+mt
source-wordcount: '508'
ht-degree: 1%

---

# 使用計算屬性 {#computed-attributes}

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

規則準備就緒後，請發佈計算屬性以供其他下游服務(包括Journey Optimizer)使用。

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
