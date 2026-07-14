---
solution: Journey Optimizer
product: journey optimizer
title: 時區管理
description: 瞭解時區管理
feature: Journeys, Profiles
topic: Content Management
role: User
level: Intermediate
keywords: 時區，屬性，歷程，條件，時間，日期，自訂
exl-id: 3bcc08d6-1210-4ff9-92f4-edee8285b469
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/PdwGEuWqJcncbkokE0eOhMaEk9L0AmCJ--VZBxxtDDU
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2: id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 996
ht-degree: 8%

---

# 時區管理 {#timezone_management}

>[!BEGINSHADEBOX]

**在此頁面上：**&#x200B;瞭解如何設定歷程的時區（固定時區或從每個設定檔取得的時區），以控制以時間為基礎的活動（例如時間條件、日期條件和自訂等待執行）的時間。

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_journey_properties_time_zone"
>title="歷程時區"
>abstract="時區設定可定義歷程的時區。 當使用固定時區時，對於所有進入歷程的個人來說都是相同的。"


您可以在歷程的[屬性](../building-journeys/journey-properties.md#timezone)中定義時區。

若要存取歷程屬性，請選取畫面右上角的鉛筆圖示。

此時區將用於包含時間元素的歷程的每個活動，例如：

* [時間條件](../building-journeys/conditions.md#time_condition)
* [日期條件](../building-journeys/conditions.md#date_condition)
* [自訂等待](../building-journeys/wait-activity.md#custom)

<!--
* [Fixed date wait](../building-journeys/wait-activity.md#fixed_date)
-->

您可以選取[固定時區](#fixed-timezone)，或選擇使用使用者設定檔](#timezone-from-profiles)中定義的時區[。

## 定義固定時區 {#fixed-timezone}

時區可以固定。 清除預先定義的時區，並從下拉式清單中選取一個時區。 如果您使用固定時區，則所有進入歷程的個人都將使用相同的時區。

若要這麼做，請在&#x200B;**[!UICONTROL 歷程屬性]**&#x200B;窗格中選取時區。

![歷程屬性中的時區選取下拉式清單](assets/journey72.png)

## 使用輪廓時區 {#timezone-from-profiles}

>[!CONTEXTUALHELP]
>id="ajo_journey_properties_profile_time_zone"
>title="使用輪廓時區"
>abstract="此選項可在「**等待**」及「**條件**」活動中使用即時輪廓時區。 如果已經定義輪廓的時區，系統便會取得該時區並在歷程中使用。 若未設定，將使用上面時區欄位中定義的時區。"

如果歷程的進入事件具有名稱空間，這表示歷程可以存取[!DNL Adobe Experience Platform]的即時客戶設定檔服務，您可能會想要使用設定檔層級定義的時區。 若要這麼做，請在&#x200B;**屬性**&#x200B;中勾選&#x200B;**在等待和條件中使用設定檔時區**。 預設不會勾選此選項。

如果為設定檔定義了時區，則會擷取該時區並由歷程使用。 如果沒有，則使用的時區是時區欄位中定義的時區。

![資料來源中的個人化計時設定檔時區設定](assets/journey73.png)

>[!NOTE]
>
>設定檔時區與&#x200B;**偏好設定詳細資料**&#x200B;欄位群組中現有的&#x200B;**時區**&#x200B;欄位搭配使用。

## 在運算式中使用時區 {#timezone-in-expressions}

歷程的開始和結束日期無法連結至特定時區。 它們會自動關聯至執行個體的時區。

+++ AI知識參考

本節包含結構化知識，用於支援與本主題相關的解譯、擷取和問答。

如需完整瞭解，此資訊應結合本頁的檔案。 兩者皆非獨立來源；頁面說明功能，本節提供額外內容，以協助去除術語、意圖、適用性和限制條件的歧義。

* **TL；DR：**&#x200B;本頁說明如何在Adobe Journey Optimizer歷程屬性中設定時區設定，選擇套用至所有設定檔的固定時區，或是從即時客戶設定檔取得的每個設定檔時區。

**意圖：**
* 在歷程上設定固定時區，以便所有設定檔遵循條件和等待的相同時間參考
* 啟用每個設定檔的時區，以便「等待」和「條件」活動使用每個人的儲存時區偏好設定
* 瞭解哪些歷程活動受歷程時區設定影響
* 識別儲存個別時區值的設定檔欄位群組

**字彙表：**
* **固定時區**：在歷程屬性中選取的單一時區，統一套用至進入歷程&#x200B;*（產品特定）*&#x200B;的每個設定檔
* **設定檔時區**：儲存在「偏好設定詳細資料」欄位群組的`timeZone`欄位中的個人時區，當「在等待和條件中使用設定檔時區」選項啟用時使用&#x200B;*（產品特定）*
* **喜好設定詳細資料欄位群組**：包含用於設定檔層級時區解析的`timeZone`屬性的XDM欄位群組

**護欄：**
* 「在等待和條件中使用設定檔時區」選項僅在歷程的進入事件具有名稱空間（即歷程可以到達即時客戶設定檔服務）時可用
* 預設不會核取選項；除非明確啟用，否則會使用固定時區
* 如果已啟用選項，但未在設定檔上定義時區，則歷程會回到歷程屬性中定義的固定時區
* 歷程開始和結束日期無法連結至特定時區；會自動與執行個體的時區相關聯

**術語：**
* 正式名稱：時區管理 — 首字母縮寫：none — 變體：時區設定、歷程時區
* 同義字：「固定時區」=「對所有個人都相同」；「設定檔時區」=「在等待和條件中使用設定檔時區」
* 請勿混淆：「歷程時區」（適用於活動）≠「執行個體時區」（適用於歷程開始/結束日期，會自動設定）

**常見問題集：**
* **問：我可以在哪裡設定歷程的時區？**  — 在「歷程屬性」窗格中，可透過歷程畫布右上角的鉛筆圖示存取。
* **問：哪些活動使用歷程時區？**  — 時間條件、日期條件和自訂等待活動。
* **問：如何讓每個設定檔都遵循自己的當地時區？**  — 在歷程屬性中，啟用「在等待和條件中使用設定檔時區」選項。 這要求歷程具有名稱空間，才能存取即時客戶個人檔案服務。
* **問：如果設定檔未定義時區，而且已啟用設定檔時區選項，會發生什麼情況？**  — 歷程會回到歷程屬性時區欄位中定義的固定時區。
* **問：哪個設定檔欄位儲存個人的時區？**  — 設定檔結構描述中「偏好設定詳細資料」欄位群組內的`timeZone`欄位。
* **問：我可以將歷程的開始和結束日期設為特定時區嗎？**  — 否。 歷程開始和結束日期會自動與執行個體的時區相關聯，且無法連結至自訂時區。

+++
