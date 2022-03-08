---
title: 建立 IP 池
description: '"瞭解如何管理ip池"'
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 606334c3-e3e6-41c1-a10e-63508a3ed747
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '471'
ht-degree: 1%

---

# 建立 IP 池 {#create-ip-pools}

## 關於IP池 {#about-ip-pools}

使用Journey Optimizer，可以建立IP池，將子域的IP地址分組在一起。

強烈建議建立IP池以實現電子郵件傳輸。 通過這樣做，可以防止子域的信譽影響其他子域。

例如，一個最佳做法是為您的營銷消息設定一個IP池，為事務性消息設定另一個IP池。 這樣，如果您的營銷消息之一執行不善，並且被客戶聲明為垃圾郵件，則不會影響發送給該客戶的事務性消息，該客戶仍將接收事務性消息（購買確認、密碼恢復消息等）。

## 建立IP池 {#create-ip-pool}

要建立IP池，請執行以下步驟：

1. 訪問 **[!UICONTROL Channels]** / **[!UICONTROL IP pools]** 菜單，然後按一下 **[!UICONTROL Create IP Pool]**。

   ![](assets/ip-pool-create.png)

1. 提供IP池的名稱和說明（可選）。

   >[!NOTE]
   >
   >子域的名稱必須以字母(A-Z)開頭，並且只包括字母數字字元或特殊字元(_、.、-)。

1. 從下拉清單中選擇要包含在池中的IP地址，然後按一下 **[!UICONTROL Submit]**。

   ![](assets/ip-pool-config.png)

   >[!NOTE]
   >
   >清單中提供了隨實例設定的所有IP地址。

IP池現在已建立並顯示在清單中。 您可以選擇它以訪問其屬性並顯示關聯的消息預設。 有關如何將消息預設與IP池關聯的詳細資訊，請參閱 [此部分](message-presets.md))。

![](assets/ip-pool-created.png)

## 編輯IP池 {#edit-ip-pool}

編輯IP池：

1. 在清單中，按一下IP池名稱以將其開啟。

   ![](assets/ip-pool-list.png)

1. 根據需要編輯其屬性。 您可以修改說明，並添加或刪除IP地址。

   ![](assets/ip-pool-edit.png)

   >[!CAUTION]
   >
   >考慮刪除IP時，請格外小心，因為這會給其他IP增加額外負載，並可能對您的可交付性造成嚴重影響。 如有任何疑問，請與交付能力專家聯繫。

1. 儲存您的變更。

>[!NOTE]
>
>IP池名稱不可編輯。 如果要修改它，需要刪除IP池，然後使用您選擇的名稱建立另一個池。

更新會立即生效或非同步生效，具體取決於與 [消息預設](message-presets.md) 或否：

* 如果IP池為 **不** 在消息預設中選中，更新是即時(**[!UICONTROL Success]** 狀態)。
* 如果IP池 **是** 在消息預設中選擇，更新最多可能需要7-10個工作日(**[!UICONTROL Processing]** 狀態)。

要檢查IP池更新狀態，請按一下 **[!UICONTROL More actions]** 按鈕 **[!UICONTROL Recent updates]**。

![](assets/ip-pool-recent-update.png)

>[!NOTE]
>
>成功更新IP池後，您可能必須等待：
>* 在被統一消息消耗前幾分鐘，
>* 直到IP池在批處理消息中生效的下一個批處理。


您還可以使用 **[!UICONTROL Delete]** 按鈕以刪除IP池。 請注意，無法刪除已與消息預設關聯的IP池。

