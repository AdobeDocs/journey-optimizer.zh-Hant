---
solution: Journey Optimizer
product: journey optimizer
title: 管理品牌
description: 瞭解如何建立及管理您的創造性模型
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: 9ef6b02c-0a17-4b46-bcd3-8e922eef059a
source-git-commit: d2110b995bc26df861825cdd49ca2fd39f904442
workflow-type: tm+mt
source-wordcount: '501'
ht-degree: 0%

---

# 建立和管理產生模型 {#generative-models}

使用內建模型、自訂Firefly模型和協力廠商影像產生提供者，擴展您的AI影像建立功能，以符合您的特定需求並改善品牌一致性。

選擇符合您需求的正確模式：

- **[!UICONTROL Adobe模型]**&#x200B;由Firefly Image Model 4提供技術支援，現成可用立即產生影像，無需額外設定。
- 由Gemini 2.5 Flash支援的&#x200B;**[!UICONTROL 合作夥伴機型]**&#x200B;針對特定使用案例提供特殊功能。 如需在AI Assistant中的影像上使用&#x200B;**Gemini**&#x200B;搭配&#x200B;**文字重疊**&#x200B;的逐步工作流程，請參閱[使用Gemini做為文字重疊影像的產生模型](generative-uc.md#generative-gemini)。
- **[!UICONTROL 自訂模型]**&#x200B;是在您自己的資產上訓練並由您的組織新增的品牌特定模型。

  在&#x200B;**[!UICONTROL Adobe Firefly檔案]**&#x200B;中進一步瞭解[自訂模型](https://helpx.adobe.com/tw/firefly/web/work-with-enterprise-features/train-custom-models/custom-models-overview.html)

在設定之後，當您在內容中建立影像時，可以選取任何產生模型。 [進一步瞭解如何產生影像](generative-image.md)。

## 管理產生模型

從集中位置管理您的產生模型。 檢視所有可用的模式、篩選和搜尋以尋找特定模式，並為您的品牌設定其設定。

1. 從&#x200B;**[!UICONTROL 品牌]**&#x200B;功能表，選取&#x200B;**[!UICONTROL 產生式模型]**&#x200B;標籤。

   ![](assets/gen-model-manage-1.png){zoomable="yes"}

1. 按一下![](assets/do-not-localize/Smock_Filter_18_N.svg)圖示以存取篩選功能表。 依&#x200B;**[!UICONTROL 型別]**&#x200B;或&#x200B;**[!UICONTROL 狀態]**&#x200B;篩選模型。

   ![](assets/gen-model-manage-2.png){zoomable="yes"}

1. 使用搜尋列依名稱尋找特定的產生模型。

1. 按一下![](assets/do-not-localize/Smock_More_18_N.svg)圖示以存取進階功能表，您可在此啟用或停用模型，或將其刪除。

   請注意，只能刪除&#x200B;**[!UICONTROL 自訂模型]**。

   ![](assets/gen-model-manage-6.png){zoomable="yes"}

1. 按一下[新增模型]&#x200B;**&#x200B;**，從頭開始建立新的產生模型。

現在當您在內容中建立影像時，可以選取任何產生模型。 [進一步瞭解如何產生影像](generative-image.md)。

## 新增產生模型

>[!IMPORTANT]
>
>建立自訂Firefly模型需要Firefly ETLA合約。

自訂Firefly模型是在您自己的資產上訓練的品牌專屬AI模型，可讓您產生與品牌識別、風格和視覺准則完全一致的影像。

透過建立自訂Firefly模型提供者，您可以將AI功能擴展至預設模型之外，並確保產生的內容一致地反映您品牌獨特的審美觀和要求。

➡️ [瞭解如何訓練您的自訂模型](https://helpx.adobe.com/tw/firefly/web/work-with-enterprise-features/train-custom-models/train-firefly-custom-models.html)

1. 從&#x200B;**[!UICONTROL 品牌]**&#x200B;功能表，存取&#x200B;**[!UICONTROL 產生式模型]**&#x200B;索引標籤，然後按一下&#x200B;**[!UICONTROL 新增模型]**。

   ![](assets/gen-model-manage-4.png){zoomable="yes"}

1. 輸入模型的&#x200B;**[!UICONTROL 名稱]**。

1. 輸入您的&#x200B;**[!UICONTROL 模型識別碼]**。

   +++ 尋找您的Firefly模型ID

   1. 存取Firefly網站，並導覽至您訓練的模型。
   1. 存取[預覽和測試](https://helpx.adobe.com/tw/firefly/web/work-with-enterprise-features/train-custom-models/train-firefly-custom-models.html#preview-and-test)功能表。
   1. 在URL中，找出`customModelId=`之後的值。 複製此值以用作模型ID。

   如需詳細資訊，請參閱[Firefly自訂模型檔案](https://helpx.adobe.com/tw/firefly/web/work-with-enterprise-features/train-custom-models/manage-custom-models.html)。

   ![](assets/gen-model-manage-10.png){zoomable="yes"}

   +++

   </br>

   ![](assets/gen-model-manage-5.png){zoomable="yes"}

1. 選擇性地輸入&#x200B;**[!UICONTROL 描述]**&#x200B;以協助識別模型。

1. 按一下&#x200B;**[!UICONTROL 測試連線]**&#x200B;以驗證模型組態。

1. 連線測試成功後，按一下&#x200B;**[!UICONTROL 儲存]**&#x200B;以儲存您的模型組態。

   ![](assets/gen-model-manage-7.png){zoomable="yes"}

1. 儲存後，您的自訂模型會新增至模型清單。 您可以隨時停用或刪除它。

   ![](assets/gen-model-manage-8.png){zoomable="yes"}

<!--
1. Once the connection test is successful, choose whether to enable the model for selected brands.

1. Enable or disable the option to connect the model to all brands.

    If disabled, select which brands this model should be applied to.
-->

設定之後，當您在內容中建立影像時，可以選取任何自訂的產生模型。 [進一步瞭解如何產生影像](generative-image.md)。

![](assets/gen-model-manage-9.png){zoomable="yes"}
