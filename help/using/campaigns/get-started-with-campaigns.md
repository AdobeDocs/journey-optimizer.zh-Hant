---
solution: Journey Optimizer
product: journey optimizer
title: 開始使用行銷活動
description: 深入了解 Journey Optimizer 的行銷活動
feature: Campaigns
topic: Content Management
role: User
level: Beginner
keywords: 行銷活動、如何進行、開始、最佳化程式
exl-id: e2506a43-e4f5-48af-bd14-ab76c54b7c90
source-git-commit: 5821bc3f3c6e81ae1ae7389bbca1bdcec11cc805
workflow-type: tm+mt
source-wordcount: '809'
ht-degree: 70%

---

# 開始使用行銷活動 {#get-started-campaigns}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule"
>title="行銷活動排程"
>abstract="預設情況下，行銷活動經由手動啟用後開始執行，並在訊息傳送一次後立即結束。您可以彈性設定發送訊息的具體日期和時間。此外，您可以對定期執行的動作行銷活動指定結束日期。在動作觸發程序中，你亦可根據自己的偏好設定訊息傳送頻率。"

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule_start"
>title="行銷活動開始"
>abstract="指定傳送訊息的日期和時間。"

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule_end"
>title="行銷活動結束"
>abstract="指定應停止執行週期性行銷活動的時間。"

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule_triggers"
>title="行銷活動動作觸發程序"
>abstract="定義應傳送行銷活動訊息的頻率。"

>[!CONTEXTUALHELP]
>id="ajo_campaigns_throttling"
>title="速率控制"
>abstract="指定想要的速率限制，以設定行銷活動的速率控制。此功能對於防止下游系統 (例如登陸頁面或客戶服務平台) 上的超載特別有用。"

>[!CONTEXTUALHELP]
>id="ajo_homepage_card3"
>title="建立行銷活動"
>abstract="使用 **Adobe Journey Optimizer**，透過各種管道將一次性內容傳遞至特定對象。當使用歷程時，動作會依序執行。 透過行銷活動，可同時執行動作 (立即執行或根據指定的排程執行)。"

>[!CONTEXTUALHELP]
>id="campaigns_list"
>title="行銷活動"
>abstract="建立行銷活動以跨不同管道向特定客群提供一次性內容。建立行銷活動之前，請確保您準備好可供使用的管道設定與 Adobe Experience Platform 客群。"

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_type"
>title="行銷活動類型"
>abstract="選取行銷活動的型別。 可用的管道會依選取的型別而有所不同。 <br>**排程行銷活動** （動作行銷活動） — 適用於可以排程在特定時間執行的簡單、一次性批次通訊。<br>**API觸發的行銷活動** — 透過API呼叫啟動，可直接從外部系統啟用自動化、事件型傳訊。<br>**協調的行銷活動** — 提供視覺化的拖放畫布，以設計和自動化複雜的多步驟行銷工作流程，從對象細分到跨管道的個人化訊息傳遞。"

使用 Journey Optimizer 行銷活動，透過各種頻道將一次性內容傳遞至特定客群。 當使用歷程時，動作會依序執行。 透過行銷活動，可同時執行動作 (立即執行或根據指定的排程執行)。

![](assets/gs-campaigns.png)

您可以在Journey Optimizer中建立不同型別的行銷活動。 支援的管道和使用案例會因行銷活動型別而異。 以下列出這些型別。

* **動作行銷活動**

  行動行銷活動（或排程行銷活動）允許對行銷使用案例進行簡單的臨時批次通訊，例如促銷優惠、參與行銷活動、公告、法律通知或原則更新。 在此頁面[上進一步瞭解Action行銷活動功能、使用案例和支援的管道](create-campaign.md)。

* **由 API 觸發的行銷活動**

  API觸發的行銷活動可讓行銷通訊在適當的時間聯絡對象，或讓交易/營運訊息聯絡個人（例如密碼重設），其需求可能涉及個人化，不僅使用設定檔屬性，還會在觸發程式（即REST API裝載）中使用即時內容資料。 在此頁面[上進一步瞭解API觸發的行銷活動功能、使用案例和支援的管道](api-triggered-campaigns.md)。

