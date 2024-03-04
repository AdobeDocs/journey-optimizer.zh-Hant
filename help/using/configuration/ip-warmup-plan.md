---
solution: Journey Optimizer
product: journey optimizer
title: 建立 IP 暖身計劃
description: 瞭解如何在Journey Optimizer中建立IP熱身計畫
feature: IP Warmup Plans
topic: Administration
role: Admin
level: Experienced
keywords: IP、群組、子網域、傳遞能力
hide: true
hidefromtoc: true
badge: label="Beta"
exl-id: c2434086-2ed4-4cd0-aecd-2eea8f0a55f6
source-git-commit: e8a178ea337fb57f2c2460c9e3e53257787c7bfd
workflow-type: tm+mt
source-wordcount: '1576'
ht-degree: 8%

---

# 建立 IP 暖身計劃 {#ip-warmup}

>[!BEGINSHADEBOX]

本文件指南會提供以下內容：

* [開始使用IP熱身](ip-warmup-gs.md)
* [建立 IP 暖身行銷活動](ip-warmup-campaign.md)
* **[建立IP熱身計畫](ip-warmup-plan.md)**
* [執行 IP 暖身計劃](ip-warmup-execution.md)

>[!ENDSHADEBOX]

建立一或多個 [IP熱身行銷活動](ip-warmup-campaign.md) 啟用專用表面並啟用對應的選項後，您就可以開始建立IP熱身計畫。

若要存取、建立、編輯和刪除IP熱身計畫，您必須擁有 **[!UICONTROL 傳遞能力顧問]** 角色或IP熱身計畫相關許可權。

+++瞭解如何指派「傳遞能力顧問」角色或IP熱身計畫相關許可權

將對應許可權指派給特定 **[!UICONTROL 角色]**：

1. 從 [!DNL Permissions] 產品，導覽至 **[!UICONTROL 角色]** 功能表，並選取您要使用新設定的角色 **[!UICONTROL IP熱身設定]** 許可權。

1. 從您的 **[!UICONTROL 角色]** 儀表板，按一下 **[!UICONTROL 編輯]**.

   ![](assets/ip_permissions_1.png)

1. 拖放 **[!UICONTROL IP熱身設定]** 指派許可權的資源。

1. 從 **[!UICONTROL IP熱身設定]** 資源下拉式清單，選取您的使用者需要哪些許可權。

   ![](assets/ip_permissions_2.png)

1. 按一下&#x200B;**[!UICONTROL 儲存]**。

將對應角色指派給 **[!UICONTROL 使用者]**：

1. 從 [!DNL Permissions] 產品，導覽至 **[!UICONTROL 角色]** 功能表並選取 **[!UICONTROL 傳遞能力顧問]** 內建角色。

1. 從您的 **[!UICONTROL 角色]** 儀表板，存取 **[!UICONTROL 使用者]** 標籤。

   ![](assets/ip_permissions_3.png)

1. 按一下 **[!UICONTROL 新增使用者]** 以指派 **[!UICONTROL 傳遞能力顧問]** 內建角色。

   ![](assets/ip_permissions_4.png)

1. 選取您的 **[!UICONTROL 使用者]** 並按一下 **[!UICONTROL 儲存]**.

   ![](assets/ip_permissions_5.png)

+++

## 準備 IP 暖身計畫檔案 {#prepare-file}

IP熱身是一項活動，包括逐漸增加從您的IP和網域傳送到主要網際網路服務提供者(ISP)的電子郵件數量，以建立您作為合法傳送者的聲譽。

此活動通常在傳遞能力專家的協助下執行，該專家會根據產業網域、使用案例、地區、ISP和各種其他因素，協助您準備完善的計畫。

<!--When working with the [!DNL Journey Optimizer] IP warmup feature, this plan takes the form of an Excel file that must contain a number of predefined columns.-->

在中建立IP熱身計畫之前 [!DNL Journey Optimizer] 介面，您必須在Excel範本中填入所有可為計畫提供摘要的資料。

* 您可以從使用者介面下載空白Excel [IP熱身計畫範本](assets/IPWarmupPlan-Template.xlsx) 以填入。

* 您也可以下載 [IP熱身計畫範例](assets/IPWarmupPlan-Sample.xlsx) 已填入一些您可當作範例的資料。

<!--
* From the user interface you can download the blank Excel IP warmup plan template to fill in.

* You can also download a sample IP warmup plan already filled in with some data you can use as an example.
-->

