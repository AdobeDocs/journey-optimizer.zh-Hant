---
solution: Journey Optimizer
product: journey optimizer
title: 開始使用行銷活動
description: 深入了解 Journey Optimizer 的行銷活動
feature: Campaigns
topic: Content Management
role: User
level: Beginner
mini-toc-levels: 1
keywords: 行銷活動、如何進行、開始、最佳化程式
exl-id: e2506a43-e4f5-48af-bd14-ab76c54b7c90
source-git-commit: 0ec43a204f5fcf0bddf38cfd381f0ea496c7de70
workflow-type: tm+mt
source-wordcount: '955'
ht-degree: 59%

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
>abstract="選取行銷活動類型。可用管道根據所選類型而有所不同。<br>**已排程行銷活動** (動作行銷活動) – 非常適合簡單的一次性批次通訊，您可以安排在特定時間執行。<br>**API 觸發的行銷活動** – 透過 API 呼叫啟動，啟用直接從外部系統傳送以事件為基礎的自動化訊息功能。<br>**協調式行銷活動** – 提供視覺化的拖放式版面，以便設計和自動化複雜的多步驟行銷工作流程，從客群細分到跨管道傳送個人化訊息皆包含在內。"

>[!CONTEXTUALHELP]
>id="ajo_campaigns_create_orchestration"
>title="行銷活動"
>abstract="建立您的細分流程、精心製作跨管道訊息，並規劃您的行銷活動。支援的管道：電子郵件、簡訊、推播通知。"

>[!CONTEXTUALHELP]
>id="ajo_campaigns_create_scheduled_marketing"
>title="行銷活動"
>abstract="傳遞單次或定期的傳出傳遞或持續的傳入動作。"

>[!CONTEXTUALHELP]
>id="ajo_campaigns_create_scheduled_transactional"
>title="行銷活動"
>abstract="提供單一或定期的傳出交易型動作。"

>[!CONTEXTUALHELP]
>id="ajo_campaigns_create_api_marketing"
>title="行銷活動"
>abstract="向目標客群傳遞個人化行銷通訊內容。支援的管道：電子郵件、簡訊、推播通知。"

>[!CONTEXTUALHELP]
>id="ajo_campaigns_create_api_transactional"
>title="行銷活動"
>abstract="向個別輪廓或輪廓集傳遞交易型通訊內容。支援的管道：電子郵件、簡訊、推播通知。"

使用[!DNL Journey Optimizer]行銷活動，跨多個管道將一次性內容傳遞至特定對象。 不同於逐步執行動作的歷程，行銷活動會同時執行動作 — 立即執行或依定義的排程執行。

![](assets/gs-campaigns.png)

## 行銷活動型別

[!DNL Journey Optimizer]支援三種行銷活動型別。 每種型別適合不同的使用案例，並支援不同的管道。

![](assets/campaign-modal.png)

>[!BEGINTABS]

>[!TAB 協調的行銷活動]

**協調的行銷活動**&#x200B;可跨通路提供複雜且品牌啟動的行銷活動，協助您大規模提高參與度、營收和客戶忠誠度。

雖然跨頻道行銷至關重要，但協調的行銷活動可使其順暢無礙。透過視覺化的拖放介面，您可以跨多個頻道設計和自動化複雜的行銷工作流程，從細分到訊息傳遞。所有事情都在單個直觀環境中進行，專為速度、控制能力和效率而打造。

➡️ [瞭解如何使用協調的行銷活動](../orchestrated/gs-orchestrated-campaigns.md)。

>[!TAB 動作行銷活動（或排程的行銷活動）]

**動作行銷活動** （也稱為排程行銷活動）允許簡單的隨機批次通訊。

* **已排程 — 行銷** — 針對行銷使用案例，例如促銷優惠、參與行銷活動、公告、法律通知或原則更新。 需要收件者選擇加入。
* **已排程 — 異動** — 不像行銷活動，異動活動不需要收件者選擇加入。 此類別用於與中斷、緊急情況、取消相關的通訊。 支援的管道：電子郵件、簡訊、推播通知。

➡️ [瞭解如何使用動作行銷活動](create-campaign.md)

>[!TAB 由 API 觸發的行銷活動]

**API觸發的行銷活動**&#x200B;可讓您使用API呼叫觸發行銷活動的執行。 在需要時，這些通訊可以傳送，其中可能不僅涉及使用設定檔屬性（如密碼重設）進行個人化，還涉及觸發程式中的即時內容資料（即REST API裝載）。

