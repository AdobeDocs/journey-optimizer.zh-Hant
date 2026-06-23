---
solution: Journey Optimizer
product: journey optimizer
title: Adobe Campaign Standard 動作
description: 瞭解Adobe Campaign Standard動作
feature: Journeys, Actions, Custom Actions
topic: Administration
role: User
level: Intermediate
keywords: 歷程，整合， standard，行銷活動， ACS
exl-id: 50565cd9-7415-4c6a-9651-24fefeded3f5
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/spxxZT-JH5yzziL8-oSkJdBcKEppm-4ZzeLC2-laCaM
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: c2beecbb-b93e-4ae3-baa9-72adcdc06781
  - id: d8353d85-5da7-453d-bd68-40ad33fa0ab7
  - id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1484
ht-degree: 5%

---

# [!DNL Adobe Campaign] Standard 動作 {#using_campaign_action}

>[!BEGINSHADEBOX]

**在此頁面上：**&#x200B;瞭解如何仰賴Adobe Campaign Standard異動訊息範本，在歷程中使用內建的Campaign Standard電子郵件、推播和簡訊動作活動。

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_journey_action_custom_acs"
>title="自訂動作"
>abstract="如果您有 [!DNL Adobe Campaign] Standard，則可整合。 這可讓您使用 [!DNL Adobe Campaign] 交易型訊息功能傳送電子郵件、推播通知及簡訊。"

如果您有[!DNL Adobe Campaign] Standard，則可使用下列內建動作活動： **[!UICONTROL 電子郵件]**、**[!UICONTROL 推播]**&#x200B;和&#x200B;**[!UICONTROL 簡訊]**。

>[!NOTE]
>
>為此，您需要設定內建動作。 請參見[此頁面](../action/acs-action.md)。

針對這些管道中的每一個，您選取[!DNL Adobe Campaign]標準異動訊息&#x200B;**範本**。 對於內建電子郵件、簡訊和推播頻道，我們仰賴「交易式傳訊」來執行訊息傳送。 這表示如果您想在歷程中使用特定訊息範本，則必須以[!DNL Adobe Campaign] Standard發佈。 請參閱[此頁面](https://experienceleague.adobe.com/docs/campaign-standard/using/communication-channels/transactional-messaging/getting-started-with-transactional-msg.html?lang=zh-Hant)以瞭解如何使用此功能。

>[!NOTE]
>
>必須發佈Campaign Standard交易式訊息及其相關事件，才能在Journey Optimizer中使用。 如果事件已發佈，但訊息尚未發佈，將無法在Journey Optimizer介面中看見。 如果訊息已發佈，但其關聯事件尚未發佈，則會顯示在Journey Optimizer介面中，但將無法使用。

![[!DNL Adobe Campaign]歷程中的標準動作設定](assets/journey59.png)

您可以使用事件（也稱為即時）或設定檔交易式訊息範本。

>[!NOTE]
>
>當我們傳送即時異動訊息(rtEvent)或因自訂動作而透過協力廠商系統路由訊息時，疲勞、封鎖清單或取消訂閱管理需要特定設定。 例如，如果「unsubscribe」屬性儲存在[!DNL Adobe Experience Platform]或協力廠商系統中，則必須在傳送訊息之前新增條件，以檢查此條件。

當您選取範本時，訊息裝載中預期的所有欄位都會顯示在活動設定窗格的&#x200B;**[!UICONTROL 位址]**&#x200B;和&#x200B;**[!UICONTROL Personalization資料]**&#x200B;下。 您需要將每個欄位與您要使用的欄位相對應，無論是從事件還是從資料來源進行。 您也可以使用進階運算式編輯器以手動方式傳遞值、對擷取的資訊執行資料操作（例如將字串轉換為大寫）或使用函式，例如「if， then， else」。 請參閱[此頁面](expression/expressionadvanced.md)。

![Campaign Standard訊息範本選取介面](assets/journey60.png)

## 電子郵件和簡訊 {#section_asc_51g_nhb}

對於&#x200B;**[!UICONTROL 電子郵件]**&#x200B;和&#x200B;**[!UICONTROL 簡訊]**，引數相同。

