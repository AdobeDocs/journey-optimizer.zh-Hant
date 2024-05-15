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
source-git-commit: 644e0959ee0d0ec8ee0c4ec54c3bcd1cc3c4dda9
workflow-type: tm+mt
source-wordcount: '658'
ht-degree: 54%

---

# 開始使用 AI 助理 {#gs-content-assistant}

>[!CONTEXTUALHELP]
>id="ajo_ai_generation_settings"
>title="AI 助理"
>abstract="精心設計和個人化傳遞後，您可以使用 AI 助理來強化內容。此功能可讓您透過描述您想產生的內容來進行微調，進而簡化個人化和改善內容的流程。"


>[!CONTEXTUALHELP]
>id="ajo_ai_generation_context"
>title="使用AI助理定義內容"
>abstract="若要使用選取的內容作為內容產生的輸入，請啟動 **使用原始內容** 切換。 您也可以上傳您的品牌資產以將其做為來源。如果您不使用所選內容，則必須上傳並選取品牌資產。"


>[!CONTEXTUALHELP]
>id="ajo_ai_generation_start"
>title="Adobe 生成式 AI 詞彙"
>abstract="若要取得此功能的存取權限，您必需同意 Adobe Experience Cloud 生成式 AI 使用者準則。您為此功能提供的任何提示、上下文或補充資訊或其他輸入都必須與特定上下文相關聯，其中可以包括您的品牌素材、網站內容、資料、此類資料的架構、範本或其他可信任文件，並且不得包含任何個人資訊 (個人資訊包括任何可連結到特定個人的資訊)。您應該檢查此功能之任何輸出的準確性，並確保它適合您的使用案例"
>additional-url="https://www.adobe.com/tw/legal/licenses-terms/adobe-gen-ai-user-guidelines.html" text="Adobe 生成式 AI 使用者準則"

>[!BEGINSHADEBOX]

**目錄**

* 開始使用 AI 助理
* [使用 AI 助理產生電子郵件](generative-email.md)
* [使用 AI 助理產生簡訊](generative-sms.md)
* [使用AI助理產生推播](generative-push.md)
* [使用AI助理進行內容實驗](generative-experimentation.md)

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Adobe Journey Optimizer中的AI小幫手目前僅供特定使用者選購，做為Beta版提供。

Adobe Journey Optimizer 中的 AI 助理可為文字和影像提供主動式內容變化建議。它可用於電子郵件、推播和簡訊頻道。 這項新功能提供提示型文字與影像產生功能。 透過 Adobe Firefly 管理影像產生功能。

使用 AI 助理，利用不同的主要標題和影像進行實驗，讓訊息的影響達到最佳成效。 產生多個變體並建置實驗加以比較。 運用 Journey Optimizer 內容實驗，您可以定義多種訊息處理，以測量對目標對象執行哪種處理的效果最佳。 您可以選擇變更傳遞內容或主旨。 訊息對象會隨機分配給每種處理，以就指定的量度而言，判斷哪種處理的效果最佳。 若要了解內容實驗的詳細資訊，請參閱[本章節](../campaigns/content-experiment.md)。

## 護欄和限制 {#generative-guardrails}

在Journey Optimizer中使用AI助理產生電子郵件的一般准則如下：

* 產生的內容品質強烈受到您定義的行銷目標/提示所影響。 使用定義明確的提示讓GenAI模型正確解譯。 
* 上傳品牌資產，以便對品牌內容取得準確資訊。 否則，內容會以公開可用的資訊為基礎。 上傳的內容可以有下列格式：PDF、JPEG、PNG或ZIP檔案（具有支援的檔案格式）。
* 已上傳品牌資產的大小上限為50MB。 大型檔案或大量影像可以運作，但處理時間會增加。
* 最好使用Adobe Campaign編寫的電子郵件範本 [內建電子郵件範本](../email/use-email-templates.md)，此元件為品牌特定範本或自訂範本，可建立您的電子郵件內容。 建議使用最多8至10個影像的電子郵件範本。
* 選擇變體時，請務必使用向上縮圖、向下縮圖或標幟圖示來報告任何有問題的輸出。
* 您使用AI助理須遵守Adobe Experience Cloud Generative AI使用指南。 [了解更多](https://www.adobe.com/tw/legal/licenses-terms/adobe-gen-ai-user-guidelines.html)

下列限制適用於Journey Optimizer中的AI助理：

* 支援的語言只有英文。
* 僅適用於電子郵件、推播和簡訊頻道。
* GenAI內容可能並不一定都準確：請分享您的意見回饋，以便我們的工程師可以調整模型。
* 您可以上傳多個品牌資產，但只能針對特定世代使用一個品牌資產。

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
<a href="generative-push.md"><strong>產生推播通知</strong></a>
</div>
<p></td>
</tr></table>
