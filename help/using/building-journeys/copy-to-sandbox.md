---
title: 將歷程複製至其他非道
description: 了解如何將歷程複製至其他非道
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 8c63f2f2-5cec-4cb2-b3bf-2387eefb5002
source-git-commit: cca94d15da5473aa9890c67af7971f2e745d261e
workflow-type: tm+mt
source-wordcount: '837'
ht-degree: 0%

---

# 將歷程複製至其他沙箱 {#copy-to-sandbox}

>[!CONTEXTUALHELP]
>id="ajo_journey_copy_main"
>title="將歷程複製至其他沙箱"
>abstract="Journey Optimizer可讓您將整個歷程從一個沙箱複製到另一個沙箱。 例如，您可以將歷程從階段沙箱環境複製到生產沙箱。 除了歷程本身，Journey Optimizer也會複製歷程所仰賴的大部分物件。"

>[!CONTEXTUALHELP]
>id="ajo_journey_copy_sandbox_details"
>title="沙箱詳細資料"
>abstract="選取您要將歷程複製到哪個目的地沙箱。 您IMS組織內只有沙箱可供使用。"

>[!CONTEXTUALHELP]
>id="ajo_journey_copy_object_details"
>title="物件詳細資訊"
>abstract="這是您要複製的歷程。"

>[!CONTEXTUALHELP]
>id="ajo_journey_copy_dependent_objects"
>title="相依對象"
>abstract="這是歷程中使用的關聯物件清單。 此清單會顯示名稱、物件類型，以及內部Journey Optimizer ID。"

Journey Optimizer可讓您將整個歷程從一個沙箱複製到另一個沙箱。 例如，您可以將歷程從Stage沙箱環境複製到生產沙箱。 除了歷程本身，Journey Optimizer也會複製歷程所仰賴的大部分物件：區段、曲面（即預設集）、結構、事件和動作。 有關複製對象的詳細資訊，請參閱 [節](../building-journeys/copy-to-sandbox.md#limitations).

>[!CAUTION]
>
>我們不保證所有連結的元素都會複製到目的地沙箱。 強烈建議您先執行徹底檢查，再發佈歷程。 這可讓您識別任何可能遺失的物件。

目標沙箱中複製的物件是唯一的，且不會覆寫現有的元素。 歷程和歷程中的任何訊息都會以草稿模式帶入。 這可讓您在目標沙箱上發佈之前，先執行徹底驗證。 復製程式只會複製歷程的中繼資料以及該歷程中的物件。 此程式不會複製任何設定檔或資料集資料。

若要將歷程複製到另一個沙箱，請依照下列步驟操作：

1. 在「歷程管理」功能表區段中，按一下 **[!UICONTROL 歷程]**. 歷程清單隨即顯示。

2. 搜尋您要複製的歷程，按一下 **更多動作** 圖示（歷程名稱旁的三個點），然後按一下 **複製至沙箱**.

   ![](assets/copy-sandbox1.png)

   此 **複製至沙箱** 畫面。

   ![](assets/copy-sandbox2.png)

3. 選取 **目標沙箱** 從下拉式欄位。 您IMS組織內只有沙箱可供使用。

4. 檢閱 **相依對象** 區段。 這是歷程中使用的關聯物件清單。 此清單會顯示名稱、物件類型，以及內部Journey Optimizer ID。

5. 按一下 **複製** 按鈕，以開始將歷程複製到target沙箱。

   ![](assets/copy-sandbox3.png)

   複製過程開始，並顯示每個對象的進度。 復製程式會依歷程的複雜性以及需要複製的物件數量而有所不同。 如果遇到錯誤，則會顯示相關對象的消息。

   ![](assets/copy-sandbox4.png)

6. 複製完成後，按一下 **關閉**.

7. 存取您的目標沙箱，並對所有複製的物件執行徹底檢查。

## 複製流程和限制 {#limitations}

我們不保證所有連結的元素都會複製到目的地沙箱。 強烈建議您執行徹底檢查。 找出任何可能遺失的物件，並在發佈歷程前手動建立。

會複製下列物件：

* 區段

   一個區段只能從一個沙箱複製到另一個沙箱。 複製區段後，就無法在目的地沙箱上編輯。

* 方案

   系統會複製此歷程中使用的結構。

* 訊息

   歷程中使用的管道動作活動。 系統不會檢查訊息中用於個人化的欄位是否完整。 不會複製內容區塊。

* 歷程 — 畫布詳細資料

   畫布上歷程的表示，包括歷程中的物件，例如條件、動作、事件、讀取區段等。 從復本中排除跳轉活動。

* 活動

   系統會複製歷程中使用的事件和事件詳細資料。

* 動作

   系統會複製歷程中使用的動作和動作詳細資料。

不會複製曲面（即預設集）。 系統會根據訊息類型和表面名稱，自動選取目的地沙箱上最接近的可能相符項目。 如果目標沙箱上沒有找到曲面，則曲面複製將失敗。 這表示訊息復本也會失敗，因為訊息需要有可供設定的表面。 在這種情況下，至少需要建立一個面，以便為消息的正確通道建立，以便複製工作。

對於方案、合併策略和段，第二次嘗試複製這些對象時，將只引用它們。 它們將被視為已存在的對象，並將被再次複製。 這表示這些物件只能複製一次。

Adobe Journey Optimizer必須等上五分鐘，才能參考結構、合併原則和區段，而不會在畫布中看到錯誤。 等待5分鐘，即可使用這些參考。
