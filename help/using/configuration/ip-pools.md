---
title: 建立 IP 池
description: 了解如何管理IP池
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 606334c3-e3e6-41c1-a10e-63508a3ed747
source-git-commit: b720134ae82a596321aa2815a36e92e6b19c71ba
workflow-type: tm+mt
source-wordcount: '592'
ht-degree: 1%

---

# 建立 IP 池 {#create-ip-pools}

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_pool_header"
>title="設定IP池"
>abstract="您可以建立IP池，將子網域的IP位址分組，以改善電子郵件傳遞能力。"

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_pool"
>title="設定IP池"
>abstract="使用Journey Optimizer，您可以建立IP池，將子網域的IP位址分組。 這可能會大幅改善電子郵件的傳遞能力，因為這麼做可防止子網域的信譽影響其他子網域。"

## 關於IP池 {#about-ip-pools}

使用 [!DNL Journey Optimizer]，您可以建立IP池，將子網域的IP位址分組。

強烈建議建立IP池以實現電子郵件傳遞。 如此一來，您就能防止子網域的信譽影響其他子網域。

例如，一個最佳實務是為行銷訊息建立一個IP池，為交易式訊息另一個IP池。 這樣，如果您的其中一個行銷訊息執行不良，且被客戶宣告為垃圾訊息，則不會影響傳送給同一位客戶的交易式訊息，該客戶仍會收到交易式訊息（購買確認、密碼復原訊息等）。

## 建立IP池 {#create-ip-pool}

要建立IP池，請執行以下步驟：

1. 存取 **[!UICONTROL 管理]** > **[!UICONTROL 管道]** > **[!UICONTROL IP池]** ，然後按一下 **[!UICONTROL 建立IP池]**.

   ![](assets/ip-pool-create.png)

1. 提供IP池的名稱和說明（可選）。

   >[!NOTE]
   >
   >名稱必須以字母(A-Z)開頭，且僅包含英數字元或特殊字元(_、.、-)。

1. 從下拉清單中選擇要包含在池中的IP地址，然後按一下 **[!UICONTROL 提交]**.

   ![](assets/ip-pool-config.png)

   >[!NOTE]
   >
   >清單中會提供與您執行個體布建的所有IP位址。

IP池現在已建立並顯示在清單中。 您可以選取它以存取其屬性並顯示相關的通道表面（即訊息預設集）。 有關如何將通道表面與IP池關聯的詳細資訊，請參閱 [本節](channel-surfaces.md).

![](assets/ip-pool-created.png)

## 編輯IP池 {#edit-ip-pool}

要編輯IP池，請執行以下操作：

1. 從清單中，按一下IP池名稱以開啟它。

   ![](assets/ip-pool-list.png)

1. 視需要編輯其屬性。 您可以修改說明，以及新增或移除IP位址。

   >[!NOTE]
   >
   >IP池名稱不可編輯。 如果要修改它，則需要刪除IP池，並使用您選擇的名稱建立另一個池。

   ![](assets/ip-pool-edit.png)

   >[!CAUTION]
   >
   >考慮刪除IP時請格外小心，因為這會對其他IP造成額外負載，且可能對您的傳送能力造成嚴重影響。 如有疑問，請聯絡傳遞能力專家。

1. 儲存您的變更。

更新會立即或非同步生效，具體取決於與 [通道表面](channel-surfaces.md) 或否：

* 如果IP池為 **not** 與任何通道表面相關聯，更新為瞬時(**[!UICONTROL 成功]** 狀態)。
* 如果IP池 **is** 與通道曲面相關聯，更新最多需要3小時(**[!UICONTROL 處理]** 狀態)。

>[!NOTE]
>
>當 [建立通道曲面](channel-surfaces.md#create-channel-surface)，如果選擇的IP池在版本(**[!UICONTROL 處理]** 狀態)，並且從未與為該曲面選擇的子域相關聯，則無法繼續建立曲面。 [了解更多](channel-surfaces.md#subdomains-and-ip-pools)

要檢查IP池更新狀態，請按一下 **[!UICONTROL 更多動作]** 按鈕並選取 **[!UICONTROL 最近更新]**.

![](assets/ip-pool-recent-update.png)

>[!NOTE]
>
>成功更新IP池後，您可能需要等待：
>* 在被統一消息使用前幾分鐘，
>* 直到IP池的下一批處理在批處理消息中生效。


您也可以使用 **[!UICONTROL 刪除]** 按鈕刪除IP池。 請注意，您無法刪除已與通道表關聯的IP池。

