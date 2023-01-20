---
solution: Journey Optimizer
product: journey optimizer
title: 資料治理
description: 定義連結至標籤和行銷動作的控管政策
feature: Data Governance
topic: Administration
role: Admin
level: Intermediate
keywords: 資料，治理， DULE，標籤，標籤，平台，政策
exl-id: be3efd3b-35d5-4cf7-9015-29d1e305355d
source-git-commit: 16738786e4ebeef3417fd0f6e5be741b348c2744
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 資料治理 {#restrict-fields}


>[!IMPORTANT]
>
>資料使用標籤和執行 (DULE) 的使用目前僅限選定客戶使用，並將在未來版本中部署至所有環境。

透過其資料使用標籤與實作 (DULE) 控管架構，Journey Optimizer 現在可以運用 Adobe Experience Platform 控管政策，防止敏感欄位透過自訂動作匯出至協力廠商系統。 如果系統在自訂動作參數中識別限制欄位，系統會顯示錯誤，使您無法發佈歷程。

Adobe Experience Platform 可讓您為欄位加上標籤，並為每個頻道建立行銷動作。 然後，您會定義連結至標籤和行銷動作的治理政策。

在 Journey Optimizer 中，您可以將這些政策套用至自訂動作，以防止特定欄位匯出至協力廠商系統。

有關資料控管框架以及如何使用標籤和原則的詳細資訊，請參閱 Adobe Experience Platform 文件：

* [資料控管服務總覽](https://experienceleague.adobe.com/docs/experience-platform/data-governance/home.html?lang=zh-Hant)
* [資料使用標籤總覽](https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/overview.html?lang=zh-Hant)
* [資料使用原則](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/overview.html?lang=zh-Hant)

## 重要備註 {#important-notes}

* 資料治理僅適用於歷程中的自訂動作。 不支援 Campaign Classic 和 Campaign Standard 動作。
* 只有在自訂動作層級設定行銷動作 (必要或其他) 時，才適用治理政策。
* 不支援使用現成可用聯集結構的欄位群組所屬的屬性。 這些屬性將從介面中隱藏。 您需要使用不同方案建立其他欄位群組。

## 定義治理政策 {#governance-policies}

您可以使用現有的標籤、行銷動作和政策。 以下是建立新設定的主要步驟：

* 新增標籤，並將標籤套用至您不想匯出至協力廠商系統的特定欄位，例如人員的血液類型。
* 為您歷程中所使用的每個協力廠商自訂動作定義行銷動作。
* 建立治理政策，並將其與標籤和行銷動作建立關聯。

有關如何管理政策的詳細資訊，請參閱本[文件](https://experienceleague.adobe.com/docs/experience-platform/data-governance/policies/user-guide.html?lang=zh-Hant#consent-policy)。

以您需要標示為敏感並限制匯出至協力廠商的血液類型欄位為例。 不同的步驟如下：

1. 在左側選單中的&#x200B;**隱私權**&#x200B;下方，按一下 **政策**。
   ![](assets/action-privacy0.png)
1. 選取&#x200B;**標籤**，按一下&#x200B;**建立標籤**。
   ![](assets/action-privacy1.png)
1. 定義此標籤的名稱和易記名稱。 例如，_ePHI1_。
   ![](assets/action-privacy2.png)
1. 在左側選單中的&#x200B;**資料管理**&#x200B;下方，按一下&#x200B;**方案**，然後按一下&#x200B;**套用存取權和資料治理標籤**&#x200B;按鈕。 選取您的方案和欄位 (血液類型)，然後選取先前建立的標籤，例如範例中的 _ePHI1_。
   ![](assets/action-privacy3.png)
1. 返回&#x200B;**政策**&#x200B;選單，選取&#x200B;**行銷動作**&#x200B;標籤，按一下&#x200B;**建立行銷動作**。建議您針對歷程中所使用的每個協力廠商自訂動作建立一個行銷動作。 例如，建立 _Slack 行銷動作_，其將用於您的 Slack 自訂動作。
   ![](assets/action-privacy4.png)
1. 選取&#x200B;**瀏覽**&#x200B;標籤，按一下&#x200B;**建立政策**&#x200B;並選取&#x200B;**資料治理政策**。選取您的標籤 (_ePHI1_) 和行銷動作 (_Slack 行銷動作_)。
   ![](assets/action-privacy5.png)

當您要在歷程中以 _Slack 行銷動作_&#x200B;使用您的 Slack 自訂動作時，會運用到相關政策。

## 設定自訂動作 {#consent-custom-action}

在左側選單中的&#x200B;**管理**&#x200B;下方，按一下&#x200B;**設定**&#x200B;並選取&#x200B;**動作**。開啟 Slack 自訂動作。 設定自訂動作時，可使用兩個欄位進行資料治理。

![](assets/action-privacy6.png)

* 此&#x200B;**頻道**&#x200B;欄位可讓您選取與此自訂動作相關的頻道：**電子郵件**、**簡訊**，或&#x200B;**推播通知**。它會以所選頻道的預設行銷動作，預先填入&#x200B;**必要的行銷動作**&#x200B;欄位。 如果您選取&#x200B;**其他**，預設情況下不會定義任何行銷動作。 在範例中，我們選取&#x200B;**其他**&#x200B;頻道。

* 此&#x200B;**必要的行銷動作**&#x200B;可讓您定義與自訂動作相關的行銷動作。 例如，如果您使用該自訂動作傳送使用協力廠商的電子郵件，則可選取&#x200B;**電子郵件目標定位**。在範例中，我們選取 _Slack 行銷動作_。系統會擷取並運用與該行銷動作相關聯的治理政策。

[本節](../action/about-custom-action-configuration.md#consent-management)詳細介紹了設定自訂動作的其他步驟。

## 建立歷程 {#consent-journey}

在左側選單中的&#x200B;**歷程管理**&#x200B;下方，按一下&#x200B;**歷程**。建立您的歷程並新增自訂動作。 在歷程中新增自訂動作時，有數個選項可讓您管理資料治理。按一下&#x200B;**顯示唯讀欄位**&#x200B;以顯示所有參數。

此&#x200B;**頻道**&#x200B;與在設定自訂動作時定義的&#x200B;**必要的行銷動作**，會顯示在畫面頂端。 您無法修改這些欄位。

![](assets/action-privacy7.png)

您可以定義&#x200B;**其他行銷動作**&#x200B;來設定自訂動作類型。 這可讓您定義此歷程中自訂動作的用途。 除了必要的行銷動作 (通常是頻道專用的) 之外，您還可以定義其他行銷動作，這些動作為此特定歷程中的自訂動作專用。 例如：運動訓練通訊、電子報、健身通訊等。 所需的行銷動作和其他行銷動作皆適用。

在我們的範例中，我們不使用其他行銷動作。

如果其中一個標示為 _ePHI1_ (我們範例中的血液類型欄位) 的欄位會在動作參數中進行偵測，則顯示錯誤，使您無法發佈歷程。

![](assets/action-privacy8.png)

[本節](../building-journeys/using-custom-actions.md)詳細介紹了在歷程中設定自訂動作的其他步驟。
