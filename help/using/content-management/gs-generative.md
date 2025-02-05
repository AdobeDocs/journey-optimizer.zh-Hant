---
solution: Journey Optimizer
product: journey optimizer
title: 開始使用 Journey Optimizer 內容加速器中的 AI 助理
description: 了解如何在 Journey Optimizer 內容加速器中存取並使用 AI 助理完成工作
feature: Content Assistant
topic: Content Management
role: User
level: Beginner
exl-id: 6e291ce3-f324-4e5d-975b-5229dea4d581
source-git-commit: 2de3766c9fea36422c017ccaab3eb0a2501c6740
workflow-type: tm+mt
source-wordcount: '874'
ht-degree: 98%

---

# 開始使用 AI 助理內容加速器 {#gs-content-assistant}

>[!CONTEXTUALHELP]
>id="ajo_ai_generation_settings"
>title="Journey Optimizer 中的 AI 助理內容加速器"
>abstract="精心打造並個人化您要傳遞的內容之後，便可以使用 Journey Optimizer AI 助理內容加速器來強化內容。此功能可讓您透過描述想要產生的內容來微調內容，進而簡化個人化和內容改善的過程。"

>[!CONTEXTUALHELP]
>id="ajo_ai_generation_context"
>title="上傳品牌資產"
>abstract="您可以使用「上傳品牌資產」選單新增任何品牌資產，所含內容可為 Journey Optimizer AI 助理內容加速器提供更多背景資訊，或者選取先前上傳的資產。此選項可確保 AI 助理能夠存取所有必要的資料，以增強其功能與相關性。"

>[!CONTEXTUALHELP]
>id="ajo_ai_generation_start"
>title="Adobe 生成式 AI 條款"
>abstract="要存取此功能，您必須同意 Adobe Experience Cloud 生成式 AI 使用者準則。請檢查此功能之任何輸出的準確性，並確保它適合您的使用案例。"
>additional-url="https://www.adobe.com/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html" text="Adobe 生成式 AI 使用者準則"

>[!INFO]
>
>透過[即時功能預覽](https://experienceleague.adobe.com/zh-hant/apps/journey-optimizer/ai-assistant-content-accelerator){target="_blank"}，讓您親身體驗實作，直接探索並全面了解各項功能。


在 Adobe Journey Optimizer 中，Azure OpenAI 與 Azure 視覺技術所支援的 AI 助理內容加速器，可為文字和影像提供主動式內容變化版本建議。它可用於電子郵件、推播和簡訊管道。這項新功能提供提示型文字與影像產生功能。 透過 Adobe Firefly 管理影像產生功能。

使用 Adobe 中的 AI 助理內容加速器，利用不同的主要標題和影像進行實驗，讓訊息的影響達到最佳成效。 產生多個變體並建置實驗加以比較。 運用 Journey Optimizer 內容實驗，您可以定義多種訊息處理，以測量對目標客群執行哪種處理的效果最佳。 您可以選擇變更傳遞內容或主旨。 訊息客群會隨機分配給每種處理，以就指定的量度而言，判斷哪種處理的效果最佳。 若要了解內容實驗的詳細資訊，請參閱[本章節](../content-management/content-experiment.md)。

>[!IMPORTANT]
>
>* 開始使用此功能之前，請先閱讀相關的[護欄與限制](#generative-guardrails)。
>
>
>* 您必須先同意[使用者合約](https://www.adobe.com/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html){target="_blank"}後，才能使用 Adobe Journey Optimizer 中的內容加速 AI 助理內容加速器。如需詳細資訊，請聯絡您的 Adobe 代表。

## 存取 AI 助理內容加速器 {#generative-access}

若要存取 Adobe Journey Optimizer 中的 AI 助理內容加速器，使用者必須擁有&#x200B;**產生內容**&#x200B;的權限。[了解更多](../administration/permissions.md)

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

以下會列出使用 Adobe Journey Optimizer 的 AI 助理內容加速器產生電子郵件的一般準則：

* 產生的內容品質強烈受到您定義的行銷目標/提示所影響。 使用定義明確的提示讓 GenAI 模型準確解釋。  
* 上傳品牌資產以獲得準確的品牌內容。 另外，內容以公開資訊為依據。上傳的內容可以採用以下格式：PDF、JPEG、PNG 或 ZIP 檔案 (支援的檔案格式)。
* 上傳的品牌資產最大為 50MB。較大的檔案或大量影像可以處理，但處理時間會增加。
* 使用品牌特定範本，或是自訂範本，就能使用 Adobe Journey Optimizer 中的 AI 助理內容加速器，建立電子郵件內容。建議電子郵件範本最多包含 8-10 張影像。
* 選擇變體時，請確保使用向上、向下或標記圖示報告任何有問題的輸出。
* 使用 AI 助理必須遵守 Adobe Experience Cloud 生成式 AI 使用者手冊。[了解更多](https://www.adobe.com/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html)
* Adobe 承諾提升在媒體創作中使用生成式 AI 工具的透明度，Adobe 將在下載或匯出的內容或專案包含 Firefly 產生的資產時，套用 Content Credentials。[了解更多](https://helpx.adobe.com/firefly/using/content-credentials.html)

以下限制適用於 Adobe Journey Optimizer 的 AI 助理內容加速器：

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
