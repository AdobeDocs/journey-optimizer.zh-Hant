---
solution: Journey Optimizer
product: journey optimizer
title: 在沙箱之間複製Journey Optimizer物件
description: 瞭解如何在沙箱之間複製歷程、內容範本和片段。
feature: Journeys, Sandboxes
topic: Content Management
role: User, Developer, Data Engineer
level: Experienced
keywords: 沙箱，歷程，複製，環境
source-git-commit: 62b5cfd480414c898ab6f123de8c6b9f99667b7d
workflow-type: tm+mt
source-wordcount: '1074'
ht-degree: 4%

---


# 將Journey Optimizer物件複製到另一個沙箱 {#copy-to-sandbox}

沙箱工具可讓您運用套件匯出和匯入，跨多個沙箱複製物件，例如歷程、內容範本或片段。 套件可以包含單一物件或多個物件。 套件中包含的任何物件都必須來自相同沙箱。

本頁說明Journey Optimizer內容中的沙箱工具使用案例。 如需功能本身的詳細資訊，請參閱[Experience Platform檔案](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/sandbox-tooling.html)。

>[!NOTE]
>
>此功能需要&#x200B;**沙箱管理**&#x200B;功能的下列許可權：管理沙箱（或檢視沙箱）和管理套件。 [了解更多](../administration/ootb-permissions.md)

復製程式會透過來源沙箱和目標沙箱之間的套件匯出和匯入進行。 以下是從一個沙箱複製歷程到另一個沙箱的一般步驟：

1. 在來源沙箱中新增要匯出為封裝的物件。
1. 將套件匯出至目標沙箱。

此外，您可以運用Journey Optimizer **物件復制服務REST API**&#x200B;來管理沙箱的物件。 [瞭解如何使用物件復制服務REST API](https://developer.adobe.com/journey-optimizer-apis/references/sandbox/)

## 匯出的物件與最佳實務 {#objects}

Journey Optimizer可將歷程、內容範本和片段匯出至另一個沙箱。 以下各節提供每種物件型別的資訊和最佳實務。

### 一般最佳實務 {#global}

* 複製物件時，父物件中的任何相依性（例如巢狀片段、歷程對象或動作）都會正確更新，以確保目標沙箱中的對應正確。

* 如果匯出的物件包含設定檔個人化，請確定目標沙箱中存在適當的結構描述，以避免任何個人化問題。

### 歷程 {#journeys}

