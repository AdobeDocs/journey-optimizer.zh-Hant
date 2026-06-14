---
solution: Journey Optimizer
product: journey optimizer
title: 在Journey Optimizer中調整垂直對齊和邊框間距
description: 了解如何調整垂直對齊方式和邊框間距
feature: Email Design
topic: Content Management
role: User
level: Beginner, Intermediate
keywords: 垂直對齊，電子郵件編輯器，邊框間距
exl-id: 1e1d90ff-df5d-4432-a63a-a32d0d281d48
TQID: https://experienceleague.adobe.com/vJhROWi5ZiOLJrESMe-oUkmve1vSXrE5sNewDLpv-eE
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2:
  - id: ee5bb250-0884-4d71-86eb-d8489e8bcadd
  - id: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
source-git-commit: bc98cb2b61c7c5c8dac78b494fe293a4106a88c4
workflow-type: tm+mt
source-wordcount: 412
ht-degree: 6%

---

# 調整垂直對齊與邊框間距 {#alignment-and-padding}

>[!BEGINSHADEBOX]

**在此頁面上：**&#x200B;瞭解如何調整Email Designer中欄和結構的垂直對齊和填補，包括如何修正剩餘片段填補，以實現正確的行動呈現。

>[!ENDSHADEBOX]

在此範例中，我們將調整由三欄組成的結構元件內的邊框間距和垂直對齊方式。

1. 直接在電子郵件中選取結構元件，或使用左側功能表中可用的&#x200B;**[!UICONTROL 導覽樹狀結構]**。

1. 在工具列中按一下&#x200B;**[!UICONTROL 選取資料行]**，然後選擇您要編輯的資料行。 您也可以從結構樹中選取它。

   該欄的可編輯引數會顯示在&#x200B;**[!UICONTROL 樣式]**&#x200B;索引標籤中。

   ![](assets/alignment_2.png)

1. 在&#x200B;**[!UICONTROL 對齊方式]**&#x200B;下，選取&#x200B;**[!UICONTROL 上]**、**[!UICONTROL 中]**&#x200B;或&#x200B;**[!UICONTROL 下]**。

   ![](assets/alignment_3.png)

1. 在&#x200B;**[!UICONTROL 內距]**&#x200B;下，定義所有邊的內距。

   若要微調內距，請選取&#x200B;**[!UICONTROL 每一邊不同的內距]**。 按一下鎖定圖示以中斷同步。

   ![](assets/alignment_4.png)

1. 以類似的方式調整其他欄的對齊方式和邊框間距。

1. 儲存您的變更。

>[!TIP]
>
>在Android裝置上為Gmail設計電子郵件內容時，請確定影像和分隔符號使用欄邊距，而非大型的固定邊界。 Android上的Gmail經常會不正確地呈現過大的影像和邊界，造成版面溢位或分隔線減少。 使用較小的影像寬度或仰賴欄式邊框間距來維持顯示的一致性。

## 使用階層連結導覽管理片段邊距 {#fragment-padding-breadcrumb}

在電子郵件Designer中使用[片段](../content-management/fragments.md)時，您可能會遇到隱藏的或殘留的內距，這些內距對行動轉譯的影響與案頭不同。 當片段已解除鎖定或[繼承已中斷](use-visual-fragments.md#break-inheritance)時，這會特別常見，因為剩餘的樣式可以保留在基礎欄或文字元件中。

若要識別及編輯片段中的剩餘邊框間距：

1. 使用&#x200B;**[!UICONTROL 導覽樹狀結構]**，或直接按一下編輯器中的元素，以選取片段中的每個父結構或欄。 這有助於您找出行動裝置特有的隱藏邊框間距或邊界。

1. 在階層連結中選取元素後，導覽至右側的&#x200B;**[!UICONTROL 樣式]**&#x200B;索引標籤。

1. 檢閱&#x200B;**[!UICONTROL 內距]**&#x200B;設定，並視需要移除或重新調整內距，以取得正確的行動對齊方式。

1. 如果重複使用片段時對齊問題持續存在，請對片段中的其他欄或文字元件重複此程式。

>[!NOTE]
>
>當重複插入和移除片段時，此行為是預期行為，因為樣式規則可以累積。 請一律使用階層連結導覽來驗證邊框間距值，尤其是在鎖定行動裝置為目標時。