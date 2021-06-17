---
title: 關於歷程事件的ExperienceEvent結構
description: 了解歷程事件的ExperienceEvent結構
feature: 結構描述
topic: 管理
role: Administrator
level: Intermediate
source-git-commit: 8f77802fcaa23790f9de4e8f15e593643b13fb1e
workflow-type: tm+mt
source-wordcount: '320'
ht-degree: 1%

---

# 關於[!DNL Journey Optimizer]事件的ExperienceEvent結構

[!DNL Journey Optimizer] 事件是透過串流獲取傳送至Adobe Experience Platform的XDM體驗事件。

因此，為[!DNL Journey Optimizer]設定事件的重要先決條件是您熟悉Adobe Experience Platform的體驗資料模型（或XDM）、如何組成XDM體驗事件結構，以及如何將XDM格式化資料串流至Adobe Experience Platform。

## [!DNL Journey Optimizer]事件的架構需求

為[!DNL Journey Optimizer]設定事件的第一步，是確保您已定義XDM架構來代表事件，並建立資料集來記錄Adobe Experience Platform上的事件例項。 雖然不一定需要為事件建立資料集，但將事件傳送至特定資料集可讓您維護使用者的事件歷史記錄，以供日後參考和分析，因此這始終是個好主意。 如果您尚未擁有適合事件的結構和資料集，這兩項工作都可在Adobe Experience Platform網頁介面中完成。

![](../assets/schema1.png)

將用於[!DNL Journey Optimizer]事件的任何XDM架構都應符合下列需求：

* 結構必須為XDM ExperienceEvent類別。

   ![](../assets/schema2.png)

* 對於系統產生的事件，結構必須包含Orchestration eventID欄位群組。 [!DNL Journey Optimizer] 使用此欄位來識別歷程中使用的事件。

   ![](../assets/schema3.png)

* 宣告身分欄位，以識別事件的主題。 如果未指定身份，則可以使用身份映射。 不建議採用此做法。

   ![](../assets/schema4.png)

* 如果您希望此資料在稍後的歷程中可供查閱，請為設定檔標籤結構和資料集。

   ![](../assets/schema5.png)

   ![](../assets/schema6.png)

* 歡迎加入資料欄位，以擷取您要與事件一併包含的任何其他內容資料，例如使用者、產生事件的裝置、位置，或與事件相關的任何其他有意義的情況等資訊。

   ![](../assets/schema7.png)

   ![](../assets/schema8.png)
