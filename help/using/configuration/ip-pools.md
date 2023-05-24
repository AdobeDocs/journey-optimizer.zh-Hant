---
solution: Journey Optimizer
product: journey optimizer
title: 建立 IP 池
description: 瞭解如何管理IP池
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
keywords: IP 、池、組、子域、可傳遞性
exl-id: 606334c3-e3e6-41c1-a10e-63508a3ed747
source-git-commit: f4068450dde5f85652096c09e7f817dbab40a3d8
workflow-type: tm+mt
source-wordcount: '717'
ht-degree: 10%

---

# 建立 IP 池 {#create-ip-pools}

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_pool_header"
>title="設定 IP 池"
>abstract="IP 池會收集您的子網域的 IP 位址以提高電子郵件的可遞送性。"

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_pool"
>title="設定 IP 池"
>abstract="使用 Journey Optimizer，您可以建立 IP 池以將子網域的 IP 位址聚集在一起。這可能會大幅提高您的電子郵件可遞送性，因為這樣做可以防止某個子網域的聲譽影響您的其他子網域。"

## 關於IP池 {#about-ip-pools}

與 [!DNL Journey Optimizer]，可以建立IP池以將子域的IP地址分組在一起。

強烈建議建立IP池以實現電子郵件傳輸。 通過這樣做，可以防止子域的信譽影響其他子域。

例如，一個最佳做法是為您的營銷消息設定一個IP池，為事務性消息設定另一個IP池。 這樣，如果您的營銷消息之一執行不善，並且被客戶聲明為垃圾郵件，則不會影響發送給該客戶的事務性消息，該客戶仍將接收事務性消息（購買確認、密碼恢復消息等）。

>[!CAUTION]
>
>IP池配置對所有環境都是常見的。 因此，任何IP池建立或版本都會影響生產沙箱。

## 建立IP池 {#create-ip-pool}

要建立IP池，請執行以下步驟：

1. 訪問 **[!UICONTROL 管理]** > **[!UICONTROL 頻道]** > **[!UICONTROL IP池]** 菜單，然後按一下 **[!UICONTROL 建立IP池]**。

   ![](assets/ip-pool-create.png)

1. 提供IP池的名稱和說明（可選）。

   >[!NOTE]
   >
   >名稱必須以字母(A-Z)開頭，並且只包括字母數字字元或特殊字元(_、.、-)。

1. 從下拉清單中選擇要包含在池中的IP地址，然後按一下 **[!UICONTROL 提交]**。

   ![](assets/ip-pool-config.png)

   >[!NOTE]
   >
   >清單中提供了隨實例設定的所有IP地址。

選擇IP時，可以從清單中看到與IP關聯的PTR記錄。 這樣，在建立IP池時，您就可以驗證每個IP的品牌資訊，並選擇具有相同品牌資訊的IP。 [瞭解有關PTR記錄的詳細資訊](ptr-records.md)

![](assets/ip-pool-ptr-record.png)

>[!NOTE]
>
>如果沒有為IP配置PTR記錄，則不能選擇該IP。 聯繫您的Adobe代表，以配置該IP的PTR記錄。

建立IP池後，當懸停在IP池下拉清單下顯示的IP地址上時，PTR資訊可見。

![](assets/ip-pool-ptr-record-tooltip.png)

IP池現在已建立並顯示在清單中。 您可以選擇它以訪問其屬性並顯示關聯的通道表面（即消息預設）。 有關如何將通道表面與IP池關聯的詳細資訊，請參閱 [此部分](channel-surfaces.md)。

![](assets/ip-pool-created.png)

## 編輯IP池 {#edit-ip-pool}

要編輯IP池，請執行以下步驟。

1. 在清單中，按一下IP池名稱以將其開啟。

   ![](assets/ip-pool-list.png)

1. 根據需要編輯其屬性。 您可以修改說明，並添加或刪除IP地址。

   >[!NOTE]
   >
   >IP池名稱不可編輯。 如果要修改它，需要刪除IP池，然後使用您選擇的名稱建立另一個池。

   ![](assets/ip-pool-edit.png)

   >[!CAUTION]
   >
   >考慮刪除IP時，請格外小心，因為這會給其他IP增加額外負載，並可能對您的可交付性造成嚴重影響。 如有任何疑問，請與交付能力專家聯繫。

1. 儲存您的變更。

更新會立即生效或非同步生效，具體取決於與 [通道表面](channel-surfaces.md) 或否：

* 如果IP池為 **不** 與任何通道曲面相關，更新是瞬時(**[!UICONTROL 成功]** 狀態)。
* 如果IP池 **是** 與通道表面關聯，更新最多需要3小時(**[!UICONTROL 處理]** 狀態)。

>[!NOTE]
>
>當 [建立通道曲面](channel-surfaces.md#create-channel-surface)，如果選擇的IP池位於版本(**[!UICONTROL 處理]** 狀態)，並且從未與為該曲面選擇的子域關聯，因此無法繼續建立曲面。 [了解更多](channel-surfaces.md#subdomains-and-ip-pools)

要檢查IP池更新狀態，請按一下 **[!UICONTROL 更多操作]** 按鈕 **[!UICONTROL 最近更新]**。

![](assets/ip-pool-recent-update.png)

>[!NOTE]
>
>成功更新IP池後，您可能必須等待：
>* 在被統一消息消耗前幾分鐘，
>* 直到IP池在批處理消息中生效的下一個批處理。


您還可以使用 **[!UICONTROL 刪除]** 按鈕以刪除IP池。 請注意，不能刪除已與通道表面關聯的IP池。

