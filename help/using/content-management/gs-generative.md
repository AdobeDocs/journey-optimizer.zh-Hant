---
solution: Journey Optimizer
product: journey optimizer
title: 開始使用Journey Optimizer中的AI助理
description: 瞭解如何在Journey Optimizer中存取及使用AI助理
feature: Content Assistant
topic: Content Management
role: User
level: Beginner
exl-id: 6e291ce3-f324-4e5d-975b-5229dea4d581
source-git-commit: 5cfae89416219fac54d310d9fa3f40fdfdd8878e
workflow-type: tm+mt
source-wordcount: '846'
ht-degree: 75%

---

# 開始使用 AI 助理 {#gs-content-assistant}

>[!CONTEXTUALHELP]
>id="ajo_ai_generation_settings"
>title="Journey Optimizer中的AI助理"
>abstract="完成傳遞的製作和個人化後，您可以使用Journey Optimizer中的AI助理來增強內容。 此功能可讓您透過描述想要產生的內容來微調內容，進而簡化個人化和內容改善的過程。"

>[!CONTEXTUALHELP]
>id="ajo_ai_generation_context"
>title="上傳品牌資產"
>abstract="「上傳品牌資產」選單可讓您新增任何品牌資產，其中包含可為Journey Optimizer中的AI助理提供額外內容的內容，或選取先前上傳的資產。 此選項可確保 AI 助理能夠存取所有必要的資料，以增強其功能與相關性。"

>[!CONTEXTUALHELP]
>id="ajo_ai_generation_start"
>title="Adobe 生成式 AI 條款"
>abstract="要存取此功能，您必須同意 Adobe Experience Cloud 生成式 AI 使用者準則。請檢查此功能之任何輸出的準確性，並確保它適合您的使用案例。"
>additional-url="https://www.adobe.com/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html" text="Adobe 生成式 AI 使用者準則"

>[!INFO]
>
>透過[即時功能預覽](https://experienceleague.adobe.com/zh-hant/apps/journey-optimizer/ai-assistant-content-accelerator){target="_blank"}，讓您親身體驗實作，直接探索並全面了解各項功能。


Adobe Journey Optimizer中的AI Assistant由Microsoft Azure OpenAI和Adobe Firefly提供技術支援，針對文字和影像提供主動式內容變化建議。 它可用於電子郵件、推播和簡訊管道。這項新功能提供提示型文字與影像產生功能。 透過 Adobe Firefly 管理影像產生功能。

使用Adobe Journey Optimizer中的AI小幫手，透過實驗不同的主要標題和影像，將訊息的影響最佳化。 產生多個變體並建置實驗加以比較。 運用 Journey Optimizer 內容實驗，您可以定義多種訊息處理，以測量對目標客群執行哪種處理的效果最佳。 您可以選擇變更傳遞內容或主旨。 訊息客群會隨機分配給每種處理，以就指定的量度而言，判斷哪種處理的效果最佳。 若要了解內容實驗的詳細資訊，請參閱[本章節](../content-management/content-experiment.md)。

>[!IMPORTANT]
>
>* 開始使用此功能之前，請先閱讀相關的[護欄與限制](#generative-guardrails)。
>
>
>* 您必須先同意[使用者合約](https://www.adobe.com/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html){target="_blank"}，才能在Adobe Journey Optimizer中使用AI小幫手。 如需詳細資訊，請聯絡您的 Adobe 代表。

## 存取AI助理 {#generative-access}

若要存取Adobe Journey Optimizer中的AI小幫手功能，使用者必須被授予&#x200B;**產生內容**&#x200B;許可權。 [了解更多](../administration/permissions.md)

+++  了解如何指派內容產生相關權限

1. 在&#x200B;**權限**&#x200B;產品中，前往&#x200B;**角色**&#x200B;標籤，然後選取所需的&#x200B;**角色**。

1. 按一下&#x200B;**編輯**&#x200B;以修改權限。

1. 新增 **AI 助理**&#x200B;資源，然後從下拉式選單中，選取&#x200B;**產生內容**。

   ![](assets/gen-ai-role.png){zoomable="yes"}

1. 按一下&#x200B;**儲存**，以套用所做的變更。

   任何已指派給此角色的使用者都會自動更新其權限。

1. 若要將此角色指派給新使用者，請瀏覽至&#x200B;**角色**&#x200B;儀表板中的&#x200B;**使用者**&#x200B;標籤，然後按一下&#x200B;**新增使用者**。

1. 輸入使用者的名稱、電子郵件地址，或從清單當中選擇，然後按一下&#x200B;**儲存**。

1. 如果之前未建立使用者，請參閱[此文件](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/access-control/abac/permissions-ui/users)。

使用者將會收到一封電子郵件，提供存取執行個體的指示。

+++

## 護欄與限制 {#generative-guardrails}

在Adobe Journey Optimizer中使用AI助理產生電子郵件的一般准則如下：

* 產生內容的品質很大程度上受到您定義的行銷目標/提示的影響。使用定義明確的提示讓 GenAI 模型準確解釋。  
* 上傳品牌資產以獲得準確的品牌內容。 另外，內容以公開資訊為依據。上傳的內容可以採用以下格式：PDF、JPEG、PNG 或 ZIP 檔案 (支援的檔案格式)。
* 上傳的品牌資產最大為 50MB。較大的檔案或大量影像可以處理，但處理時間會增加。
* 使用品牌特定或自訂範本，以使用Adobe Journey Optimizer中的AI助理建立您的電子郵件內容。 建議電子郵件範本最多包含 8-10 張影像。
* 選擇變體時，請確保使用向上、向下或標記圖示報告任何有問題的輸出。
* 使用 AI 助理必須遵守 Adobe Experience Cloud 生成式 AI 使用者手冊。[了解更多](https://www.adobe.com/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html)
* Adobe 承諾提升在媒體創作中使用生成式 AI 工具的透明度，Adobe 將在下載或匯出的內容或專案包含 Firefly 產生的資產時，套用 Content Credentials。[了解更多](https://helpx.adobe.com/firefly/using/content-credentials.html)

下列限制適用於Adobe Journey Optimizer中的AI助理：

* 支援的語言僅有英文。非英文輸入可能會產生不一致或錯誤的結果。 目前無法解決或改善因非英文的回應所引起的問題。
* 僅適用於電子郵件、推播、網頁及簡訊管道。
* GenAI 內容可能不完全準確：請分享您的回饋，以便我們的工程師可以改進模型。
* 您可以上傳多個品牌資產，但對於特定產生內容只能利用一個。


## AI 助理內容產生功能 {#generative-features}


<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="generative-email.md">
<img alt="電子郵件產生" src="assets/do-not-localize/text-genai.jpeg">
</a>
<div>
<a href="generative-email.md"><strong>電子郵件產生</strong></a>
</div>
<p>
</td>
<td>
<a href="generative-sms.md">
<img alt="簡訊產生" src="assets/do-not-localize/image-genai.jpeg">
</a>
<div><a href="generative-sms.md"><strong>簡訊產生</strong>
</div>
<p>
</td>
<td>
<a href="generative-push.md">
<img alt="推播產生" src="assets/do-not-localize/email-genai.jpeg">
</a>
<div>
<a href="generative-push.md"><strong>推播通知產生</strong></a>
</div>
<p></td>
<td>
<a href="generative-web.md">
<img alt="網頁產生" src="assets/do-not-localize/web-genai.jpeg">
</a>
<div><a href="generative-web.md"><strong>網頁產生</strong>
</div>
<p>
</td>
</tr></table>