* **已觸發API — 行銷** — 傳送個人化行銷通訊給目標對象。
* **已觸發API — 異動** — 在個人執行動作後傳送訊息，例如密碼重設要求、購物車購買等。

➡️ [瞭解如何使用API觸發的行銷活動](api-triggered-campaigns.md)


>[!ENDTABS]

## 依行銷活動型別區分的支援管道 {#channels}

下表顯示不同行銷活動型別中每個管道的可用性，並指出其支援位置。

| Channel | 動作（行銷） | 動作（異動） | API觸發（行銷） | API觸發（異動） | 已協調 |
|----------------------|---------------------|-------------------------|----------------------------|--------------------------------|--------------|
| 電子郵件 | ✅ | ✅ | ✅ | ✅ | ✅ |
| 簡訊 | ✅ | ✅ | ✅ | ✅ | ✅ |
| 推播通知 | ✅ | ✅ | ✅ | ✅ | ✅ |
| 應用程式內 | ✅ | — | — | — | — |
| 直接郵件 | ✅ | — | — | — | — |
| 網頁 | ✅ | — | — | — | — |
| 程式碼型費用 | ✅ | — | — | — | — |
| 內容卡 | ✅ | — | — | — | — |
| WhatsApp | ✅ | — | — | — | — |
| 折線圖 | ✅ | — | — | — | — |

## 先決條件 {#prerequisites}

在使用行銷活動之前，請確定您已檢閱下列必要條件。

* **對象**&#x200B;對象在建立行銷活動之前必須可供使用。 [開始使用客群](../audience/about-audiences.md)。

* **頻道設定** — 若要選取頻道，您必須已建立對應的頻道設定（即預設集）並且可供使用。 [了解如何設定頻道設定](../configuration/channel-surfaces.md)。

* **許可權** — 行銷活動僅適用於具有下列適當許可權的使用者。 如果您無法存取Campaign功能，請聯絡您的管理員以要求必要的許可權。 [瞭解有關 Journey Optimizer 內建角色的詳細資訊](../administration/ootb-product-profiles.md)

  | 行銷活動類型 | 權限 |
  |----------------------------|----------------------------------------------------------------------------|
  | **動作行銷活動** | 行銷活動管理員<br>行銷活動核准者<br>行銷活動管理員<br>行銷活動檢視器 |
  | **由 API 觸發的行銷活動** | 行銷活動管理員<br>行銷活動核准者<br>行銷活動管理員<br>行銷活動檢視器 |
  | **協調的行銷活動** | 協調的行銷活動管理員<br>協調的行銷活動核准者<br>協調的行銷活動管理員<br>協調的行銷活動檢視器 |

  +++了解如何指派行銷活動相關角色

   1. 若要將角色指派給 [!DNL Permissions] 產品中的使用者，請導覽至&#x200B;**[!UICONTROL 角色]**&#x200B;標籤，然後選擇其中一個與上述&#x200B;**[!UICONTROL 角色]**&#x200B;相關的內建行銷活動。

   1. 在&#x200B;**[!UICONTROL 使用者]**&#x200B;標籤中，按一下&#x200B;**[!UICONTROL 新增使用者]**。

   1. 輸入您的使用者名稱或電子郵件地址，或從清單中選取使用者，然後按一下[儲存]。****

      如果之前未建立使用者，請參閱[新增使用者文件](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/access-control/ui/users)。

  接著，使用者應會收到一封電子郵件，並重新導向至您的執行個體。

  +++

## 讓我們深入探討

目前您已瞭解[!DNL Journey Optimizer]中的行銷活動，該是時候深入探討這些文件章節內容，才能開始建立首次行銷活動。

<table style="table-layout:fixed"><tr style="border: 0; text-align: center;">
<td><a href="create-campaign.md"><img width="70%" alt="動作行銷活動" src="assets/do-not-localize/gs-action-campaign.png"></a><br/><a href="create-campaign.md">動作行銷活動</a></td>
<td><a href="api-triggered-campaigns.md"><img width="70%" alt="簡訊" src="assets/do-not-localize/gs-api-triggered-campaign.png"></a><br/><a href="api-triggered-campaigns.md">由 API 觸發的行銷活動</a></td>
<td><a href="../orchestrated/gs-orchestrated-campaigns.md"><img width="70%" alt="推播" src="assets/do-not-localize/gs-orchestrated-campaign.png"></a><a href="../orchestrated/gs-orchestrated-campaigns.md">協調的行銷活動</a></td>
</tr></table>