* 匯出歷程時，除了歷程本身，Journey Optimizer也會複製歷程所依賴的大部分物件：受眾、結構描述、事件和動作。 如需所複製物件的詳細資訊，請參閱此[區段](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/sandbox-tooling.html#abobe-journey-optimizer-objects)。

* 我們不保證所有連結的元素都會複製到目的地沙箱。 我們強烈建議您執行徹底檢查，例如在發佈歷程之前。 這可讓您識別任何可能遺失的物件。

* 目標沙箱中的複製物件是唯一的，沒有覆寫現有元素的風險。 歷程及歷程內的任何訊息都會以草稿模式帶入。 這可讓您在目標沙箱上發佈之前執行徹底驗證。

* 復製程式只會複製歷程的中繼資料以及該歷程中的物件。 此程式不會複製任何設定檔或資料集資料。

### 內容範本 {#content-templates}

* 匯出內容範本時，所有巢狀片段也會一併複製。

* 匯出內容範本有時會導致片段重複。 例如，如果兩個範本共用相同的片段並且在不同的套件中複製，則兩個範本都需要在目標沙箱中重複使用相同的片段。 若要避免重複，請在匯入過程中選取「使用現有」選項。 [瞭解如何匯入套件](#import)

* 若要進一步避免重複，建議匯出單一套件中的內容範本。 這可確保系統有效率地管理重複資料刪除。

### 片段 {#fragments}

* 片段可以有多個狀態，例如即時、草稿和即時草稿。 匯出片段時，其最新的草稿狀態會複製到目標沙箱。

* 匯出片段時，也會一併複製所有巢狀片段。

## 將物件新增為封裝{#export}

若要將物件複製到另一個沙箱，您首先需要將其新增為來源沙箱中的套件。 請依照下列步驟操作：

1. 導覽至儲存第一個要複製之物件的詳細目錄，例如歷程清單。 按一下&#x200B;**更多動作**&#x200B;圖示（物件名稱旁邊的三個點），然後按一下&#x200B;**新增到封裝**。

   ![](assets/journey-sandbox1.png)

1. 在&#x200B;**新增至封裝**&#x200B;視窗中，選擇您要將物件新增至現有的封裝，還是要建立新的封裝：

   ![](assets/journey-sandbox2.png)

   * **現有的封裝**：從下拉式功能表中選取封裝。
   * **建立新封裝**：輸入封裝名稱。 您也可以新增說明。

1. 重複這些步驟，以新增所有要與封裝一起匯出的物件。

>[!NOTE]
>
>除了歷程本身外，對於歷程匯出，Journey Optimizer也會複製歷程所依賴的大部分物件：對象、結構描述、事件和動作。 如需歷程匯出的詳細資訊，請參閱[本節](../building-journeys/copy-to-sandbox.md)。

## Publish要匯出的套件 {#publish}

準備好要匯出套件後，請依照下列步驟進行發佈：

1. 瀏覽至&#x200B;**[!UICONTROL 管理]** > **[!UICONTROL 沙箱]**&#x200B;功能表，選取&#x200B;**套件**&#x200B;標籤。

1. 開啟您要匯出的套件，選取您要匯出的物件，然後按一下&#x200B;**Publish**。

   在此範例中，我們要匯出歷程、內容範本和片段。

   ![](assets/journey-sandbox4.png)

1. 若要從&#x200B;**[!UICONTROL 工作]**&#x200B;索引標籤追蹤封裝發行集的狀態。 如需工作的詳細資訊，請從清單中選取該工作，然後按一下&#x200B;**[!UICONTROL 檢視匯入詳細資料]**&#x200B;按鈕。

   ![](assets/journey-sandbox9.png)

## 將套件匯入目標沙箱中 {#import}

發佈套件後，您需要將它匯入目標沙箱。 請依照下列步驟操作：

1. 瀏覽至&#x200B;**[!UICONTROL 沙箱]**&#x200B;功能表，並選取&#x200B;**[!UICONTROL 瀏覽]**&#x200B;標籤。

1. 搜尋您要匯入封裝的沙箱，然後按一下其名稱旁的+圖示。

   ![](assets/journey-sandbox5.png)

   >[!NOTE]
   >
   >只能使用您的組織內的沙箱。

1. 在&#x200B;**目標沙箱**&#x200B;欄位中，檢查是否已選取正確的目標沙箱，並從&#x200B;**[!UICONTROL 封裝名稱]**&#x200B;下拉式清單中選取要匯入的封裝。 按一下&#x200B;**下一步**。

   ![](assets/journey-sandbox6.png)

1. 檢閱套裝程式物件與相依性。 這是已新增至封裝的物件清單，以及其他物件歷程，視受眾、結構描述、事件或動作而定。

   對於每個物件，您可以選擇建立新物件或使用目標沙箱中的現有物件。 舉例來說，這可讓您避免使用通用片段匯入內容範本時可能會發生的片段重複。

   ![](assets/journey-sandbox7.png)

1. 按一下右上角的&#x200B;**完成**&#x200B;按鈕，開始將封裝複製到目標沙箱。 復製程式會因物件的複雜性以及需要複製多少物件而有所不同。

1. 按一下匯入工作以複查複製結果：

   * 按一下&#x200B;**檢視匯入的物件**&#x200B;按鈕，以顯示每個已複製的個別物件。
   * 按一下&#x200B;**檢視匯入詳細資料**&#x200B;按鈕，檢查每個物件的匯入結果。

   ![](assets/journey-sandbox8.png)

1. 存取您的目標沙箱，並對所有複製的物件執行徹底檢查。