>[!NOTE]
>
>針對電子郵件使用設定檔的交易式範本時，[!DNL Adobe Campaign] Standard會自動處理取消訂閱機制。
>在[交易式電子郵件範本](https://experienceleague.adobe.com/docs/campaign-standard/using/communication-channels/transactional-messaging/getting-started-with-transactional-msg.html?lang=zh-Hant)中包含&#x200B;**[!UICONTROL 取消訂閱連結]**&#x200B;內容區塊。
>如果您使用以事件為基礎的範本(rtEvent)，請在訊息中納入連結，將收件者的電子郵件當作URL引數傳遞，並將它們導向取消訂閱登入頁面。
>建立登入頁面，並確保收件者的取消訂閱決定已傳輸至Adobe。

首先，您需要選擇異動訊息範本。

有兩個類別可供使用： **[!UICONTROL 位址]**&#x200B;和&#x200B;**[!UICONTROL Personalization資料]**。

您可以使用介面輕鬆定義在何處擷取&#x200B;**[!UICONTROL 位址]**&#x200B;或&#x200B;**[!UICONTROL Personalization資料]**。 您可以瀏覽事件和可用資料來源的欄位。 您也可以將進階運算式編輯器用於更進階的使用案例，例如使用需要傳遞引數或執行操作的資料來源。 請參閱[此頁面](expression/expressionadvanced.md)。

**[!UICONTROL 位址]**

>[!NOTE]
>
>此類別只有在您選取「事件」交易式訊息時才會顯示。 對於「設定檔」訊息，系統會自動從[!DNL Adobe Campaign] Standard擷取&#x200B;**[!UICONTROL 位址]**&#x200B;欄位。

這些是系統需要知道將訊息傳送到何處的欄位。 如果是電子郵件範本，則為電子郵件地址。 如果是簡訊，則為行動電話號碼。

用於Campaign Standard整合的![訊息引數設定](assets/journey61.png)

**[!UICONTROL Personalization資料]**

>[!NOTE]
>
>您無法在個人化資料中傳遞集合。 如果交易式電子郵件或簡訊需要集合，則無法運作。 另請注意，個人化資料採用預期格式（例如：字串、小數等）。 您必須注意遵守這些預期的格式。

這些是[!DNL Adobe Campaign]標準訊息預期的欄位。 這些欄位可用於個人化訊息、套用條件式格式或挑選特定訊息變體。

![Journey Optimizer與Campaign Standard之間的欄位對應](assets/journey62.png)

## 推播 {#section_im3_hvf_nhb}

在使用推播活動之前，您的行動應用程式需要與Campaign Standard一起設定以傳送推播通知。 使用此[文章](https://helpx.adobe.com/tw/campaign/kb/integrate-mobile-sdk.html)針對行動裝置採取必要的實作步驟。

首先，您需要從下拉式清單中選擇行動應用程式和交易式訊息。

適用於Campaign Standard引數對應的進階運算式編輯器![](assets/journey62bis.png)

有兩個類別可供使用： **[!UICONTROL Target]**&#x200B;和&#x200B;**[!UICONTROL Personalization資料]**。

**[!UICONTROL Target]**

>[!NOTE]
>
>只有在選取事件訊息時，才會顯示此類別。 對於設定檔訊息，系統使用[!DNL Adobe Campaign] Standard所執行的調解，自動擷取&#x200B;**[!UICONTROL 目標]**&#x200B;欄位。

在此區段中，您必須定義&#x200B;**[!UICONTROL 推播平台]**。 下拉式清單可讓您選取&#x200B;**[!UICONTROL Apple推播通知伺服器]** (iOS)或&#x200B;**[!UICONTROL Firebase雲端訊息]** (Android)。 或者，您可以從事件或資料來源選取特定欄位，或定義進階運算式。

您也需要定義&#x200B;**[!UICONTROL 註冊權杖]**。 運算式取決於在事件裝載或其他[!DNL Journey Optimizer]資訊中定義權杖的方式。 如果代號是在執行個體的集合中定義，則它可以是簡單欄位或更複雜的運算式：

```
@event{Event_push._experience.campaign.message.profileSnapshot.pushNotificationTokens.first().token}
```

**[!UICONTROL Personalization資料]**

>[!NOTE]
>
>您無法在個人化資料中傳遞集合。 如果交易式推播需要集合，則無法運作。 另請注意，個人化資料採用預期格式（例如：字串、小數等）。 您必須注意遵守這些預期的格式。

這些是[!DNL Adobe Campaign]標準訊息中使用的交易式範本預期的欄位。 這些欄位可用於個人化您的訊息、套用條件式格式，或挑選特定的訊息變體。

+++ AI知識參考

本節包含結構化知識，用於支援與本主題相關的解譯、擷取和問答。

如需完整瞭解，此資訊應結合本頁的檔案。 兩者皆非獨立來源；頁面說明功能，本節提供額外內容，以協助去除術語、意圖、適用性和限制條件的歧義。

* **TL；DR：**&#x200B;此頁面說明如何透過Campaign異動訊息範本，在Journey Optimizer歷程中使用內建的Adobe Campaign Standard電子郵件、簡訊和推播動作活動。

**意圖：**

* 使用Adobe Campaign Standard整合設定歷程中的電子郵件、簡訊或推播動作活動
* 選擇並將Campaign Standard交易式訊息範本對應到歷程欄位
* 將歷程事件或資料來源中的地址和Personalization資料欄位對應到訊息裝載
* 處理事件和設定檔異動電子郵件範本的取消訂閱
* 設定Campaign Standard推播動作的推播通知目標平台和註冊權杖

**字彙表：**

* **異動訊息**： Adobe Campaign Standard根據事件&#x200B;*（產品特定）*&#x200B;傳送觸發的即時訊息（電子郵件、簡訊、推播）的功能
* **rtEvent**： Adobe Campaign Standard中的即時事件交易式訊息範本，用於事件型訊息&#x200B;*（產品特定）*
* **設定檔交易式範本**：使用設定檔資料進行收件者解析和取消訂閱處理&#x200B;*（產品特定）*&#x200B;的Campaign Standard交易式訊息範本
* **註冊Token**：將推播通知定位至特定行動應用程式安裝&#x200B;*（產品特定）*&#x200B;所需的裝置層級識別碼

**護欄：**

* 內建動作必須在使用前進行設定；請參閱動作設定頁面。
* 必須發佈Campaign Standard交易式訊息及其相關事件，範本才能在Journey Optimizer中使用。
* 無法在Personalization資料欄位中傳遞集合。
* 對於事件型(rtEvent)範本，在傳送之前必須以條件手動處理取消訂閱管理。
* 若為設定檔推送訊息，系統會自動擷取「目標」欄位，「目標」類別僅會顯示在事件訊息中。
* 必須先使用Campaign Standard設定行動應用程式，才能使用推播活動。

**術語：**

* 正式名稱：Adobe Campaign Standard — 首字母縮寫：ACS — 變體：Campaign Standard
* 同義字：&quot;event transactional message&quot; = &quot;rtEvent&quot;；&quot;real-time transactional message&quot; = &quot;rtEvent&quot;
* 請勿混淆：「設定檔交易式範本」（自動處理取消訂閱）≠「事件交易式範本」（必須手動處理取消訂閱）

**常見問題集：**

* **問：透過Adobe Campaign Standard整合可以使用哪些管道？**  — 電子郵件、簡訊和推播通知通道可作為內建動作活動使用。
* **問：在Journey Optimizer中使用交易式訊息之前，是否需要在Campaign Standard中發佈該訊息？**  — 是，交易式訊息及其相關事件都必須發佈；未發佈的訊息將無法使用，即使顯示在介面中亦然。
* **問：設定檔電子郵件範本的取消訂閱處理方式為何？**  — 使用設定檔交易式範本時，Adobe Campaign Standard會自動處理取消訂閱；在範本中納入取消訂閱連結內容區塊。
* **問：我可以將集合傳遞為個人化資料嗎？**  — 否，無法在Personalization資料中傳遞集合；交易式訊息不能預期集合。
* **問：我應將事件型電子郵件的收件者地址對應到何處？**  — 活動設定窗格中的位址類別僅對事件交易式訊息可見；對於設定檔訊息，會自動擷取位址。

+++
