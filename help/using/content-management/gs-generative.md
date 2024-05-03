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
source-git-commit: 98ce21578d30ac50665561438715d19d1723f4a7
workflow-type: tm+mt
source-wordcount: '500'
ht-degree: 47%

---

# 開始使用 AI 助理 {#gs-content-assistant}

>[!CONTEXTUALHELP]
>id="ajo_content_generation"
>title="建立該電子郵件內容"
>abstract="Adobe Journey Optimizer AI 助理可為文字和影像提供主動式內容變化建議。其可用於電子郵件、推播、簡訊和 Web 管道。 這項新功能提供提示型文字與影像產生功能。 "

>[!BEGINSHADEBOX]

**目錄**

* **[開始使用 AI 助理](gs-generative.md)**
* [使用 AI 助理產生電子郵件](generative-email.md)
* [使用 AI 助理產生簡訊](generative-sms.md)
* [使用AI助理產生推播](generative-push.md)
* [使用AI助理進行內容實驗](generative-experimentation.md)

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Adobe Journey Optimizer AI 助理目前僅作為測試版提供給部分使用者。 若要加入 Beta 版計畫，請連絡 Adobe 客戶服務。

Adobe Journey Optimizer AI 助理可為文字和影像提供主動式內容變化建議。它可用於電子郵件、推播和簡訊頻道。 這項新功能提供提示型文字與影像產生功能。 透過 Adobe Firefly 管理影像產生功能。

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
