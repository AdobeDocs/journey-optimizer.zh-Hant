---
solution: Journey Optimizer
product: journey optimizer
title: 設定自訂動作
description: 瞭解如何設定自訂動作
feature: Journeys, Actions, Custom Actions
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Experienced
keywords: 動作，協力廠商，自訂，歷程， API
exl-id: 4df2fc7c-85cb-410a-a31f-1bc1ece237bb
source-git-commit: 12423d9fe07e5c757154ae4f732ff20ec6dc2427
workflow-type: tm+mt
source-wordcount: '1799'
ht-degree: 17%

---

# 設定自訂動作 {#configure-an-action}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_custom_configuration"
>title="自訂動作"
>abstract="如果您使用協力廠商系統來傳送訊息，或想要歷程傳送 API 呼叫至協力廠商系統，請使用自訂動作來設定系統至您歷程的連線。例如，您可使用自訂動作連線至下列系統：Epsilon、Slack、[Adobe Developer](https://developer.adobe.com)、Firebase 等等。"

如果您使用協力廠商系統來傳送訊息，或想要歷程傳送 API 呼叫至協力廠商系統，請使用自訂動作來設定系統至您歷程的連線。例如，您可以使用自訂動作連線到下列系統：Epsilon、Slack、 [Adobe Developer](https://developer.adobe.com){target="_blank"}、Firebase等

自訂動作是技術使用者定義的其他動作，可供行銷人員使用。 設定後，其會顯示在您歷程的左側浮動視窗中，位於 **[!UICONTROL 動作]** 類別。 在[本頁](../building-journeys/about-journey-activities.md#action-activities)中瞭解更多。

## 限制{#custom-actions-limitations}

自訂動作隨附下列幾項限制 [此頁面](../start/guardrails.md).

在自訂動作引數中，您可以傳遞簡單集合以及物件集合。 進一步瞭解中的集合限制 [此頁面](../building-journeys/collections.md#limitations).

另請注意，自訂動作引數採用預期格式（例如：字串、小數等）。 您必須注意遵守這些預期的格式。 在本節瞭解更多 [使用案例](../building-journeys/collections.md).

自訂動作僅在使用時支援JSON格式 [請求](../action/about-custom-action-configuration.md#define-the-message-parameters) 或 [回應裝載](../action/action-response.md).

## 最佳作法{#custom-action-enhancements-best-practices}

使用自訂動作選擇要作為目標的端點時，請確定：

* 此端點可使用來自[節流 API](../configuration/throttling.md) 或[設定 API 上限](../configuration/capping.md)的設定來支援歷程的輸送量，藉此加以限制。 請留意，節流設定不可低於 200 TPS。任何目標端點至少需要支援 200 TPS。
* 此端點的回應時間必須儘可能縮短。 根據預期輸送量，高回應時間可能會影響實際輸送量。

所有自訂動作皆已定義1分鐘上300,000次呼叫的上限。 此外，預設上限會針對每個主機和每個沙箱執行。 例如，在沙箱上，如果您有主機相同的兩個端點 (例如：`https://www.adobe.com/endpoint1` 和 `https://www.adobe.com/endpoint2`)，此上限會套用至 adobe.com 主機下的所有端點。 「endpoint1」和「endpoint2」會共用相同的上限設定，而且讓一個端點達到限制會影響到另一個端點。

此限制是根據客戶使用情況來設定，可保護自訂動作鎖定為目標的外部端點。您需要定義適當的讀取率 (使用自訂動作時為每秒 5000 個設定檔)，以在對象歷程中將其列入考量。 如有需要，您可以透過上限/節流 API 定義較高的上限或節流限制來覆寫此設定。 請參閱[此頁面](../configuration/external-systems.md)。

基於以下各種原因，您不應使用自訂動作來鎖定公用端點：

* 如果沒有適當的上限或節流，可能會傳送過多呼叫至可能不支援此磁碟區的公用端點。
* 設定檔資料可透過自訂動作傳送，因此定位公用端點可能會導致無意間在外部共用個人資訊。
* 您無法控制公用端點傳回的資料。 如果端點變更其API或開始傳送不正確的資訊，這些資訊將可在傳送的通訊中使用，並可能產生負面影響。

## 同意與資料控管 {#privacy}

在Journey Optimizer中，您可以將資料控管和同意原則套用至自訂動作，以防止特定欄位匯出至協力廠商系統，或排除尚未同意接收電子郵件、推播或簡訊通訊的客戶。 如需詳細資訊，請參閱下列頁面：

* [資料控管](../action/action-privacy.md).
* [同意](../action/action-privacy.md).


## 設定步驟 {#configuration-steps}

以下是設定自訂動作所需的主要步驟：

1. 在「管理」功能表區段中，選取 **[!UICONTROL 設定]**. 在  **[!UICONTROL 動作]** 區段，按一下 **[!UICONTROL 管理]**. 按一下 **[!UICONTROL 建立動作]** 以建立新動作。 動作設定窗格會在畫面右側開啟。

   ![](assets/custom2.png)

1. 輸入動作的名稱。

   >[!NOTE]
   >
   >只允許使用英數字元和底線。 長度上限為30個字元。

1. 新增說明至您的動作。 此步驟為選填。
1. 使用此動作的歷程次數會顯示在 **[!UICONTROL 使用位置]** 欄位。 您可以按一下 **[!UICONTROL 檢視歷程]** 按鈕來顯示使用此動作的歷程清單。
1. 定義不同的 **[!UICONTROL URL設定]** 引數。 請參閱[此頁面](../action/about-custom-action-configuration.md#url-configuration)。
1. 設定 **[!UICONTROL 驗證]** 區段。 此設定與資料來源的設定相同。  請參閱[本節](../datasource/external-data-sources.md#custom-authentication-mode)。
1. 定義 **[!UICONTROL 動作引數]**. 請參閱[此頁面](../action/about-custom-action-configuration.md#define-the-message-parameters)。
1. 按一下&#x200B;**[!UICONTROL 儲存]**。

   自訂動作現已設定完畢，且可供您在歷程中使用。 請參閱[此頁面](../building-journeys/about-journey-activities.md#action-activities)。

   >[!NOTE]
   >
   >當歷程中使用自訂動作時，大部分引數均為唯讀。 您只能修改 **[!UICONTROL 名稱]**， **[!UICONTROL 說明]**， **[!UICONTROL URL]** 欄位和 **[!UICONTROL 驗證]** 區段。

## 端點設定 {#url-configuration}

設定自訂動作時，您需要定義下列專案 **[!UICONTROL 端點設定]** 引數：

![](assets/action-response1bis.png){width="70%" align="left"}

1. 在 **[!UICONTROL URL]** 欄位，指定外部服務的URL：

   * 如果URL是靜態的，請在此欄位中輸入URL。

   * 如果URL包含動態路徑，請只輸入URL的靜態部分，也就是配置、主機、連線埠，以及（選擇性）路徑的靜態部分。

     範例：`https://xxx.yyy.com/somethingstatic/`

     將自訂動作新增至歷程時，您將指定URL的動態路徑。 [了解更多](../building-journeys/using-custom-actions.md)。

   >[!NOTE]
   >
   >基於安全考量，我們強烈建議您針對URL使用HTTPS配置。 我們不允許使用非公開的Adobe位址和IP位址。
   >
   >定義自訂動作時只允許預設連線埠：80用於http，443用於https。

1. 選取通話 **[!UICONTROL 方法]**：它可以 **[!UICONTROL POST]**， **[!UICONTROL GET]** 或 **[!UICONTROL PUT]**.

   >[!NOTE]
   >
   > 此 **DELETE** 方法不受支援。 如果您需要更新現有資源，請選取 **PUT** 方法。

1. 定義標頭和查詢引數：

   * 在 **[!UICONTROL 標頭]** 區段，按一下 **[!UICONTROL 新增標題欄位]** 定義要傳送給外部服務之要求訊息的HTTP標頭。 此 **[!UICONTROL Content-Type]** 和 **[!UICONTROL 字元集]** 標頭欄位預設為設定。 您無法刪除這些欄位。 僅限 **[!UICONTROL Content-Type]** 標頭可以修改。 其值應符合JSON格式。 以下是預設值：

   ![](assets/content-type-header.png)

   * 在 **[!UICONTROL 查詢引數]** 區段，按一下 **[!UICONTROL 新增查詢引數欄位]** 以定義您要新增至URL的引數。

   ![](assets/journeyurlconfiguration2bis.png)

1. 輸入欄位的標籤或名稱。

1. 選取型別： **[!UICONTROL 常數]** 或 **[!UICONTROL 變數]**. 如果您已選取 **[!UICONTROL 常數]**，然後輸入中的常數值 **[!UICONTROL 值]** 欄位。 如果您已選取 **[!UICONTROL 變數]**，則您會在將自訂動作新增至歷程時指定此變數。 [了解更多](../building-journeys/using-custom-actions.md)。

   ![](assets/journeyurlconfiguration2.png)

   >[!NOTE]
   >
   >將自訂動作新增至歷程後，如果歷程處於草稿狀態，您仍可新增標題或查詢引數欄位至歷程。 如果您不希望歷程受設定變更影響，請複製自訂動作，並將欄位新增到新的自訂動作。
   >
   >標頭會根據欄位剖析規則進行驗證。 進一步瞭解 [本檔案](https://tools.ietf.org/html/rfc7230#section-3.2.4){_blank}.

## 定義裝載引數 {#define-the-message-parameters}

1. 在 **[!UICONTROL 請求]** 區段，貼上要傳送至外部服務的JSON裝載範例。 此欄位是選用欄位，僅適用於POST和PUT呼叫方法。

1. 在 **[!UICONTROL 回應]** 區段，貼上呼叫傳回之裝載的範例。 此欄位是選用欄位，可用於所有呼叫方法。 如需如何在自訂動作中運用API呼叫回應的詳細資訊，請參閱 [此頁面](../action/action-response.md).

>[!NOTE]
>
>回應功能目前在Beta版中提供。

![](assets/action-response2bis.png){width="70%" align="left"}

>[!NOTE]
>
>裝載範例不可包含Null值。 承載中的欄位名稱不得包含「。」 設定的 Cookie。開頭不能為「$」字元。

您將能夠定義引數型別（例如：字串、整數等）。

您也可以選擇指定引數是常數還是變數：

* **常數** 表示引數的值是由技術角色在動作設定窗格中定義。 值在歷程中一律相同。 這不會改變，且行銷人員在歷程中使用自訂動作時不會看到。 例如，它可能是協力廠商系統期望的ID。 在這種情況下，切換常數/變數右側的欄位是傳遞的值。
* **變數** 表示引數的值會有所不同。 在歷程中使用此自訂動作的行銷人員可自由傳遞所需值，或指定從何處擷取此引數的值(例如從事件、Adobe Experience Platform等)。 在這種情況下，切換常數/變數右側的欄位是行銷人員將在歷程中看到的標籤，以命名此引數。

![](assets/customactionpayloadmessage2.png)

## mTLS通訊協定支援 {#mtls-protocol-support}

您現在可以使用相互傳輸層安全性(mTLS)，確保對HTTP API目的地和Adobe Journey Optimizer自訂動作的輸出連線具有增強的安全性。 mTLS是一種用於相互驗證的端對端安全性方法，可確保共用資訊的雙方在共用資料之前，都是聲稱的身分。 mTLS包括相較於TLS的額外步驟，其中伺服器也會要求使用者端的憑證並在其末端驗證它。

在Adobe Journey Optimizer中，mTLS會與自訂動作搭配使用。 您不需額外設定Adobe Journey Optimizer自訂動作，即可啟用mTLS。 當自訂動作的端點啟用mTLS時，系統會從Adobe Experience Platform金鑰存放區擷取憑證，並自動將其提供給端點（這是mTLS連線的必要）。

如果您想要將mTLS與這些Adobe Journey Optimizer和Experience PlatformHTTP API目標工作流程搭配使用，您放入Adobe Journey Optimizer客戶動作UI或目標UI的伺服器位址必須停用TLS通訊協定，並且僅啟用mTLS。 如果仍在端點上啟用TLS 1.2通訊協定，則不會傳送使用者端驗證的憑證。 這表示若要搭配這些工作流程使用mTLS，您的「接收」伺服器端點必須是mTLS **僅限** 已啟用連線端點。

>[!IMPORTANT]
>
>您的Adobe Journey Optimizer自訂動作或歷程中不需要額外設定，即可啟用mTLS；當偵測到啟用mTLS的端點時，此程式會自動發生。 每個憑證的一般名稱(CN)和主體替代名稱(SAN)都可在檔案中作為憑證的一部分提供，如果您希望這樣做，還可以用作其他所有權驗證層。
>
>RFC 2818於2000年5月發行，它不建議在HTTPS憑證中使用一般名稱(CN)欄位來進行主體名稱驗證。 它建議改用「dns名稱」型別的「主體替代名稱」延伸模組(SAN)。

如果您要檢查CN或SAN以進行其他協力廠商驗證，可以在這裡下載相關憑證：

```
Prod:
{
    "serviceName": "AJO Journeys",
    "publicCertificate": "-----BEGIN CERTIFICATE-----
MIIG9TCCBd2gAwIBAgIQBX+pDP5hB0gqDzFKyq5wLjANBgkqhkiG9w0BAQsFADBZ
MQswCQYDVQQGEwJVUzEVMBMGA1UEChMMRGlnaUNlcnQgSW5jMTMwMQYDVQQDEypE
aWdpQ2VydCBHbG9iYWwgRzIgVExTIFJTQSBTSEEyNTYgMjAyMCBDQTEwHhcNMjQw
NTA5MDAwMDAwWhcNMjUwNjA5MjM1OTU5WjB0MQswCQYDVQQGEwJVUzETMBEGA1UE
CBMKQ2FsaWZvcm5pYTERMA8GA1UEBxMIU2FuIEpvc2UxEzARBgNVBAoTCkFkb2Jl
IEluYy4xKDAmBgNVBAMTH2Fqby1qb3VybmV5cy5hZXAtbXRscy5hZG9iZS5jb20w
ggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQDaI8HZHzbmPEgTy9O7cYmq
ZVX5283Gw7j7v4/O810jZXItBDmsSiWotvTgAT0s2oZMZZ6tGPbQB7hL+xJJ+yu2
HxFl1WzB4UGHJ+UbrL94hI930xQs0FVgSOGgIarj5HucF2ZxwHIkVHY5whrOq9t4
UxFBG0siUPQrTzV9GfA0wREElugpTbwaM8CTWwOQ9ekroOD2C5zAcLTycXFtSMiU
B4L4u38S9hGoBByzzKv9GnUMQudvt/s5zsGykZgEEYeN6IitfVO6BOD9jT94Aytx
/O3XH5w8v4KNTn+An99bXFmyg3JRUFSYZFxha8s1f6uu0XbdToQ+ao0WkE06nMmV
AgMBAAGjggOcMIIDmDAfBgNVHSMEGDAWgBR0hYDAZsffN97PvSk3qgMdvu3NFzAd
BgNVHQ4EFgQUn8OqtzccNdrsb+fbRnTHmtTZxLMwKgYDVR0RBCMwIYIfYWpvLWpv
dXJuZXlzLmFlcC1tdGxzLmFkb2JlLmNvbTA+BgNVHSAENzA1MDMGBmeBDAECAjAp
MCcGCCsGAQUFBwIBFhtodHRwOi8vd3d3LmRpZ2ljZXJ0LmNvbS9DUFMwDgYDVR0P
AQH/BAQDAgWgMB0GA1UdJQQWMBQGCCsGAQUFBwMBBggrBgEFBQcDAjCBnwYDVR0f
BIGXMIGUMEigRqBEhkJodHRwOi8vY3JsMy5kaWdpY2VydC5jb20vRGlnaUNlcnRH
bG9iYWxHMlRMU1JTQVNIQTI1NjIwMjBDQTEtMS5jcmwwSKBGoESGQmh0dHA6Ly9j
cmw0LmRpZ2ljZXJ0LmNvbS9EaWdpQ2VydEdsb2JhbEcyVExTUlNBU0hBMjU2MjAy
MENBMS0xLmNybDCBhwYIKwYBBQUHAQEEezB5MCQGCCsGAQUFBzABhhhodHRwOi8v
b2NzcC5kaWdpY2VydC5jb20wUQYIKwYBBQUHMAKGRWh0dHA6Ly9jYWNlcnRzLmRp
Z2ljZXJ0LmNvbS9EaWdpQ2VydEdsb2JhbEcyVExTUlNBU0hBMjU2MjAyMENBMS0x
LmNydDAMBgNVHRMBAf8EAjAAMIIBfwYKKwYBBAHWeQIEAgSCAW8EggFrAWkAdwBO
daMnXJoQwzhbbNTfP1LrHfDgjhuNacCx+mSxYpo53wAAAY9ecsWsAAAEAwBIMEYC
IQDQclgq89ZVlwdYBJFEIs8q4WIcZ9Siw+jb9OgCrz+wjwIhALQLnC1WyT+dHjvY
FvZjc99WkjnEwhIevj/Rz7r0EzhmAHUAfVkeEuF4KnscYWd8Xv340IdcFKBOlZ65
Ay/ZDowuebgAAAGPXnLF5AAABAMARjBEAiBy9cNT3CnmSMOdJe+JbG8f7ha1UGgN
TdDlaR9x9fKmKQIgNmGjz5AzP1evB2G1TTvVLkHfWQw0864c4F23WSV+6TsAdwDP
EVbu1S58r/OHW9lpLpvpGnFnSrAX7KwB0lt3zsw7CAAAAY9ecsYnAAAEAwBIMEYC
IQCTcB7s1xDP8Olif3jj4X8jHgVxv5C3bTvG6wDYBByfcQIhAOt8PhR6tWSLtF1V
HB8r7dns7Oth1+QT7WMonQZsP/3WMA0GCSqGSIb3DQEBCwUAA4IBAQAjTy45fbQV
aVTZ71wcIyHnkJfq/8SSc/UNT5//6AMiV6kb3YsFW1+EaQ1wPHZS0Qfjs7aIsXi5
f2TCGps8onELNpOfFfptrOCMfcYGMvV1wPCBy+kuoGY/YRZlsdNUTTzQAGztfRev
79w+XIDzioCrY+sfyUkkw+N/F7/RIjzMKjP6onSfuD+5WjqVKq9kFE0fCyJixedV
BPoPM4Cktgvc9SsK17JmLWkg+V2yH1eDzmjF3sR0/dcmoAM0qgV/CDuhIIqX2o7m
3/aQSNsPUpgBVbkz+SjEtchmw8DXW/Kro8QVulsXdbkiLTOj4JopxdOzrbKgWMwr
pIw7KKJoktDk
-----END CERTIFICATE-----
-----BEGIN CERTIFICATE-----
MIIEyDCCA7CgAwIBAgIQDPW9BitWAvR6uFAsI8zwZjANBgkqhkiG9w0BAQsFADBh
MQswCQYDVQQGEwJVUzEVMBMGA1UEChMMRGlnaUNlcnQgSW5jMRkwFwYDVQQLExB3
d3cuZGlnaWNlcnQuY29tMSAwHgYDVQQDExdEaWdpQ2VydCBHbG9iYWwgUm9vdCBH
MjAeFw0yMTAzMzAwMDAwMDBaFw0zMTAzMjkyMzU5NTlaMFkxCzAJBgNVBAYTAlVT
MRUwEwYDVQQKEwxEaWdpQ2VydCBJbmMxMzAxBgNVBAMTKkRpZ2lDZXJ0IEdsb2Jh
bCBHMiBUTFMgUlNBIFNIQTI1NiAyMDIwIENBMTCCASIwDQYJKoZIhvcNAQEBBQAD
ggEPADCCAQoCggEBAMz3EGJPprtjb+2QUlbFbSd7ehJWivH0+dbn4Y+9lavyYEEV
cNsSAPonCrVXOFt9slGTcZUOakGUWzUb+nv6u8W+JDD+Vu/E832X4xT1FE3LpxDy
FuqrIvAxIhFhaZAmunjZlx/jfWardUSVc8is/+9dCopZQ+GssjoP80j812s3wWPc
3kbW20X+fSP9kOhRBx5Ro1/tSUZUfyyIxfQTnJcVPAPooTncaQwywa8WV0yUR0J8
osicfebUTVSvQpmowQTCd5zWSOTOEeAqgJnwQ3DPP3Zr0UxJqyRewg2C/Uaoq2yT
zGJSQnWS+Jr6Xl6ysGHlHx+5fwmY6D36g39HaaECAwEAAaOCAYIwggF+MBIGA1Ud
EwEB/wQIMAYBAf8CAQAwHQYDVR0OBBYEFHSFgMBmx9833s+9KTeqAx2+7c0XMB8G
A1UdIwQYMBaAFE4iVCAYlebjbuYP+vq5Eu0GF485MA4GA1UdDwEB/wQEAwIBhjAd
BgNVHSUEFjAUBggrBgEFBQcDAQYIKwYBBQUHAwIwdgYIKwYBBQUHAQEEajBoMCQG
CCsGAQUFBzABhhhodHRwOi8vb2NzcC5kaWdpY2VydC5jb20wQAYIKwYBBQUHMAKG
NGh0dHA6Ly9jYWNlcnRzLmRpZ2ljZXJ0LmNvbS9EaWdpQ2VydEdsb2JhbFJvb3RH
Mi5jcnQwQgYDVR0fBDswOTA3oDWgM4YxaHR0cDovL2NybDMuZGlnaWNlcnQuY29t
L0RpZ2lDZXJ0R2xvYmFsUm9vdEcyLmNybDA9BgNVHSAENjA0MAsGCWCGSAGG/WwC
ATAHBgVngQwBATAIBgZngQwBAgEwCAYGZ4EMAQICMAgGBmeBDAECAzANBgkqhkiG
9w0BAQsFAAOCAQEAkPFwyyiXaZd8dP3A+iZ7U6utzWX9upwGnIrXWkOH7U1MVl+t
wcW1BSAuWdH/SvWgKtiwla3JLko716f2b4gp/DA/JIS7w7d7kwcsr4drdjPtAFVS
slme5LnQ89/nD/7d+MS5EHKBCQRfz5eeLjJ1js+aWNJXMX43AYGyZm0pGrFmCW3R
bpD0ufovARTFXFZkAdl9h6g4U5+LXUZtXMYnhIHUfoyMo5tS58aI7Dd8KvvwVVo4
chDYABPPTHPbqjc1qCmBaZx2vN4Ye5DUys/vZwP9BFohFrH/6j/f3IL16/RZkiMN
JCqVJUzKoZHm1Lesh3Sz8W2jmdv51b2EQJ8HmA==
-----END CERTIFICATE-----
-----BEGIN CERTIFICATE-----
MIIDjjCCAnagAwIBAgIQAzrx5qcRqaC7KGSxHQn65TANBgkqhkiG9w0BAQsFADBh
MQswCQYDVQQGEwJVUzEVMBMGA1UEChMMRGlnaUNlcnQgSW5jMRkwFwYDVQQLExB3
d3cuZGlnaWNlcnQuY29tMSAwHgYDVQQDExdEaWdpQ2VydCBHbG9iYWwgUm9vdCBH
MjAeFw0xMzA4MDExMjAwMDBaFw0zODAxMTUxMjAwMDBaMGExCzAJBgNVBAYTAlVT
MRUwEwYDVQQKEwxEaWdpQ2VydCBJbmMxGTAXBgNVBAsTEHd3dy5kaWdpY2VydC5j
b20xIDAeBgNVBAMTF0RpZ2lDZXJ0IEdsb2JhbCBSb290IEcyMIIBIjANBgkqhkiG
9w0BAQEFAAOCAQ8AMIIBCgKCAQEAuzfNNNx7a8myaJCtSnX/RrohCgiN9RlUyfuI
2/Ou8jqJkTx65qsGGmvPrC3oXgkkRLpimn7Wo6h+4FR1IAWsULecYxpsMNzaHxmx
1x7e/dfgy5SDN67sH0NO3Xss0r0upS/kqbitOtSZpLYl6ZtrAGCSYP9PIUkY92eQ
q2EGnI/yuum06ZIya7XzV+hdG82MHauVBJVJ8zUtluNJbd134/tJS7SsVQepj5Wz
tCO7TG1F8PapspUwtP1MVYwnSlcUfIKdzXOS0xZKBgyMUNGPHgm+F6HmIcr9g+UQ
vIOlCsRnKPZzFBQ9RnbDhxSJITRNrw9FDKZJobq7nMWxM4MphQIDAQABo0IwQDAP
BgNVHRMBAf8EBTADAQH/MA4GA1UdDwEB/wQEAwIBhjAdBgNVHQ4EFgQUTiJUIBiV
5uNu5g/6+rkS7QYXjzkwDQYJKoZIhvcNAQELBQADggEBAGBnKJRvDkhj6zHd6mcY
1Yl9PMWLSn/pvtsrF9+wX3N3KjITOYFnQoQj8kVnNeyIv/iPsGEMNKSuIEyExtv4
NeF22d+mQrvHRAiGfzZ0JFrabA0UWTW98kndth/Jsw1HKj2ZL7tcu7XUIOGZX1NG
Fdtom/DzMNU+MeKNhJ7jitralj41E6Vf8PlwUHBHQRFXGU7Aj64GxJUTFy8bJZ91
8rGOmaFvE7FBcf6IKshPECBV1/MUReXgRPTqh5Uykw7+U0b6LJ3/iyK5S9kJRaTe
pLiaWN0bfVKfjllDiIGknibVb63dDcY3fe0Dkhvld1927jyNxF1WW6LZZm6zNTfl
MrY=
-----END CERTIFICATE-----",
    "expiryDate": "2025-06-09T23:59:59Z"
}
```

