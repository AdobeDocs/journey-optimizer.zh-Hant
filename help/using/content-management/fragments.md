---
solution: Journey Optimizer
product: journey optimizer
title: 開始使用片段
description: 瞭解如何使用內容片段，以在Journey Optimizer行銷活動和歷程中重複使用內容
feature: Fragments
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: 7131a953-baca-4e7c-a8df-97c0bd6ac567
source-git-commit: c42fc1069e11b8e34b7477fc26ed8a6b4ef95ac7
workflow-type: tm+mt
source-wordcount: '315'
ht-degree: 11%

---

# 開始使用片段 {#fragments}

>[!CONTEXTUALHELP]
>id="ajo_create_fragment"
>title="定義您專屬的內容片段"
>abstract="建立及管理獨立的內容片段，以便在多個歷程和行銷活動中重複使用你的內容。"
>additional-url="https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer/using/content-management/fragments/create-fragments" text="建立內容片段"

片段是可重複使用的元件，可在一封或多封電子郵件中加以參照 [!DNL Journey Optimizer] 行銷活動和歷程。 此功能允許預先建置多個自訂內容區塊，可供行銷使用者在改良的設計流程中快速組合電子郵件內容。

![](../rn/assets/do-not-localize/fragments.gif)

➡️ [瞭解如何在這些影片中管理、編寫和使用片段](#video-fragments)

若要充分利用片段：

* **建立您自己的片段**：從頭開始建立視覺效果或運算式片段，或是將內容儲存為片段。 [瞭解如何建立片段](#create-fragments). 此外，您也可以善用Journey Optimizer **內容重設API** 以管理內容片段。 有關詳細資訊，請參閱 [Journey Optimizer API檔案](https://developer.adobe.com/journey-optimizer-apis/references/content/){target="_blank"}.
* **重複使用您的片段：** 視需要在您的內容中多次使用。 另請參閱 [新增視覺片段](../email/use-visual-fragments.md) 和 [利用運算式片段](../personalization/use-expression-fragments.md)

## 開始之前 {#fragment-prerequisites}

若要建立、編輯、封存和發佈片段，您需要 **[!DNL Manage library items]** 和 **[Publish片段]** 包含在中的許可權 **[!DNL Content Library Manager]** 產品設定檔。 [了解更多](../administration/ootb-product-profiles.md#content-library-manager)

在此版本中，適用下列限制：

* **視覺片段** 僅適用於電子郵件頻道。
* **運算式片段** 不適用於應用程式內頻道。

## 視覺效果和運算式片段 {#visual-expression}

提供兩種型別的片段：

* **視覺片段** 是預先定義的視覺化區塊，您可以使用在多個電子郵件傳遞中重複使用 [傳送Designer電子郵件](../email/get-started-email-design.md)，或在 [內容範本](../email/use-email-templates.md).
* **運算式片段** 是預先定義的運算式，可從的 [個人化編輯器](../personalization/personalization-build-expressions.md).

所有已建立的片段都可從以下位置存取： **[!UICONTROL 內容管理]** > **[!UICONTROL 片段]**  左側功能表。 [瞭解如何管理片段](../content-management/manage-fragments.md)

![](assets/fragment-list.png)

## 操作說明影片 {#video-fragments}

瞭解如何管理、編寫和使用 **視覺片段** 在 [!DNL Journey Optimizer].

>[!VIDEO](https://video.tv.adobe.com/v/3419932/?quality=12)

瞭解如何管理、編寫和使用 **運算式片段** 在 [!DNL Journey Optimizer].

>[!VIDEO](https://video.tv.adobe.com/v/3424587/?quality=12)
