---
solution: Journey Optimizer
product: journey optimizer
title: 加快傳遞速度
description: 瞭解如何加快傳遞速度
feature: Journeys, Use Cases, IP Warmup Plans
topic: Content Management
role: User, Developer
level: Intermediate, Experienced
hide: true
keywords: 可遞送性，歷程，使用案例，電子郵件，聲譽
exl-id: 83d1b68d-011a-4109-b5f0-6ca1ade2944d
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/en0jMw69ddHSQrIH05-9FfGuDwNKb36f5Lp3fLp2oAk
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: df64005d-8f9a-422e-ba4d-c6f6dc3454b4
subfeature_v2:
  - id: d8353d85-5da7-453d-bd68-40ad33fa0ab7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
source-git-commit: b5d14f7b40933f110ff666db858e976e5de711db
workflow-type: tm+mt
source-wordcount: 807
ht-degree: 2%

---

# 使用案例：加快傳遞速度{#use-case-ramp-up-your-deliveries}

>[!BEGINSHADEBOX]

**在此頁面上：**&#x200B;瞭解如何使用「最佳化」活動與設定檔上限，建立逐步加快電子郵件傳送的歷程，協助您熱身新的IP位址並建立您的寄件者信譽。

>[!ENDSHADEBOX]

如果您最近移至其他電子郵件服務提供者、IP位址或電子郵件網域或子網域，您必須建立您作為寄件者的信譽。 否則，您的傳遞可能會遭到封鎖或移至收件者信箱的垃圾郵件資料夾。 在[傳遞能力最佳實務指南](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/generic-resources/increase-reputation-with-ip-warming.html?lang=zh-Hant){target="_blank"}中瞭解如何利用IP暖身提高您的電子郵件信譽。

若要熱身IP，您可以逐步增加傳遞數量。 深入瞭解[在Journey Optimizer](../reports/deliverability.md)中最佳化傳遞能力。

此使用案例的目的是建立歷程，以加快電子郵件傳遞速度。 若要設定此歷程，請遵循下列步驟：

1. 建立歷程。 [閱讀全文](journey-gs.md)。

1. 將&#x200B;**[!UICONTROL 最佳化]**&#x200B;活動新增至歷程。 [閱讀全文](optimize.md)。

1. 在&#x200B;**[!UICONTROL 條件]**&#x200B;活動設定中，設定傳遞的收件者數目上限：

   1. 在&#x200B;**[!UICONTROL 最佳化]**&#x200B;活動設定中，選取&#x200B;**[!UICONTROL 條件]**&#x200B;方法，並將&#x200B;**[!UICONTROL 型別]**&#x200B;欄位設定為&#x200B;**[!UICONTROL 設定檔上限]**。 [閱讀全文](conditions.md#profile_cap)。

   1. 將&#x200B;**[!UICONTROL 限制]**&#x200B;欄位設定為此傳遞的收件者數目上限。

   ![控制傳遞磁碟區的設定檔上限條件設定](assets/profile-cap-condition.png)

   您可以逐漸提高此限制，最多可達您的訂閱者總數。

1. 在&#x200B;**[!UICONTROL 條件]**&#x200B;活動之後，將&#x200B;**[!UICONTROL 電子郵件]**&#x200B;動作活動新增至名義路徑。

   ![斜向傳遞歷程中的電子郵件訊息設定](assets/ramp-up-deliveries-message.png)

   當歷程執行時，會傳送訊息給輸入的設定檔，最多為您指定的設定檔數量上限。 當達到此限制時，輸入的設定檔會採用替代路徑。

1. 使用您選擇的活動完成歷程。

IP啟動後，您就可以移除此條件。

+++ AI知識參考

本節包含結構化知識，用於支援與本主題相關的解譯、擷取和問答。

如需完整瞭解，此資訊應結合本頁的檔案。 兩者皆非獨立來源；頁面說明功能，本節提供額外內容，以協助去除術語、意圖、適用性和限制條件的歧義。

- **TL；DR：**&#x200B;此使用案例說明如何建立Adobe Journey Optimizer歷程，該歷程使用設定檔上限條件逐漸增加電子郵件傳遞量，以在IP預熱期間保護寄件者信譽。

**意圖：**
- 建立歷程，逐步增加IP暖體的電子郵件傳送量
- 設定設定檔上限條件，以限制每次傳遞執行的收件者人數
- 切換至新的電子郵件服務提供者、IP位址或網域時，保護寄件者信譽
- 當IP完全暖機後，請移除磁碟區上限條件

**字彙表：**
- **IP預熱**：從新IP位址或網域逐漸增加電子郵件傳送量的程式，以建立與信箱提供者&#x200B;*（產品特定）*&#x200B;的寄件者信譽
- **設定檔上限**： Optimize活動中的條件型別，可限制在指定歷程執行&#x200B;*（產品特定）*&#x200B;中接收訊息的設定檔數目上限
- **最佳化活動**：歷程畫布活動，用於套用條件、目標定位規則或實驗，以控制設定檔如何流經歷程&#x200B;*（產品特定）*

**護欄：**
- 設定檔上限條件必須在最佳化活動的條件方法中設定，以控制傳送量。
- 超過上限的設定檔會採用歷程中定義的替代路徑。
- 設定檔上限應隨時間逐漸增加，最多可增加訂閱者總數。

**術語：**
- 正式名稱：Rampup deliveries — 縮寫：none — 變體：IP warming、IP warmup、delivery rampup
- 同義字： &quot;IP warming&quot; = &quot;IP warmup&quot; = &quot;sender prespondence building&quot;
- 請勿混淆：「設定檔上限」≠「對象大小限制」（設定檔上限是每次執行的傳送限制；對象大小是合格的設定檔總數）

**常見問題集：**
- **問：為何切換至新IP或網域時，需要加快傳遞速度？**  — 新的IP或網域沒有傳送記錄，因此信箱提供者可能會封鎖或垃圾郵件資料夾訊息，直到透過逐漸增加容量建立良好的信譽為止。
- **問：設定檔上限條件如何控制傳遞量？**  — 它會設定可在單一歷程執行中接收訊息的設定檔數目上限；超過該限制的設定檔會改用替代路徑。
- **問：何時可以移除設定檔上限條件？**  — 當IP完全啟動並建立您的傳送者信譽後，您就可以從歷程中移除條件。
- **問：我可以隨著時間逐漸增加上限嗎？**  — 是；您可以更新設定檔上限條件中的限制欄位，以逐步增加每次執行的收件者數目，直到您的完整訂閱者計數為止。

+++