>[!CAUTION]
>
>請與您的傳遞顧問合作，確認您的IP熱身計畫檔案設定正確。
>
>請務必使用範本中提供的格式。

以下是包含IP熱身計畫的檔案範例。

![](assets/ip-warmup-sample-file.png)

>[!NOTE]
>
>目前，您應將 **屬性** 和 **值** 未接觸的儲存格。

### IP熱身計畫標籤 {#ip-warmup-plan-tab}

* 在此範例中，已準備超過17天的計畫(稱為&#39;**執行**『)來達到超過一百萬個設定檔的目標數量。

* 此計畫會透過六個步驟執行 **階段**，每個檔案至少包含一個回合。

* 您可以對要傳送至的網域擁有任意數目的欄。 在此範例中，計劃分為六個欄：

   * 其中四個對應至 **現成可用的網域群組** 用於您的計畫(Gmail、Microsoft、Yahoo和Orange)。
   * 其中一個對應至自訂網域群組(您需要使用 [自訂網域群組](#custom-domain-group-tab) 標籤)。
   * 第六欄， **其他**，包含計畫未明確涵蓋之其他網域的所有剩餘位址。 此欄是選用的：如果省略，電子郵件將只傳送到指定的網域。
* 此 **參與天數** 欄會顯示僅鎖定在輸入的最後一個期間與您的品牌互動的設定檔。

我們的想法是逐步增加每個執行中的目標位址數量，同時減少每個階段的執行數量。

以下列出您可以新增到計畫中的現成主要網域群組：

<!--
* Gmail
* Adobe
* WP
* Comcast
* Yahoo
* Bigpond
* Orange
* Softbank
* Docomo
* United Internet
* Microsoft
* KDDI
* Italia Online
* La Poste
* Apple
-->

+++ Gmail gmail.com；google.com；googlemail.com；googlemail.co.uk
+++

+++WP wp.pl；o2.pl
+++

+++康卡斯特comcast.net
+++

+++Yahoo aol.fi；games.com；cs.com；yahoo.com.in；y7mail.com；yahoo.co.uk；yahoo.hu；yahoo.co.hu；yahoo.cn；yahoogroups.com.sg；yahoogroups.com.au；aol.es；yahoo.com.au yahoo.com.vn aol.co.nz yahoo.com.br yahoo.ne.jp ymail.com netscape.com yahoo.com.pe yahoo.co.id citlink.net wmconnect.com yahoo.com.jp yahoo.com.hk aol.com.br yahoo.co.kr yahoo.com.ar ygm.com yahoo.co.nz aol.com goowy.com rocketmail.com frontiernet.net aim.com yahoogroups.co.in netscape.net luckymail.com yahoo.co.jp yahoo.com.kr yahoo.co.za verizon.net aol.com.ve aol.com.ar aol.com.co wild4music.com yahoogroups.com.cn yahoo.com.co wow.com yahoo.com yahooxtra.co.nz yahoo.com.mx yahoo.com.ph sky.com aol.com.mx aol.com.au aolchina.com yahoo.com.net yahoo.com.tw talk21.com compuserve.com yahoo.com.sg yahoogroups.com.tw frontier.com yahoo.co.in yahoo.co.il verizon.net.in yahoo.com.tr yahoogroups.com.hk yahoogroups.co.uk yahoo.com.biz yahoo.com.hr aol.co.uk ybb.ne.jp yahoogroups.co.kr yahoo.com.my rogers.com gte.net yahoogroups.com yahoo.co.th yahoo.com.cn love.com bellatlantic.net yahoo.com.ve yahoo.com.ua；yahoo.ca；aol.hk；；aolpoland.pl；aolnorge.no；aol.fi；；yahoo.hr；aol.cz；yahoo.ee；aol.be；aolcom.tr；yahoo.si；；aol.it；；yahoo.es；yahog.dk；yahogroups.ca；；aol.kr；ahoo；aol.nl；yahoo.bg；；aol.se；yahoo.de；；；；aol.dk；；yahoo.nl；；；aol.dk；AOL.k；SK；yahogroups.de yahoo.gr；；yahoo.ro；；yahoo.gr；；aol.in；yahoo.rs；aol.de；aol；；；；yahoo.se；myaol yahoo.pt；；yahoo.pt；；yahogrupper.dk； yahoo.fr；；；aol.ch； yahoo.it；； AOLPOLCKA.pl；；；yahogruppi.it；；yahoo.cl；；；
+++

+++Bigpond bigpond.com；bigpond.com.au；bigpond.net；telstra.com；bigpond.net.au
+++

+++橙色voila.com；francetelecom.com；orange.com；orange.fr；wanadoo.fr；voila.fr
+++

+++Softbank c.vodafone.ne.jp；jp-h.ne.jp；k.vodafone.ne.jp；jp-d.ne.jp；jp-c.ne.jp；t.vodafone.ne.jp；h.vodafone.ne.jp r.vodafone.ne.jp；q.vodafone.ne.jp jp-t.ne.jp jp-q.ne.jp s.vodafone.ne.jp jp-s.ne.jp jp-r.ne.jp jp-k.ne.jp n.vodafone.ne.jp d.vodafone.ne.jp softbank.ne.jp jp-n.ne.jp；；；；；；；；；；
+++

+++Docomo docomo.ne.jp
+++

+++United Internet gmx.de；1and1.com；gmx.fr；mail.com；1und1.de；gmx.com；gmx.net；gmx.at；web.de；gmx.ch
+++

+++Microsoft hotmail.com.tr；live.de；live.ru；live.nl；windowslive.com；live.jp；mts.net；xbox.com live.com.au；hotmail.fr；hotmail.cl；hotmail.co.th；live.hk；hotmail.com.au；hotmail.com；live.com.my hotmail.co.kr outlook.com.br hotmail.co.il live.co.kr live.co.uk live.com.mx hotmail.co.uk live.com.sg msn.com hotmail.co.jp live.co.za live.com.pt outlook.com live.com live.com.ar hotmail.com.br hotmail.com.ar；live.ie；live.cn；；hotmail.dk；；outlook.ie；live.cn；live.no；live.dk；hotmail.it；live.se；；live.be；live.in；hotmail.se；；hotmail.ch；hotmail.gr；live.it；；hotmail.ca；；live.ca；hotmail.de
+++

+++KDDI au.com；ezweb.ne.jp；uqmobile.jp
+++

+++Italia Online inwind.it；blu.it；virgilio.it；giallo.it；iol.it；libero.it
+++

+++波斯特酒店laposte.net
+++

+++Apple mac.com；icloud.com；apple.com；me.com
+++

### 自訂網域群組標籤 {#custom-domain-group-tab}

您也可以包含自訂網域群組，以新增更多欄到計畫中。

使用 **[!UICONTROL 自訂網域群組]** 標籤定義新的網域群組。 您可以為每個網域新增其涵蓋的所有子網域。<!--TBC-->

例如，如果您新增自訂網域Luma，您希望加入下列子網域：luma.com、luma.co.uk、luma.it、luma.fr、luma.de等。

![](assets/ip-warmup-sample-file-custom.png)

### 範例 {#example}

假設您想要有兩個自訂網域群組：

* 一個僅適用於Hotmail網域。
* 一個用於網域群組Microsoft中的所有其他網域（因此排除所有Hotmail網域）。

請注意，所有其他網域將會收集到 **[!UICONTROL 其他]** 欄。

1. 在 **[!UICONTROL 自訂網域群組]** 標籤，建立 **Hotmail** 網域群組。

1. 在同一列新增所有Hotmail網域。

   您可以 [複製並貼上](#copy-paste) 列在「 」中的所有Hotmail網域 [IP熱身計畫標籤](#ip-warmup-plan-tab) 區段。

1. 新增另一列。

1. 建立 **Microsoft_X** 網域群組。

1. 將非Hotmail的所有Microsoft網域新增至相同列。 同樣地，您可以從上述清單複製並貼上它們。 [了解更多](#copy-paste)

1. 返回 **[!UICONTROL IP熱身計畫]** 標籤。

1. 建立三欄：一個用於 **Hotmail**，一個用於 **Microsoft_X** 一個用於 **其他**.

1. 根據您的需求填寫欄。

>[!NOTE]
>
>將IP熱身計畫上傳到後 [!DNL Journey Optimizer]，您不需要排除Microsoft網域群組。

<!--Only the domain groups listed in the **[!UICONTROL IP Warmup Plan]** tab will be taken into account.-->

### 複製並貼上預設網域 {#copy-paste}

例如，如果您想建立包含所有Hotmail網域的自訂網域群組，您可以從提供的預設清單中複製並貼上網域 [以上](#ip-warmup-plan-tab).

然後使用Excel轉換工具將文字轉換為欄：

1. 選取 **[!UICONTROL 資料]** > **[!UICONTROL 文字至欄……]**，選擇 **[!UICONTROL 已分隔]** 並選取 **[!UICONTROL 下一個]**.

1. 選取 **[!UICONTROL 分號]**，按一下 **[!UICONTROL 下一個]** 和 **[!UICONTROL 完成]**.

現在，每個網域都會顯示在相同列的不同欄中。

## 存取和管理IP熱身計畫 {#manage-ip-warmup-plans}

1. 存取 **[!UICONTROL 管理]** > **[!UICONTROL 頻道]** > **[!UICONTROL IP熱身計畫]** 功能表。 目前所建立的所有IP熱身計畫都會顯示出來。

   ![](assets/ip-warmup-filter-list.png)

1. 您可以依狀態篩選。 不同的狀態包括：

   * **尚未開始**：尚未啟用任何執行。 [了解更多](ip-warmup-execution.md#define-runs)
   * **即時**：成功啟用第一個階段中的第一次執行後，計畫就會變更為此狀態。 [了解更多](ip-warmup-execution.md#define-runs)
   * **已完成**：計畫已標示為已完成。 <!--This option is only available if all the runs in the plan are in **[!UICONTROL Completed]** or **[!UICONTROL Draft]** status (no run can be **[!UICONTROL Live]**).--> [了解更多](ip-warmup-execution.md#mark-as-completed)
     <!--* **Paused**: to check (user action)-->

1. 若要刪除IP熱身計畫，請選取 **[!UICONTROL 刪除]** 圖示並確認刪除。

   >[!NOTE]
   >
   >僅限具有下列專案的計畫： **尚未開始** 狀態可刪除。

   ![](assets/ip-warmup-delete-plan.png)

   >[!CAUTION]
   >
   >將會永久刪除選取的IP熱身計畫。

## 建立 IP 暖身計劃 {#create-ip-warmup-plan}

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_upload"
>title="指定您的 IP 暖身計劃"
>abstract="在 Excel 範本中填入將成為計劃內容的所有資料，例如 IP 暖身階段以及個人資料的目標數量，然後在此處上傳。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/implement-ip-warmup-plan/ip-warmup-plan.html#prepare-file" text="準備 IP 暖身計畫檔案"

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_surface"
>title="選取行銷表面"
>abstract="您選取的表面必須相同於您想要與 IP 暖身計畫相關聯之行銷活動的所選表面。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/channel-surfaces.html?lang=zh-Hant" text="設定管道表面"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/channel-surfaces.html?lang=zh-Hant" text="建立 IP 暖身行銷活動"

若要建立IP熱身計畫，請遵循下列步驟。

1. 存取 **[!UICONTROL 管理]** > **[!UICONTROL 頻道]** > **[!UICONTROL IP熱身計畫]** 功能表，然後按一下 **[!UICONTROL 建立IP熱身計畫]**.

   ![](assets/ip-warmup-create-plan.png)

1. 填寫IP熱身計畫詳細資訊：提供名稱和說明。

   ![](assets/ip-warmup-plan-details.png)

1. 選取 [表面](channel-surfaces.md) 您想要熱身。 只有行銷表面可供選取。 [進一步瞭解電子郵件型別](../email/email-settings.md#email-type)

   >[!NOTE]
   >
   >您要與IP熱身計畫關聯的行銷活動必須使用相同表面。 [瞭解如何建立IP熱身行銷活動](ip-warmup-campaign.md)

1. 上傳包含IP熱身計畫的Excel檔案。 [了解更多](#prepare-file)

   <!--
    You can also download the Excel template from the [!DNL Journey Optimizer] user interface and upload it after filling it with the IP warmup details.-->

   ![](assets/ip-warmup-upload-success.png)

   >[!NOTE]
   >
   >如果上傳失敗，請確定您使用正確的格式和檔案格式(.xls或.xlsx)。 使用 [範本](assets/IPWarmupPlan-Template.xlsx) 由Adobe提供。

1. 按一下 **[!UICONTROL 建立]**。在您上傳的檔案中定義的所有階段、執行、欄及其內容會自動顯示在 [!DNL Journey Optimizer] 介面。

   ![](assets/ip-warmup-plan-uploaded.png)

   >[!NOTE]
   >
   >此 **[!UICONTROL 已鎖定目標]** 欄會顯示每次執行的所有設定檔目標總數，也就是您所定義的每個網域群組的所有設定檔，包括 **其他** 欄（如果有）。

您現在已準備好執行IP熱身計畫。 [了解更多](ip-warmup-execution.md)
