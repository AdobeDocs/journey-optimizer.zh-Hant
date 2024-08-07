---
solution: Journey Optimizer
product: journey optimizer
title: 將歷程複製到另一個沙箱
description: 瞭解如何將歷程複製到另一個沙箱
feature: Journeys, Sandboxes
topic: Content Management
role: User, Developer, Data Engineer
level: Experienced
keywords: 沙箱，歷程，複製，環境
exl-id: 8c63f2f2-5cec-4cb2-b3bf-2387eefb5002
source-git-commit: b7c31db7a126eb134c353e26c9e263a9bd1674a6
workflow-type: tm+mt
source-wordcount: '743'
ht-degree: 9%

---

# 將歷程複製到另一個沙箱 {#copy-to-sandbox}

<!--
>[!CONTEXTUALHELP]
>id="ajo_journey_copy_main"
>title="Copy a journey to another sandbox"
>abstract="Journey Optimizer allows you to copy an entire journey from one sandbox to another. For example, you can copy a journey from the Stage sandbox environment to your Production sandbox. In addition to the Journey itself, Journey Optimizer also copies most of the objects the journey depends on."

>[!CONTEXTUALHELP]
>id="ajo_journey_copy_sandbox_details"
>title="Sandbox details"
>abstract="Select the destination sandbox you want to copy the journey to. Only sandboxes within your organization are available."

>[!CONTEXTUALHELP]
>id="ajo_journey_copy_object_details"
>title="Object details"
>abstract="This is the journey you are going to copy."

>[!CONTEXTUALHELP]
>id="ajo_journey_copy_dependent_objects"
>title="Dependent objects"
>abstract="This is the list of associated objects used in the journey. This list displays the name, the object type, as well as the internal Journey Optimizer ID."
-->

沙箱工具可讓您運用套件匯出和匯入，跨多個沙箱複製物件。 套件可以包含單一物件或多個物件。 套件中包含的任何物件都必須來自相同沙箱。

本頁說明Journey Optimizer內容中的沙箱工具使用案例。 如需功能本身的詳細資訊，請參閱[Experience Platform檔案](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/sandbox-tooling.html)。

>[!NOTE]
>
>此功能需要&#x200B;**沙箱管理**&#x200B;功能的下列許可權：管理沙箱（或檢視沙箱）和管理套件。 [了解更多](../administration/ootb-permissions.md)

## 開始使用沙箱工具{#sandbox-gs}

Journey Optimizer 可讓您將整個歷程從一個沙箱複製到另一個沙箱。例如，您可以將歷程從您的中繼沙箱環境複製到生產沙箱。 除了歷程本身，Journey Optimizer也會複製歷程所依賴的大部分物件：受眾、結構描述、事件和動作。 如需所複製物件的詳細資訊，請參閱此[區段](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/sandbox-tooling.html#abobe-journey-optimizer-objects)。

>[!CAUTION]
>
>我們不保證所有連結的元素都會複製到目的地沙箱。 我們強烈建議您在發佈歷程之前執行徹底檢查。 這可讓您識別任何可能遺失的物件。

目標沙箱中的複製物件是唯一的，沒有覆寫現有元素的風險。 歷程及歷程內的任何訊息都會以草稿模式帶入。 這可讓您在目標沙箱上發佈之前執行徹底驗證。 復製程式只會複製歷程的中繼資料以及該歷程中的物件。 此程式不會複製任何設定檔或資料集資料。

復製程式會透過來源沙箱和目標沙箱之間的套件匯出和匯入進行。 以下是從一個沙箱複製歷程到另一個沙箱的一般步驟：

1. 將歷程新增為來源沙箱中的套件。
1. 將套件匯出至目標沙箱。

此外，您可以運用Journey Optimizer **物件復制服務REST API**&#x200B;來管理沙箱的物件。 [瞭解如何使用物件復制服務REST API](https://developer.adobe.com/journey-optimizer-apis/references/sandbox/)

## 將歷程新增為封裝{#export}

若要將歷程複製到另一個沙箱，您首先需要將該歷程作為套件新增到來源沙箱中。 請依照下列步驟操作：

1. 在「歷程管理」功能表區段中，按一下&#x200B;**[!UICONTROL 歷程]**。 隨即顯示歷程清單。

1. 搜尋您要複製的歷程，按一下&#x200B;**更多動作**&#x200B;圖示（歷程名稱旁邊的三個點），然後按一下&#x200B;**新增到封裝**。

   ![](assets/journey-sandbox1.png)

   顯示&#x200B;**新增至封裝**&#x200B;視窗。

   ![](assets/journey-sandbox2.png)

1. 選擇您要將歷程新增到現有封裝或建立新封裝：

   * **現有的封裝**：從下拉式功能表中選取封裝。
   * **建立新封裝**：輸入封裝名稱。 您也可以新增說明。

1. 在「管理」功能表區段中，按一下&#x200B;**[!UICONTROL 沙箱]**，選取&#x200B;**套件**&#x200B;標籤，然後按一下您要匯出的套件。

   ![](assets/journey-sandbox3.png)

1. 選取您要匯出的物件，然後按一下&#x200B;**Publish**

   ![](assets/journey-sandbox4.png)

   如果發佈失敗，您可以檢查日誌以識別失敗原因。 開啟套件，按一下&#x200B;**檢視失敗的工作**，選取匯入工作，然後按一下&#x200B;**檢視匯入詳細資料**。

   ![](assets/journey-sandbox9.png)

## 將套件匯出至目標沙箱 {#import}

發佈套件後，您需要將它匯出至目標沙箱。

1. 在來源沙箱中，按一下&#x200B;**[!UICONTROL 沙箱]**&#x200B;功能表，選取&#x200B;**套件**&#x200B;索引標籤，然後按一下您要匯出的套件旁的+圖示。

   ![](assets/journey-sandbox5.png)

1. 從下拉式欄位中選取&#x200B;**Target沙箱**，然後按一下&#x200B;**下一步**。 只能使用您的組織內的沙箱。

   ![](assets/journey-sandbox6.png)

1. 檢閱套裝程式物件與相依性。 這是歷程中使用的關聯物件清單。此清單會顯示名稱和物件型別。 對於每個物件，您可以選擇建立新物件或使用目標沙箱中的現有物件。

   ![](assets/journey-sandbox7.png)

1. 按一下右上角的&#x200B;**完成**&#x200B;按鈕，開始將封裝複製到目標沙箱。 復製程式會因歷程的複雜度及需要複製多少物件而有所不同。

1. 按一下匯入工作以複查複製結果：

   * 按一下「檢視匯入的物件」****&#x200B;以顯示每個複製的物件。
   * 按一下&#x200B;**檢視匯入詳細資料**&#x200B;以檢查每個物件的匯入結果。

   ![](assets/journey-sandbox8.png)

1. 存取您的目標沙箱，並對所有複製的物件執行徹底檢查。
