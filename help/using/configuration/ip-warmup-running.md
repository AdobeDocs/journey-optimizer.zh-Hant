---
solution: Journey Optimizer
product: journey optimizer
title: 執行IP熱身計畫
description: 瞭解如何執行和監視IP熱身計畫
feature: Application Settings
topic: Administration
role: Admin
level: Experienced
keywords: IP、集區、群組、子網域、傳遞能力
hide: true
hidefromtoc: true
source-git-commit: 1ec2c406e777e08de97c3ad53cee5986afeb3c44
workflow-type: tm+mt
source-wordcount: '1014'
ht-degree: 1%

---

# 執行IP熱身計畫 {#ip-warmup-running}

>[!BEGINSHADEBOX]

本文件指南會提供以下內容：

* [開始使用IP熱身](ip-warmup-gs.md)
* [建立IP熱身行銷活動](ip-warmup-campaign.md)
* [建立IP熱身計畫](ip-warmup-plan.md)
* **[執行IP熱身計畫](ip-warmup-running.md)**

>[!ENDSHADEBOX]

一旦您擁有 [已建立IP熱身計畫](ip-warmup-plan.md) 並上傳與傳遞顧問準備的檔案，您可在計畫中定義階段與執行。

每個階段都對應一個由數個執行組成的期間，您會指派單一行銷活動給該期間。

對於每次執行，您都有特定數量的收件者，且您已排程執行此執行的時間。

## 定義階段 {#define-phases}

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_campaigns_excluded"
>title="選取要排除的行銷活動對象"
>abstract="從其他行銷活動中選取您想要從目前階段排除的對象。"

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_domains_excluded"
>title="選取要排除的網域群組"
>abstract="選取要從目前階段排除的網域。"

您需要將階段層級的行銷活動和對象相關聯，並根據需要為與單一創意/行銷活動關聯的所有執行開啟某些設定

在階段層級，系統會確保擷取先前目標設定檔+新設定檔，而在反複專案層級，系統會確保每次執行都具有唯一的設定檔，且計數符合計畫中所列的專案

