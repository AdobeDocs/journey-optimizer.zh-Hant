---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer中的訊息匯出
description: 瞭解如何匯出訊息
feature: Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: 匯出，訊息， HIPAA，電子郵件，簡訊，設定
badge: label="有限可用性" type="Informative"
hide: true
hidefromtoc: true
exl-id: 7b50c933-9738-4b1b-acae-08f0a8d41dab
source-git-commit: 8bc0d28ea3e7c26bd8f7a35d00a73e41f35720d0
workflow-type: tm+mt
source-wordcount: '513'
ht-degree: 8%

---

# 匯出訊息內容 {#message-export}

>[!CONTEXTUALHELP]
>id="ajo_admin_msg_export"
>title="保留並匯出您已傳送的內容"
>abstract="選取此選項可讓您使用此設定，將已傳送的電子郵件或簡訊訊息內容寫入 [!DNL Experience Platform] 資料集。記錄會自內嵌後保留7個日曆日，在此期間，您可以將記錄匯出至您自己的儲存空間。"

>[!AVAILABILITY]
>
>此功能目前僅適用於一組組織（可用性限制）。 如需詳細資訊，請聯絡您的 Adobe 代表。

**訊息匯出**&#x200B;可讓您透過[!DNL Journey Optimizer]目的地，將已傳送的電子郵件和簡訊內容從[!DNL Adobe Experience Platform]傳輸到您自己的儲存空間，這些目的地可讓您將資料從[!DNL Experience Platform]傳送到外部端點。 [了解更多](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/destinations/home){target="_blank"}

透過此功能，透過[!DNL Journey Optimizer]傳送且標示為要匯出的電子郵件和簡訊內容會寫入[!DNL Experience Platform] **AJO訊息匯出資料集**。

然後，記錄會保留在&#x200B;**AJO訊息匯出資料集**&#x200B;中，從內嵌到七天之後，您就可以將它們匯出到您選擇的外部系統。
<!--
## Terminology

* **[!DNL Experience Platform] destinations** - Framework to deliver data out of Experience Platform into external endpoints. [Learn more](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/home){target="_blank"}
* **AJO Message Export Dataset** - An [!DNL Experience Platform] dataset which stores the message content of email and SMS messages sent via [!DNL Journey Optimizer] which have been marked for export.
* **Retention**: Records in the AJO Message Export Dataset are retained for 3 calendar days from ingestion.-->

## 護欄

* 此功能僅支援電子郵件和簡訊頻道。
* AJO訊息匯出資料集中的記錄會在擷取後保留七天。
* 在啟用訊息匯出之前，不支援對已傳送的訊息使用回填，如下所述。

## 啟用訊息匯出 {#enable-message-export}

訊息匯出功能的上線流程包含兩個步驟：

1. [在](#set-up-export-dataflow)中設定匯出資料流[!DNL Experience Platform]；
1. 在[的頻道設定中](#config-message-export)啟用訊息匯出[!DNL Journey Optimizer]。

>[!WARNING]
>
>只有啟用匯出和傳送訊息後才會顯示新記錄。 不支援在設定匯出程式及啟用匯出訊息選項之前回填內容。

### 設定匯出資料流 {#set-up-export-dataflow}

您必須先定義[!DNL Experience Platform]目的地和將要使用的資料集，以設定匯出程式，才能匯出您的資料。 請遵循下列步驟。

>[!NOTE]
>
>必須針對每個沙箱設定此設定。

1. 選擇Experience Platform [目的地型別](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/destination-types){target="_blank"}。 [此頁面](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/overview){target="_blank"}上有準備好接收資料的可用目的地平台清單。

1. 在[!DNL Experience Platform]中，定義認證、貯體/容器、路徑首碼和安全性選項來設定您的目的地。 [了解作法](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/ui/activate/export-datasets){target="_blank"}

1. 使用下列資料建立資料集匯出流程：

   * Source資料集：選取&#x200B;**AJO訊息匯出資料集**。
   * 檔案格式：選取JSON或Parquet （根據下游工具選擇一個格式）。
   * 排程：確保在7天的保留期間內執行。

### 在通道設定中啟用訊息匯出 {#config-message-export}

若要將訊息匯出套用至您的行銷活動和歷程，您必須在頻道設定層級啟用專用選項。 請遵循下列步驟。

1. 在[!DNL Journey Optimizer]中，編輯或建立所需的電子郵件或簡訊[頻道設定](channel-surfaces.md#create-channel-surface)。

1. 選取&#x200B;**[!UICONTROL 啟用郵件匯出]**&#x200B;選項。

   ![](assets/config-message-export.png)

1. 儲存您的變更並提交您的頻道設定。

使用此頻道設定而透過行銷活動或歷程傳送的電子郵件和簡訊訊息，會寫入&#x200B;**AJO訊息匯出資料集**。 接著，系統會根據您定義的匯出資料流，將記錄匯出至選取的儲存體目的地。

停用&#x200B;**[!UICONTROL 啟用訊息匯出]**&#x200B;切換會停止將此頻道組態的新記錄擷取到資料集中。 現有記錄會一直保留，直到保留到期為止。