* **協調的行銷活動**

  Adobe Journey Optimizer 中的行銷活動協調可跨頻道支援品牌啟動的複雜行銷活動，協助您大規模提高參與度、收入和客戶忠誠度。

  雖然跨頻道行銷至關重要，但協調的行銷活動可使其順暢無礙。透過視覺化的拖放介面，您可以跨多個頻道設計和自動化複雜的行銷工作流程，從細分到訊息傳遞。所有事情都在一個直覺式環境中進行，專為速度、控制能力和效率而打造。 在此頁面[上進一步瞭解協調行銷活動功能、使用案例和支援的管道](../orchestrated/gs-orchestrated-campaigns.md)。

## 先決條件 {#prerequisites}

在建立行銷活動之前，請確定您已檢閱下列先決條件。

### 權限

行銷活動僅適用於具有下列適當權限的使用者。[瞭解有關 Journey Optimizer 內建角色的詳細資訊](../administration/ootb-product-profiles.md)

>[!BEGINTABS]

>[!TAB 動作行銷活動]

行銷活動管理員
行銷活動核准者
行銷活動經理
行銷活動檢視者

>[!TAB 由 API 觸發的行銷活動]

行銷活動管理員
行銷活動核准者
行銷活動經理
行銷活動檢視者

>[!TAB 協調的行銷活動]

協調的行銷活動管理員
協調的行銷活動核准者
協調的行銷活動經理
協調的行銷活動檢視者

>[!ENDTABS]

如果您無法存取行銷活動功能，請聯絡您的管理員以請求必要的權限。

+++了解如何指派行銷活動相關角色

1. 若要將角色指派給 [!DNL Permissions] 產品中的使用者，請導覽至&#x200B;**[!UICONTROL 角色]**&#x200B;標籤，然後選擇其中一個與上述&#x200B;**[!UICONTROL 角色]**&#x200B;相關的內建行銷活動。

1. 在&#x200B;**[!UICONTROL 使用者]**&#x200B;標籤中，按一下&#x200B;**[!UICONTROL 新增使用者]**。

1. 輸入您的使用者名稱或電子郵件地址，或從清單中選擇使用者，然後按一下&#x200B;**[!UICONTROL 儲存]**。

   如果之前未建立使用者，請參閱[新增使用者文件](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/access-control/ui/users)。

接著，使用者應會收到一封電子郵件，並重新導向至您的執行個體。

+++

### 客群

建立行銷活動之前必須有可用的客群。 [開始使用客群](../audience/about-audiences.md)。

### 管道設定

若要選取頻道，您必須建立相對應的頻道設定 (即預設)，使其可供使用。[了解如何設定頻道設定](../configuration/channel-surfaces.md)。

## 讓我們深入探討

目前您已瞭解[!DNL Journey Optimizer]中的行銷活動，該是時候深入探討這些文件章節內容，才能開始建立首次行銷活動。

<table style="table-layout:fixed"><tr style="border: 0; text-align: center;">
<td><a href="create-campaign.md"><img width="70%" alt="動作行銷活動" src="assets/do-not-localize/gs-action-campaign.png"></a><br/><a href="create-campaign.md">動作行銷活動</a></td>
<td><a href="api-triggered-campaigns.md"><img width="70%" alt="簡訊" src="assets/do-not-localize/gs-api-triggered-campaign.png"></a><br/><a href="api-triggered-campaigns.md">由 API 觸發的行銷活動</a></td>
<td><a href="../orchestrated/gs-orchestrated-campaigns.md"><img width="70%" alt="推播" src="assets/do-not-localize/gs-orchestrated-campaign.png"></a><a href="../orchestrated/gs-orchestrated-campaigns.md">協調的行銷活動</a></td>
</tr></table>