1. 針對每個階段，選取您要與IP熱身計畫的此階段關聯的促銷活動。

   ![](assets/ip-warmup-plan-select-campaign.png)

   請注意下列事項：

   * 僅限具有下列專案的行銷活動： **[!UICONTROL IP熱身計畫啟用]** 選項已啟用 <!--and live?--> 可供選取。 [了解更多](#create-ip-warmup-campaign)

   * 您必須選取與為目前IP熱身計畫選取之表面相同的行銷活動。

   * 您無法選取其他IP熱身行銷活動中已使用的行銷活動。

1. 在 **[!UICONTROL 設定檔排除]** 區段，您可以看到該階段先前執行的設定檔一律被排除。 例如，如果在Run #1中，前4800位目標人物中涵蓋某個設定檔，系統會自動確保相同的設定檔不會在Run #2中收到電子郵件。

1. 從 **[!UICONTROL 已排除行銷活動對象]** 區段，從其他區段選取對象 <!--executed/live?-->您要從目前階段排除的行銷活動。

   ![](assets/ip-warmup-plan-exclude-campaigns.png)

   例如，在執行階段1時，您必須 [分割它](#split-phase) 因為任何原因。 因此，您可以排除階段1中使用的行銷活動，如此一來，先前從階段1聯絡的設定檔就不會包含在階段2中。 您也可以從其他IP熱身計畫中排除行銷活動。

1. 從 **[!UICONTROL 網域群組已排除]** 區段中，選取要從該階段排除的網域。

   ![](assets/ip-warmup-plan-exclude-domains.png)

   例如，執行IP熱身幾天後，您意識到網域(即Adobe)的ISP信譽不好，您想要在不停止IP熱身計畫的情況下解決它。 在這種情況下，您可以排除Adobe網域群組。

   >[!NOTE]
   >
   >網域排除需要非執行階段，因此您可能必須分割執行階段才能新增排除專案。 同樣地，如果網域群組不是OOTB網域群組，您需要將此網域群組新增至Excel檔案、上傳該網域群組，然後排除該網域。

   ![](assets/ip-warmup-plan-phase-1.png)

1. 您可以視需要新增階段。 它將在目前的最後一個階段之後新增。

1. 使用 **[!UICONTROL 刪除階段]** 按鈕來移除任何不想要的階段。

   ![](assets/ip-warmup-plan-add-delete-phases.png)

   >[!CAUTION]
   >
   >您無法復原 **[!UICONTROL 刪除]** 動作。
   >
   >如果您從IP熱身計畫刪除所有階段，我們建議您重新上傳計畫。

## 定義回合 {#define-runs}

1. 選取每次執行的排程。 <!--which is actually a window of opportunity. meaning? how many hours? shall we specify that to clarify?-->

   ![](assets/ip-warmup-plan-send-time.png)

1. 或者，如果對象細分工作執行有任何延遲，請選取可執行IP熱身行銷活動的視窗。 如果未指定結束時間，則會在開始時間嘗試執行，如果未完成分段，則執行會失敗。

1. 啟動每次執行。 請確定您排程的時間夠早，以允許執行細分工作。 <!--explain how you can evaluate a proper time-->

   >[!CAUTION]
   >
   >每次執行必須在實際傳送時間前至少12小時啟動。 否則，可能無法完成分段。 <!--How do you know when segmentation is complete? Is there a way to prevent user from scheduling less than 12 hours before the segmentation job?-->

   <!--Sart to execute on every day basis by simply clicking the play button > for each run? do you have to come back every day to activate each run? or can you schedule them one after the other?)-->

1. 如果行銷活動尚未開始，您可以停止執行。<!--why?-->

   >[!NOTE]
   >
   >行銷活動開始執行後， **[!UICONTROL 停止]** 按鈕變為無法使用。 <!--TBC in UI-->

   ![](assets/ip-warmup-plan-stop-run.png)

1. 若要新增回合，請選取 **[!UICONTROL 在下方新增回合]** 從三個點的圖示。

   ![](assets/ip-warmup-plan-run-more-actions.png)

## 分割階段 {#split-phase}

在任何時候，如果您想要使用從特定執行開始的不同行銷活動，請選取 **[!UICONTROL 分割至新階段選項]** 從三個點的圖示。

系統會為目前階段的剩餘執行建立一個新階段。 請依照步驟操作 [以上](#define-phases) 以定義新階段。

例如，如果您為「執行#4」選取此選項，則#8要執行的執行#4位將移至新階段。

<!--
You don't have to decide the campaign upfront. You can do a split later. It's a work in progress plan: you activate one run at a time with a campaign and you always have the flexibility to modify it while working on it.

But need to explain in which case you want to modify campaigns, provide examples
-->

## 將計畫標示為已完成 {#mark-as-completed}

如果您的計畫執行得不夠好，或您想要將其刪除以建立另一個計畫，您可以將其標示為已完成。

若要這麼做，請按一下 **[!UICONTROL 更多]** IP熱身計畫的右上角按鈕並選取 **[!UICONTROL 標籤為已完成]**.

![](assets/ip-warmup-plan-mark-completed.png)

只有在計畫中的所有執行都位於時，才能使用此選項 **[!UICONTROL 成功]** 或 **[!UICONTROL 草稿]** 狀態。 無法執行任何動作 **[!UICONTROL 即時]**.

不同的執行狀態會列在 [本節](#monitor-plan).

## 監視計畫 {#monitor-plan}

若要衡量計畫的影響，您可以使用報表來檢查IP熱身行銷活動的效能。 進一步瞭解行銷活動電子郵件 [即時報告](../reports/campaign-live-report.md#email-live) 和 [全域報告](../reports/campaign-global-report.md##email-global).

IP熱身計畫本身也可作為單一地點的整合報表。 您可以檢查元素，例如 **[!UICONTROL 即時]** 或 **[!UICONTROL 成功]** 會針對每個階段執行，並檢視您的IP熱身計畫的進度。

回合可以有下列狀態：

* **[!UICONTROL 草稿]** ：每當建立執行時，無論是何時 [上傳新計畫](ip-warmup-plan.md) 或 [新增回合](#define-runs) 從使用者介面，它需要 **[!UICONTROL 草稿]** 狀態。
* **[!UICONTROL 即時]**：每當您啟動回合時，它需要 **[!UICONTROL 即時]** 狀態。
* **[!UICONTROL 成功]**<!--TBC-->：此回合的行銷活動執行已完成。 <!--i.e. campaign execution has started, no error happened and emails have reached users? to check with Sid-->
* **[!UICONTROL 已取消]**：a **[!UICONTROL 即時]** 已使用「 」取消執行 **[!UICONTROL 停止]** 按鈕。 此按鈕僅在行銷活動執行尚未開始時可用。 [了解更多](#define-runs)
* **[!UICONTROL 已失敗]**：系統發生錯誤，或用於目前階段的行銷活動已停止<!--what should the user do in that case?-->.
