---
solution: Journey Optimizer
product: journey optimizer
title: Personalization運算式的AI助理
description: 瞭解如何使用Journey Optimizer中的AI助理從自然語言（從Personalization編輯器或電子郵件Designer工具列）產生個人化運算式。
feature: Content Assistant
topic: Content Management, Artificial Intelligence
role: User
level: Intermediate
mini-toc-levels: 1
source-git-commit: 36d6158d7983f51d1480cc3c8c769159b4c528f2
workflow-type: tm+mt
source-wordcount: '979'
ht-degree: 2%

---

# 個人化運算式的AI助理{#generative-personalization-expressions}

>[!IMPORTANT]
>
>開始使用此功能之前，請先閱讀相關的[護欄與限制](gs-generative.md#generative-guardrails)。
></br>
>
>您必須先同意[使用者合約](https://www.adobe.com/tw/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html)，才能在Journey Optimizer中使用AI小幫手。 如需詳細資訊，請聯絡您的 Adobe 代表。

## 概觀 {#where-available}

[!UICONTROL AI小幫手]可協助您從純文字產生新的個人化、說明現有運算式的功能，並修正選取程式碼中的問題，讓您在語法和手動欄位探索上花費的時間更少。 您也可以重複選取或要求對話中的其他變更。 它有兩種提供方式：

* **[!UICONTROL Personalization編輯器]** — 只要有編輯器可用（主旨行、本文和開啟它的其他欄位）。 如需瞭解在何處以及如何開啟編輯器，請參閱[新增個人化](../personalization/personalization-build-expressions.md#where)。
* **電子郵件Designer** — 當您選取元件時，請使用內容工具列中的&#x200B;**[!UICONTROL 新增運算式]**&#x200B;在工具箱中開啟小幫手。 請參閱[從電子郵件Designer](#generate-email-designer)產生。

如需更廣泛的AI助理設定和語言，請參閱[開始使用AI助理](gs-generative.md)。 如需個人化概念，請參閱[開始使用個人化](../personalization/personalize.md)。 如需提示性的想法，請參閱[AI提示最佳實務](ai-assistant-prompting-guide.md)。

根據您的行銷活動或歷程內容，助理可以處理資料並建構已公開的[!UICONTROL Personalization編輯器] — 例如設定檔屬性、區段成員資格、協助程式功能和相關的個人化來源。

>[!NOTE]
>
>只有當[!UICONTROL AI助理]在該工作階段中保持開啟時，助理才會將內容與您的提示分開。 關閉助理或編輯器會清除交談；下次開啟助理時，您會開始新的交談。

## 產生個人化運算式 {#generate}

這些步驟涵蓋從頭開始產生個人化運算式。 若要使用編輯器中已存在的程式碼，請參閱[編輯、修正或說明現有的程式碼](#edit-existing)。

1. 在您的訊息或內容中，開啟&#x200B;**[!UICONTROL Personalization編輯器]**。

1. 將游標放在您要插入產生的個人化程式碼的編輯器中，然後按一下&#x200B;**[!UICONTROL AI助理]**&#x200B;按鈕。

   ![](assets/ai-perso-access.png)

1. 在文字欄位中，以純文字描述您想要的個人化運算式 — 例如您需要的設定檔屬性、區段或邏輯，然後按一下[產生]。****

   您也可以使用&#x200B;**[!UICONTROL 快速提示]**&#x200B;區段的現成提示，例如個人化問候語、促銷程式碼產生等等。

   ![](assets/ai-perso-generate.png)

   >[!NOTE]
   >
   >任何不相關的提示或問題會傳回範圍外錯誤。 調整您的提示，並詢問有關您需要個人化的相關問題。

1. 您可以與助理在多圈對話中繼續討論：它會保留提示的上下文，以便您可以逐步調整相同的運算式。 若要重新開始，請按一下&#x200B;**[!UICONTROL 新增工作階段]**&#x200B;按鈕。

   ![](assets/ai-perso-question.png)

1. 產生運算式後，按一下&#x200B;**[!UICONTROL 顯示範例設定檔的預覽]**，檢視運算式如何以範例資料評估，並以JSON檢視相關的裝載。 針對此檢查，助理會產生一組有限的合成範例設定檔；這些設定檔不會儲存或儲存在您的組織中。

   如果您需要自訂或其他範例設定檔，請向助理描述您在討論中需要的內容，並在您的提示中加入關鍵字&#x200B;**preview**，以便為您的支票產生正確的預覽設定檔。

   ![](assets/ai-perso-preview-button.png)

   +++預覽範例

   ![](assets/ai-perso-preview.png)

   >[!NOTE]
   >
   >其他預覽則用於特別檢查。 助理將調整為產生約一到五個設定檔，要求非常大的數字可能會導致要求失敗。

   +++

   >[!NOTE]
   >
   >此控制項用於在編輯器中快速檢查您的個人化程式碼，而不是內容的完整訊息預覽。 如需體驗的完整驗證，請使用您慣用的模擬流程。 [瞭解如何預覽和測試您的內容](../content-management/preview-test.md)

1. 若要在您的個人化運算式中實作輸出，請按一下&#x200B;**[!UICONTROL 套用]**。 助理輸出會插入個人化編輯器的游標位置。 若要取代現有的程式碼，請先在編輯器中選取該程式碼，然後使用&#x200B;**[!UICONTROL 使用AI助理編輯]** （請參閱[編輯、修正或說明現有的程式碼](#edit-existing)）。

   您也可以使用![復製圖示](../orchestrated/assets/do-not-localize/activity-copy.svg)圖示，將輸出複製並貼到需要的位置。

## 編輯、修正或說明現有程式碼 {#edit-existing}

您可以選取現有的個人化運算式，並使用AI Assistant來修正個人化問題、說明程式碼的用途，或要求其他變更。

1. 在編輯器中選取現有的個人化程式碼。

1. 在選取專案上按一下滑鼠右鍵，然後選擇&#x200B;**[!UICONTROL 使用AI小幫手編輯]**，以便小幫手使用您的選取專案作為內容。

   ![](assets/ai-perso-right-click.png)

1. **[!UICONTROL AI小幫手]**&#x200B;開啟。 在&#x200B;**[!UICONTROL 快速命令]**&#x200B;中，按一下&#x200B;**[!UICONTROL 說明]**&#x200B;或&#x200B;**[!UICONTROL 修正]**，或使用文字欄位要求其他變更並開始交談。

   ![](assets/ai-perso-edit.png)

1. 當您使用&#x200B;**[!UICONTROL 修正]**&#x200B;時，請按一下討論中的&#x200B;**[!UICONTROL 顯示修正詳細資料]**，以顯示修正的解釋，並在預覽前後逐行顯示。

   ![](assets/ai-perso-fix.png)

1. 當您產生個人化運算式時，請按一下&#x200B;**[!UICONTROL 套用]**&#x200B;以實作助理輸出。 它會取代您在個人化編輯器中選取的程式碼。 例如，如果您要求說明程式碼，套用將在描述其功能的運算式中新增註解。

## 從電子郵件Designer工具列產生 {#generate-email-designer}

在電子郵件Designer中，您可以從內容工具列使用[!UICONTROL AI助理進行個人化運算式]，而不需先開啟完整的[!UICONTROL Personalization編輯器]。

1. 在電子郵件Designer中，選取您要個人化的元件，然後按一下您要插入運算式的位置。

1. 在內容工具列中按一下&#x200B;**[!UICONTROL 新增運算式]**。

   ![](assets/ai-perso-add-expression.png)

1. 會開啟一個工具箱，您可以在其中提示AI助理進行個人化。 輸入您需要的簡單語言，助理會建議設定檔欄位和其他符合提示的屬性，以便您更快建立運算式。

1. 助理會產生運算式。

   ![](assets/ai-perso-add-expression-insert.png)

   您可以：

   * 使用範例值驗證運算式輸出 — 使用&#x200B;**[!UICONTROL 預覽]**&#x200B;標籤。
   * 從相同的提示產生另一個建議 — 使用&#x200B;**[!UICONTROL 重新產生]**。
   * 清除討論並重新開始 — 使用&#x200B;**[!UICONTROL 重設]**。
   * 在完整編輯器中調整運算式 — 按一下![編輯圖示](assets/do-not-localize/Smock_Edit_18_N.svg "編輯")圖示以開啟&#x200B;**[!UICONTROL Personalization編輯器]**。

1. 當您對結果感到滿意時，請按一下&#x200B;**[!UICONTROL 插入]**，將運算式新增至您的內容。
