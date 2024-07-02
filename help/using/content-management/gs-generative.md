---
solution: Journey Optimizer
product: journey optimizer
title: 開始使用 AI 助理
description: 了解如何存取和使用 Journey Optimizer 的 AI 助理
feature: Content Assistant
topic: Content Management
role: User
level: Beginner
badge: label="Beta" type="Informative"
hide: true
hidefromtoc: true
exl-id: 6e291ce3-f324-4e5d-975b-5229dea4d581
source-git-commit: 59ecb9a5376e697061ddac4cc68f09dee68570c0
workflow-type: ht
source-wordcount: '658'
ht-degree: 100%

---

# 開始使用 AI 助理 {#gs-content-assistant}

>[!CONTEXTUALHELP]
>id="ajo_ai_generation_settings"
>title="AI 助理"
>abstract="當您精心設計並個人化您的交付內容後，您就可以使用 AI 助理來增強內容。 此功能可讓您透過描述想要產生的內容來微調內容，進而簡化個人化和內容改善的過程。"


>[!CONTEXTUALHELP]
>id="ajo_ai_generation_context"
>title="使用 AI 助理定義內容"
>abstract="若要使用選取的內容作為內容產生的輸入，請啟動&#x200B;**使用原始內容**&#x200B;切換。您也可以上傳您的品牌資產，以便作為來源使用。 如果您未使用選取的內容，則必須上傳及選取品牌資產。"


>[!CONTEXTUALHELP]
>id="ajo_ai_generation_start"
>title="Adobe 生成式 AI 術語"
>abstract="要存取此功能，您必須同意 Adobe Experience Cloud Generative Al 使用者指南。您為此功能提供的任何提示、內容、補充資訊或其他輸入內容都必須與特定內容相關，其中可能包括您的品牌推廣材料、網站內容、資料、此類資料的結構描述、範本或其他受信任檔案，並且不得包含任何個人資訊 (個人資訊包括可連結回特定個人的任何內容)。 您應該檢閱此功能的任何輸出是否準確，並確定它適合您的使用案例"
>additional-url="https://www.adobe.com/tw/legal/licenses-terms/adobe-gen-ai-user-guidelines.html" text="Adobe 生成式 AI 使用者手冊"

>[!BEGINSHADEBOX]

**目錄**

* 開始使用 AI 助理
* [使用 AI 助理產生電子郵件](generative-email.md)
* [使用 AI 助理產生簡訊](generative-sms.md)
* [使用 AI 助理推播產生](generative-push.md)
* [使用 AI 助理進行內容實驗](generative-experimentation.md)

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Adobe Journey Optimizer 中的 AI Assistant 目前僅作為測試版提供給部分使用者。

Adobe Journey Optimizer 中的 AI 助理可為文字和影像提供主動式內容變化建議。它可用於電子郵件、推播和簡訊管道。這項新功能提供提示型文字與影像產生功能。 透過 Adobe Firefly 管理影像產生功能。

使用 AI 助理，利用不同的主要標題和影像進行實驗，讓訊息的影響達到最佳成效。 產生多個變體並建置實驗加以比較。 運用 Journey Optimizer 內容實驗，您可以定義多種訊息處理，以測量對目標對象執行哪種處理的效果最佳。 您可以選擇變更傳遞內容或主旨。 訊息對象會隨機分配給每種處理，以就指定的量度而言，判斷哪種處理的效果最佳。 若要了解內容實驗的詳細資訊，請參閱[本章節](../content-management/content-experiment.md)。

## 護欄與限制 {#generative-guardrails}

以下列出使用 Journey Optimizer 的 AI 助手產生電子郵件的一般準則：

* 產生內容的品質很大程度上受到您定義的行銷目標/提示的影響。 使用定義明確的提示讓 GenAI 模型準確解釋。  
* 上傳品牌資產以獲得準確的品牌內容。 另外，內容以公開資訊為依據。上傳的內容可以採用以下格式：PDF、JPEG、PNG 或 ZIP 檔案 (支援的檔案格式)。
* 上傳的品牌資產最大為 50MB。較大的檔案或大量影像可以處理，但處理時間會增加。
* 最好使用 Adobe Campaign 創作的電子郵件範本 (最好是[內建電子郵件範本](../email/use-email-templates.md)、品牌特定範本或自訂範本) 來建立電子郵件內容。 建議電子郵件範本最多包含 8-10 張影像。
* 選擇變體時，請確保使用向上、向下或標記圖示報告任何有問題的輸出。
* 您對 AI 助理的使用必須遵守 Adobe Experience Cloud Generative AI 使用者指南。 [了解更多](https://www.adobe.com/tw/legal/licenses-terms/adobe-gen-ai-user-guidelines.html)

以下限制適用於 Journey Optimizer 的 AI Assistant：

* 支援的語言僅有英文。
* 僅適用於電子郵件、推播和簡訊管道。
* GenAI 內容可能不完全準確：請分享您的回饋，以便我們的工程師可以改進模型。
* 您可以上傳多個品牌資產，但對於特定產生內容只能利用一個。

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
</tr></table>
