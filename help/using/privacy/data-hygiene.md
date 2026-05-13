---
solution: Journey Optimizer
product: journey optimizer
title: 執行資料生命週期作業
description: 瞭解如何執行資料生命週期作業
feature: Privacy, Monitoring
role: User
level: Intermediate
exl-id: 8045b559-bf5e-4b5f-9da4-accd44641a68
TQID: https://experienceleague.adobe.com/-zue9aNrWtfL3MGs7OjH-1CF436mzPh50fsru8OSEq8
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2:
  - id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 235
ht-degree: 100%

---

# 執行資料生命週期作業 {#data-hygiene}

>[!AVAILABILITY]
>
>資料生命週期功能目前僅適用已購買 **Healthcare Shield** 與&#x200B;**隱私權與安全性防護**&#x200B;附加產品的組織。

隨著資料不斷被擷取至 Adobe Experience Platform，請務必確保您的資料能如預期般使用、視需要更新，並根據組織原則刪除。

可以使用&#x200B;**[!UICONTROL 資料生命週期]**&#x200B;選單完成這些任務，該選單可讓您設定並排程資料生命週期作業，確保記錄得到正確維護。

![](assets/data-hygiene.png)


## 建議 {#data-hygiene-recommendations}

當執行資料衛生操作（例如刪除身分或資料集）時，請注意，已刪除身分相關的歷史傳遞事件將不會再出現在標準報表，或是資料湖查詢中。 這可能會導致回報為&#x200B;**已傳遞**&#x200B;的電子郵件數量，也許會和收件者收件匣中&#x200B;**已接收**&#x200B;電子郵件數量之間存在些許差異，尤其對較舊的歷程來說更是如此。

在執行大規模刪除之前，請先驗證並匯出任何必要的傳遞資料，或是報告資料。 如果資料檢疫後仍需要協調，請與 Adobe 支援協調，以便存取已封存記錄，或者使用訊息意見回饋事件資料集查詢，即可取得近期資料。

## 瞭解更多 {#data-hygiene-learn-more}

有關隱私權服務以及如何執行資料生命週期操作的詳細資訊，請參閱 Adobe Experience Platform 文件：

* [Privacy Service 概觀](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=zh-Hant)
* [Adobe Experience Platform 的資料生命週期](https://experienceleague.adobe.com/docs/experience-platform/hygiene/home.html?lang=zh-Hant)
