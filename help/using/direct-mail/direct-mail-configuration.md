---
title: 直接郵件設定
description: 瞭解如何在Journey Optimizer中設定直接郵件頻道
feature: Direct Mail, Surface
topic: Content Management
role: User
level: Experienced
keyword: direct, mail, configuration, direct-mail, provider
exl-id: ae5cc885-ade1-4683-b97e-eda1f2142041
source-git-commit: 2f7c620a712cfc104418bc985bd74e81da12147c
workflow-type: tm+mt
source-wordcount: '1364'
ht-degree: 22%

---

# 直接郵件設定 {#direct-mail-configuration}

[!DNL Journey Optimizer]可讓您個人化並產生直接郵件供應商傳送郵件給您的客戶所需的檔案。

當[建立直接郵件訊息](../direct-mail/create-direct-mail.md)時，您可以定義目標對象資料，包括所選的連絡資訊（例如郵寄地址）。 然後，包含此資料的檔案會自動產生並匯出至伺服器，您的直接郵件提供者將能夠擷取該檔案，並處理實際傳送。

在能夠產生此檔案之前，您需要建立：

1. [檔案路由組態](#file-routing-configuration)，指定檔案匯出的伺服器，並視需要加密檔案。

1. [參考檔案路由設定的直接郵件設定](#direct-mail-configuration)。 如果您尚未設定任何檔案路由選項，您將無法建立直接郵件設定。


>[!CAUTION]
>
>* 若要建立檔案路由設定，您必須擁有&#x200B;**[!DNL Manage file routing]**&#x200B;內建許可權。 [了解更多](../administration/ootb-product-profiles.md#content-library-manager)
>
>* 直接郵件檔案只會在匯出時產生；系統不會無限期儲存較舊的匯出專案。 如需更長或永久的備份，請設定檔案路由選項（SFTP或雲端儲存空間）。

## 設定檔案路由 {#file-routing-configuration}

>[!CONTEXTUALHELP]
>id="ajo_dm_file_routing_details"
>title="定義檔案路由設定"
>abstract="建立直接郵件訊息後，會產生包含目標客群資料的檔案並將其匯出到伺服器。您需要指定伺服器的詳細資訊，以便您的直接郵件提供者可以存取和使用該檔案來傳遞直接郵件。"
>additional-url="https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer/using/channels/direct-mail/create-direct-mail" text="建立新的直接郵件訊息"

>[!CONTEXTUALHELP]
>id="ajo_dm_file_routing_details_header"
>title="定義檔案路由設定"
>abstract="您需要定義將檔案匯出到何處以供直接郵件提供者使用。"

>[!CONTEXTUALHELP]
>id="ajo_dm_select_file_routing"
>title="檔案路由設定"
>abstract="選取您選擇的檔案路由設定，這會定義將檔案匯出到何處以供您的直接郵件提供者使用。"

>[!CONTEXTUALHELP]
>id="ajo_dm_file_routing_type"
>title="選取您的檔案的伺服器類型"
>abstract="選擇匯出直接郵件檔案所要使用的伺服器類型：Amazon S3、SFTP、Azure 或資料著陸區域。"

>[!CONTEXTUALHELP]
>id="ajo_dm_file_routing_aws_region"
>title="選擇 AWS 區域"
>abstract="選取要將直接郵件檔案匯出到哪個 AWS 伺服器的地理區域。一般做法是，最好選擇離您的直接郵件提供者所在位置最近的區域。"

>[!NOTE]
>
>目前[!DNL Journey Optimizer]支援Amazon S3、SFTP、Azure和資料登陸區域。

為了傳遞直接郵件訊息，[!DNL Journey Optimizer]會產生包含目標對象資料的檔案，並將其匯出至伺服器。

您必須指定伺服器詳細資料，以便直接郵件提供者可以存取及使用該檔案來傳遞郵件。

若要設定檔案路由，請遵循下列步驟。

1. 存取&#x200B;**[!UICONTROL 管理]** > **[!UICONTROL 管道]** > **[!UICONTROL 直接郵件設定]** > **[!UICONTROL 檔案路由]**&#x200B;功能表，然後按一下&#x200B;**[!UICONTROL 建立檔案路由設定]**。

   ![](assets/file-routing-config-button.png){width="800" align="center"}

1. 設定組態的名稱。

1. 選取您要用於匯出直接郵件檔案的伺服器型別：Amazon S3、SFTP、Azure或資料登陸區域。

   ![](assets/file-routing-config-type.png){width="800" align="center"}

1. 請填入每種伺服器型別的特定欄位，如以下標籤所詳述。

>[!BEGINTABS]

>[!TAB Amazon S3]

如果您選取&#x200B;**[!UICONTROL Amazon S3]**&#x200B;做為&#x200B;**[!UICONTROL 伺服器型別]**，請填入伺服器的詳細資料和認證：

* **AWS bucket名稱**:To&#x200B;知道在何處尋找您的AWS bucket名稱，請參閱[此頁面](https://docs.aws.amazon.com/AmazonS3/latest/userguide/UsingBucket.html)。

* **AWS存取金鑰**：若要瞭解在何處尋找您的AWS存取金鑰ID，請參閱[此頁面](https://docs.aws.amazon.com/IAM/latest/UserGuide/security-creds.html#access-keys-and-secret-access-keys)。

* **AWS秘密金鑰**：若要瞭解在何處尋找您的AWS秘密金鑰，請參閱[此頁面](https://aws.amazon.com/fr/blogs/security/wheres-my-secret-access-key/)。

* **AWS區域**：選擇伺服器基礎結構將位於的&#x200B;**[!UICONTROL AWS區域]**。 AWS區域是AWS用來託管其雲端基礎結構的地理區域。 一般而言，建議您選擇距離直接郵件提供者位置最近的區域。

![](assets/file-routing-config-aws-region.png){width="800" align="center"}

>[!TAB SFTP]

如果您選取&#x200B;**[!UICONTROL SFTP]**&#x200B;做為&#x200B;**[!UICONTROL 伺服器型別]**，請填入伺服器的詳細資料和認證：

* **[!UICONTROL 驗證型別]**：選取用來連線到伺服器的驗證型別（密碼或SSH金鑰）。

* **[!UICONTROL 帳戶]**：用來連線至SFTP伺服器的帳戶名稱。

* **[!UICONTROL 伺服器位址]**： &#x200B;SFTP伺服器的URL。

* **[!UICONTROL 連線埠]**： SFTP連線連線埠號碼。

* **[!UICONTROL 密碼]** / **[!UICONTROL SSH金鑰]**： &#x200B;用來連線至SFTP伺服器的密碼或SSH金鑰。

![](assets/file-routing-config-sftp-detail.png)

>[!NOTE]
>
>若要指定伺服器上儲存檔案的路徑，請更新直接郵件促銷活動的&#x200B;**[!UICONTROL 檔案名稱]**&#x200B;欄位，以包含所要的路徑。 [了解更多](create-direct-mail.md#extraction-file)

>[!TAB Azure]

如果您選取&#x200B;**[!UICONTROL Azure]**&#x200B;做為&#x200B;**[!UICONTROL 伺服器型別]**，請填入伺服器的詳細資料和認證：

* **Azure連線字串**：若要尋找您的&#x200B;**Azure連線字串**，請參閱[此頁面](https://learn.microsoft.com/en-us/azure/storage/common/storage-configure-connection-string#configure-a-connection-string-for-an-azure-storage-account)。

  **Azure連線字串**&#x200B;應遵循以下格式：

  `DefaultEndpointsProtocol=[http|https];AccountName=myAccountName;AccountKey=myAccountKey`

* **容器名稱**：若要尋找您的&#x200B;**容器名稱**，請參閱[此頁面](https://learn.microsoft.com/en-us/azure/storage/blobs/blob-containers-portal)。

  **容器名稱**&#x200B;應僅包含容器名稱，不含任何斜線。

  >[!NOTE]
  >
  >若要指定容器內的路徑以儲存檔案，請更新直接郵件促銷活動的&#x200B;**[!UICONTROL 檔案名稱]**&#x200B;欄位，以包含所要的路徑。 [了解更多](create-direct-mail.md#extraction-file)

  ![](assets/file-routing-config-azure-detail.png)

>[!TAB 資料登陸區域]

如果您選取&#x200B;**[!UICONTROL 資料登陸區域]**&#x200B;做為&#x200B;**[!UICONTROL 伺服器型別]**，則不需要特定的詳細資料。

![](assets/file-routing-config-dlz-detail.png)

[!DNL Adobe Experience Platform]的所有客戶都已為每個沙箱布建一個資料登陸區域容器。 在[Adobe Experience Platform檔案](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/sources/connectors/cloud-storage/data-landing-zone){target="_blank"}中進一步瞭解資料登陸區域。

>[!ENDTABS]

若要加密檔案，請在&#x200B;**[!UICONTROL PGP/GPG加密金鑰]**&#x200B;欄位中複製並貼上您的加密金鑰。

填寫伺服器型別的詳細資料後，請選取&#x200B;**[!UICONTROL 提交]**。 檔案路由設定是以&#x200B;**[!UICONTROL 作用中]**&#x200B;狀態建立的。 現在已準備好用於[直接郵件組態](#direct-mail-surface)。

您也可以選取&#x200B;**[!UICONTROL 另存為草稿]**&#x200B;以建立檔案路由組態，但您無法在組態中選取它，直到它是&#x200B;**[!UICONTROL 作用中]**&#x200B;為止。

## 建立直接郵件設定 {#direct-mail-surface}

>[!CONTEXTUALHELP]
>id="ajo_dm_surface_settings"
>title="定義直接郵件設定"
>abstract="直接郵件設定包含檔案格式的設定；該檔案包含目標對象資料，且將由郵件提供者使用。您也必須選取檔案路由設定，以定義該檔案匯出的位置。"
>additional-url="https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer/using/channels/direct-mail/direct-mail-configuration#file-routing-configuration" text="設定檔案路由"

<!--
>[!CONTEXTUALHELP]
>id="ajo_dm_surface_sort"
>title="Define the sort order"
>abstract="If you select this option, the sort will be by profile ID, ascending or descending. If you unselect it, the sorting configuration defined when creating the direct mail message within a journey or a campaign."-->

>[!CONTEXTUALHELP]
>id="ajo_dm_surface_split"
>title="定義檔案分割臨界值"
>abstract="您必須為包含對象資料的每個檔案設定最大記錄數。您可以選取 1 到 200,000 筆記錄之間的任一數字。達到指定的臨界值後，將為剩餘記錄建立另一個檔案。"

若要能夠透過[!DNL Journey Optimizer]傳遞直接郵件，您必須建立通道設定，以定義郵件提供者將使用的檔案格式設定。

直接郵件設定也必須包含檔案路由設定，該設定會定義將匯出直接郵件檔案的伺服器。

1. 在左側邊欄中，瀏覽至&#x200B;**[!UICONTROL 管理]** > **[!UICONTROL 管道]**&#x200B;並選取&#x200B;**[!UICONTROL 一般設定]** > **[!UICONTROL 管道設定]**。 按一下&#x200B;**[!UICONTROL 建立通道組態]**&#x200B;按鈕。 [了解更多](../configuration/channel-surfaces.md)

   ![](assets/direct-mail-config-1.png)

1. 輸入設定的名稱和說明（選擇性），然後選取要設定的通道。

   >[!NOTE]
   >
   > 名稱必須以字母(A-Z)開頭。 它只能包含英數字元。 您也可以使用底線 `_`、點 `.` 和連字號 `-` 字元。

1. 若要將自訂或核心資料使用標籤指派給組態，您可以選取&#x200B;**[!UICONTROL 管理存取權]**。 [進一步瞭解物件層級存取控制(OLAC)](../administration/object-based-access.md)。

1. 選取&#x200B;**[!UICONTROL 直接郵件]**&#x200B;頻道。

   ![](assets/direct-mail-config-2.png)

1. 選取&#x200B;**[!UICONTROL 行銷動作]**，以使用此設定將同意原則與訊息相關聯。 系統會運用與行銷動作相關的所有同意政策，以尊重客戶的偏好設定。 [了解更多](../action/consent.md#surface-marketing-actions)

1. 在通道設定的專用區段中定義直接郵件設定。

   ![](assets/surface-direct-mail-settings.png){width="800" align="center"}

   <!--![](assets/surface-direct-mail-settings-with-insertion.png)-->

1. 選取檔案格式： **[!UICONTROL CSV]**&#x200B;或&#x200B;**[!UICONTROL 文字分隔]**。

1. 如果您選取&#x200B;**[!UICONTROL 文字分隔]**，請定義您選擇的欄分隔符號：製表、分號、垂直號或&amp;符號。

   ![](assets/surface-direct-mail-column-separator.png)

1. 選取您建立的&#x200B;**[!UICONTROL 檔案路由設定]**。 這會定義檔案將匯出至何處以供直接郵件提供者使用。

   >[!CAUTION]
   >
   >如果您尚未設定任何檔案路由選項，您將無法建立直接郵件設定。 [了解更多](#file-routing-configuration)

   ![](assets/surface-direct-mail-file-routing.png){width="800" align="center"}

   <!--![](assets/surface-direct-mail-file-routing-with-insertion.png)-->

1. 提交直接郵件設定。

您現在可以在行銷活動中[建立直接郵件訊息](../direct-mail/create-direct-mail.md)。 行銷活動開始後，包含目標對象資料的檔案會自動匯出至您定義的伺服器。 然後，直接郵件提供者將能夠擷取該檔案，並繼續直接郵件傳送。

>[!NOTE]
>
>資料列中所有值都相同的重複資料列，會自動從檔案中移除。

<!--
    In the **[!UICONTROL Insertion]** section, you can choose to automatically remove duplicate rows.

    Define the maximum number of records (i.e. rows) for each file containing profile data. After the specified threshold is reached, another file will be created for the remaining records.

    ![](assets/surface-direct-mail-split.png)

    For example, if there are 100,000 records in the file and the threshold limit is set to 60,000, the records will be split into two files. The first file will contain 60,000 rows, and the second file will contain the remaining 40,000 rows.

    >[!NOTE]
    >
    >NOTE You can set any number between 1 and 200,000 records, meaning each file must contain at least 1 row and no more than 200,000 rows.

-->