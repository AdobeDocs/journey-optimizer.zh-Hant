---
solution: Journey Optimizer
product: journey optimizer
title: 傳送資料至AEP
description: 瞭解如何將資料傳送至AEP
feature: Journeys, Use Cases
topic: Content Management
role: User, Developer
level: Intermediate, Experienced
keywords: 歷程，使用案例
version: Journey Orchestration
feature_v2: []
subfeature_v2: []
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 711
ht-degree: 3%

---

# 使用案例：建立自訂動作以將資料傳送至[!DNL Adobe Experience Platform]{#send-data-to-aep}

>[!BEGINSHADEBOX]

**在此頁面上：**&#x200B;瞭解如何使用設定檔上限條件的最佳化活動，建立逐漸增加電子郵件數量的歷程，以熱身IP並保護您的寄件者信譽。

>[!ENDSHADEBOX]

如果您最近移至其他電子郵件服務提供者、IP位址或電子郵件網域或子網域，請建立您的寄件者信譽。 否則，可能會封鎖傳遞或將其移至收件者的垃圾郵件資料夾。 如需指引，請參閱[傳遞能力最佳實務指南](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/generic-resources/increase-reputation-with-ip-warming.html?lang=zh-Hant){target="_blank"}。

若要熱身IP，您可以逐步增加傳遞數量。 深入瞭解[在Journey Optimizer](../reports/deliverability.md)中最佳化傳遞能力。

此使用案例的目的是建立歷程，以加快電子郵件傳遞速度。 若要設定此歷程，請遵循下列步驟：

1. 建立歷程。 [閱讀全文](journey-gs.md)。

1. 將&#x200B;**[!UICONTROL 最佳化]**&#x200B;活動新增至歷程。 [閱讀全文](optimize.md)。

1. 在&#x200B;**[!UICONTROL 條件]**&#x200B;活動設定中，設定傳遞的收件者數目上限：

   1. 在&#x200B;**[!UICONTROL 最佳化]**&#x200B;活動設定中，選取&#x200B;**[!UICONTROL 條件]**&#x200B;方法，並將&#x200B;**[!UICONTROL 型別]**&#x200B;欄位設定為&#x200B;**[!UICONTROL 設定檔上限]**。 [閱讀全文](conditions.md#profile_cap)。

   1. 將&#x200B;**[!UICONTROL 限制]**&#x200B;欄位設定為此傳遞的收件者數目上限。

   ![控制自訂動作執行磁碟區的設定檔上限條件](assets/profile-cap-condition.png)

   您可以逐漸提高此限制，最多可達您的訂閱者總數。

1. 在&#x200B;**[!UICONTROL 條件]**&#x200B;活動之後，將&#x200B;**[!UICONTROL 電子郵件]**&#x200B;動作活動新增至名義路徑。

   ![傳送資料至外部系統的自訂動作歷程](assets/ramp-up-deliveries-message.png)

   當歷程執行時，會傳送訊息給輸入的設定檔，最多為您指定的設定檔數量上限。 當達到此限制時，輸入的設定檔會採用替代路徑。

1. 使用您選擇的活動完成歷程。

IP啟動後，您就可以移除此條件。

+++ AI知識參考

本節包含結構化知識，用於支援與本主題相關的解譯、擷取和問答。

如需完整瞭解，此資訊應結合本頁的檔案。 兩者皆非獨立來源；頁面說明功能，本節提供額外內容，以協助去除術語、意圖、適用性和限制條件的歧義。

* **TL；DR：**&#x200B;此頁面會逐步說明歷程式IP暖身使用案例，使用設定檔上限條件來增加電子郵件傳遞量，以保護寄件者信譽。

**意圖：**

* 建立IP預熱歷程，以逐步增加電子郵件傳送量
* 設定設定檔上限條件，以限制每次傳遞的收件者人數
* 將電子郵件動作活動新增至名義歷程路徑
* IP預熱完成後，移除設定檔上限條件

**字彙表：**

* **IP預熱**：從新IP位址逐漸增加電子郵件傳送量的程式，以建立寄件者信譽&#x200B;*（產品特定）*
* **設定檔上限**： Journey Optimizer中的條件型別，可限制採用特定歷程路徑&#x200B;*（產品特定）*&#x200B;的設定檔數目上限
* **名義路徑**：設定檔在符合條件時所遵循歷程的主要分支&#x200B;*（產品專屬）*

**護欄：**

* 設定檔上限條件必須在「條件」活動上設定，才能在IP預熱期間控制傳送量。
* 超過上限的輪廓會繞線至替代路徑。
* 必須在IP預熱完成後重新建立或修改歷程，以移除上限條件。

**術語：**

* 正式名稱：IP warming — 縮寫：n/a — 變體：IP熱身、寄件者信譽熱身
* 同義字：「設定檔上限」=「收件者限制條件」
* 請勿混淆：「IP預設」≠「電子郵件驗證」（SPF/DKIM/DMARC設定不同）

**常見問題集：**

* **問：為什麼我需要熱身IP？**  — 新的IP位址沒有傳送記錄，因此在建立信譽之前，信箱提供者可能會封鎖或垃圾郵件資料夾訊息。
* **問：超過設定檔上限的設定檔會發生什麼事？**  — 它們採用「條件」活動中定義的替代路徑。
* **問：如何隨著時間增加上限？**  — 編輯[條件]活動設定中的[限制]欄位，並逐漸將其提高到您的訂閱者總數。
* **問：何時可以移除設定檔上限條件？**  — 當您的IP具有足夠的傳送歷史記錄和可傳遞性量度穩定後，您就可以從歷程中移除條件。

+++
