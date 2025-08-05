---
solution: Journey Optimizer
product: journey optimizer
title: 排程動作行銷活動
description: 瞭解如何排程行動活動。
feature: Campaigns
topic: Content Management
role: User
level: Beginner
mini-toc-levels: 1
keywords: 建立，最佳化工具，行銷活動，表面，訊息
exl-id: b183eeb8-606f-444d-9302-274f159c3847
source-git-commit: 3a44111345c1627610a6b026d7b19b281c4538d3
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 16%

---

# 排程動作行銷活動 {#action-campaign-schedule}

使用&#x200B;**[!UICONTROL 排程]**&#x200B;索引標籤來定義行銷活動排程。

依預設，動作行銷活動在手動啟動後開始，並在訊息傳送後立即結束。 如果您不想在行銷活動啟動後立即執行，可以使用&#x200B;**[!UICONTROL 行銷活動開始]**&#x200B;選項指定傳送訊息的日期和時間。

**[!UICONTROL 行銷活動end]**&#x200B;選項可讓您指定行銷活動何時應停止執行。 在指定日期以外，將不會執行行銷活動。

![](assets/create-campaign-schedule.png)

>[!NOTE]
>
>在 [!DNL Adobe Journey Optimizer] 中排程行銷活動時，請確定您的開始日期/時間與所要的首次傳遞一致。對於定期行銷活動，如果初始排程時間已過，行銷活動將根據其週期規則滾動至下一個可用時段。

根據行銷活動頻道，提供其他可用排程選項：

* **頻率** （電子郵件、簡訊、推播動作）

  您可以定義行銷活動訊息的傳送頻率。 若要這麼做，請使用行銷活動建立畫面中的&#x200B;**[!UICONTROL 動作觸發器]**&#x200B;選項，指定行銷活動應該每日、每週或每月執行。

* **IP熱身計畫啟用** （電子郵件）

  對於電子郵件行銷活動，您可以建立特定的IP熱身計畫啟用行銷活動。 行銷活動排程將由與其相關聯的IP熱身計畫驅動，這表示行銷活動本身不再定義排程。 [瞭解如何建立IP熱身行銷活動](../configuration/ip-warmup-campaign.md)。

## 後續步驟 {#next}

行銷活動排程準備就緒後，您就可以檢閱並啟動行銷活動。 [了解更多](review-activate-campaign.md)
