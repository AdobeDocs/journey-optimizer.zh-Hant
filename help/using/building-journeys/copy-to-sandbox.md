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
source-git-commit: 28a4f04ebcda27213d3bac763fb9bea8ea4a0146
workflow-type: tm+mt
source-wordcount: '835'
ht-degree: 20%

---

# 將歷程複製到另一個沙箱 {#copy-to-sandbox}

>[!CONTEXTUALHELP]
>id="ajo_journey_copy_main"
>title="將歷程複製到另一個沙箱"
>abstract="Journey Optimizer 可讓您將整個歷程從一個沙箱複製到另一個沙箱。例如，您可以將歷程從預備沙箱環境複製到生產沙箱。除了歷程本身外，Journey Optimizer 還會複製歷程所依賴的大部分物件。"

>[!CONTEXTUALHELP]
>id="ajo_journey_copy_sandbox_details"
>title="沙箱詳細資料"
>abstract="選取您要將歷程複製過去的目的地沙箱。只能使用您的組織內的沙箱。"

>[!CONTEXTUALHELP]
>id="ajo_journey_copy_object_details"
>title="物件詳細資料"
>abstract="這是您將要複製的歷程。"

>[!CONTEXTUALHELP]
>id="ajo_journey_copy_dependent_objects"
>title="相依物件"
>abstract="這是歷程中使用的關聯物件清單。此清單會顯示名稱、物件類型以及內部的 Journey Optimizer ID。"

Journey Optimizer 可讓您將整個歷程從一個沙箱複製到另一個沙箱。例如，您可以將歷程從您的中繼沙箱環境複製到生產沙箱。 除了歷程本身，Journey Optimizer也會複製歷程所依賴的大部分物件：對象、表面（即預設集）、結構描述、事件和動作。 有關已複製物件的詳細資訊，請參閱此處 [區段](#limitations).

>[!CAUTION]
>
>我們不保證所有連結的元素都會複製到目的地沙箱。 我們強烈建議您在發佈歷程之前執行徹底檢查。 這可讓您識別任何可能遺失的物件。

目標沙箱中的複製物件是唯一的，沒有覆寫現有元素的風險。 歷程及歷程內的任何訊息都會以草稿模式帶入。 這可讓您在目標沙箱上發佈之前執行徹底驗證。 復製程式只會複製歷程的中繼資料以及該歷程中的物件。 此程式不會複製任何設定檔或資料集資料。

若要將歷程複製到另一個沙箱，請執行以下步驟：

1. 在歷程管理功能表區段中，按一下 **[!UICONTROL 歷程]**. 隨即顯示歷程清單。

2. 搜尋您要複製的歷程，按一下 **更多動作** 圖示（歷程名稱旁的三個點）並按一下 **複製到沙箱**.

   ![](assets/copy-sandbox1.png)

   此 **複製到沙箱** 畫面隨即顯示。

   ![](assets/copy-sandbox2.png)

3. 選取 **Target沙箱** 從下拉式欄位。 只能使用您的組織內的沙箱。

4. 檢閱 **相依物件** 區段。 這是歷程中使用的關聯物件清單。此清單會顯示名稱、物件類型以及內部的 Journey Optimizer ID。

5. 按一下 **複製** 按鈕來開始將歷程複製到目標沙箱。

   ![](assets/copy-sandbox3.png)

   復製程式隨即開始，並顯示每個個別物件的進度。 復製程式會因歷程的複雜度及需要複製多少物件而有所不同。 如果發生錯誤，則會顯示相關物件的訊息。

   ![](assets/copy-sandbox4.png)

6. 複製完成後，請按一下 **關閉**.

7. 存取您的目標沙箱，並對所有複製的物件執行徹底檢查。

## 復製程式與限制 {#limitations}

可能不會將所有連結的元素複製到目的地沙箱。 Adobe強烈建議您執行徹底檢查。 識別任何可能的遺失物件，並在發佈歷程之前手動建立。

會複製下列物件：

* 對象

  對象只能從一個沙箱複製到另一個沙箱。 對象複製後，就無法在目的地沙箱中對其進行編輯。

* 綱要

  將複製此歷程中使用的結構描述。

* 訊息

  歷程中使用的管道動作活動。 訊息中用於個人化的欄位不會檢查完整性。 不會複製內容區塊。

* 歷程 — 畫布詳細資料

  畫布上的歷程表示法，包括歷程中的物件，例如條件、動作、事件、讀取對象等。 跳轉活動會從複製中排除。

* 活動

  將會複製歷程中使用的事件和事件詳細資訊。

* 動作

  將會複製歷程中使用的動作和動作詳細資訊。

不會複製曲面（即預設集）。 系統會根據訊息型別和表面名稱，自動選取目標沙箱上最接近的相符專案。 如果在目標沙箱上找不到表面，則表面複製將會失敗。 這表示訊息復本也會失敗，因為訊息需要可供設定的介面。 在此情況下，需要為訊息的正確通道建立至少一個表面，副本才能運作。

對於結構描述、合併原則和對象，這些物件第二次嘗試複製時，只會被引用。 它們將被視為已經存在的物件，並將再次複製。 這表示這些物件只能複製一次。

Adobe Journey Optimizer會延遲五分鐘，才可參照結構描述、合併原則和對象，而不會在畫布中看到錯誤。 請等候五分鐘，這些參考資料將可供使用。
