---
solution: Journey Optimizer
product: journey optimizer
title: 配置AEM存放庫設定
description: 瞭解管理員如何在Journey Optimizer中設定AEM存放庫、自訂網域、已驗證的發佈和僅限作者的內容片段存取。
feature: Integrations
topic: Administration
role: Admin
level: Experienced
hide: true
keywords: AEM，內容片段，管理，存放庫，驗證，作者，發佈
feature_v2: id: fe96aceb-8194-4a8a-a6b0-75302d02804d
subfeature_v2: id: c7dc31c0-c4f7-42a7-8cf5-a8c5aeb0de74
source-git-commit: 7cf2235a14f9ebb49fac02161743f75fee141504
workflow-type: tm+mt
source-wordcount: 467
ht-degree: 0%

---

# 設定Adobe Experience Manager存放庫存取權 {#aem-admin-settings}

>[!BEGINSHADEBOX]

**在此頁面上：**&#x200B;瞭解管理員如何將沙箱連線至Adobe Experience Manager存放庫 — 設定僅限作者或發佈存取權、自訂網域及驗證 — 讓行銷人員能夠在其歷程及行銷活動中使用AEM內容片段。

>[!ENDSHADEBOX]

Adobe Journey Optimizer與&#x200B;**[!DNL Adobe Experience Manager as a Cloud Service]**&#x200B;整合，因此您可以在歷程與行銷活動中使用&#x200B;**內容片段**。 **預設會從Adobe Experience Manager發佈存放庫讀取內容片段**，管理員可以在&#x200B;**[!UICONTROL AEM整合]**&#x200B;功能表中切換為僅限作者或調整發佈存取權。

➡️設定存放庫後，請繼續[使用Experience Manager內容片段](../integrations/aem-fragments.md)，以在Journey Optimizer中編寫和選取工作。

## 設定存放庫 {#configure-ui}

>[!NOTE]
>
> **[!UICONTROL AEM整合]**&#x200B;儲存每個沙箱&#x200B;**的存放庫設定**。 每個沙箱都會保留自己的整合，且不會套用至多個沙箱。

Journey Optimizer會為每個組織、沙箱和Adobe Experience Manager存放庫儲存一個整合。 如果您儲存相同組合的新整合，它會取代先前的設定，而只保留最新的設定。

若要設定您的存放庫：

1. 存取&#x200B;**[!UICONTROL 管理]** > **[!UICONTROL 管道]** > **[!UICONTROL AEM整合]**。

1. 按一下&#x200B;**[!UICONTROL 建立整合]**。

   ![](assets/aem-admin-settings-1.png)

1. 如果您使用&#x200B;**[!DNL Adobe Experience Manager Managed Services]**，請在&#x200B;**[!UICONTROL 自訂AMS存放庫ID]**&#x200B;欄位中輸入以`adobecqms.net`結尾的存放庫主機名稱。

   ![](assets/aem-admin-settings-6.png)

1. 選擇要設定的存放庫，然後按一下&#x200B;**[!UICONTROL 下一步]**。

   此外，您可以按一下&#x200B;**[!UICONTROL 檢視]**&#x200B;來存取此存放庫。

   >[!IMPORTANT]
   >
   >儲存相同組織、沙箱和存放庫的新設定&#x200B;**取代**&#x200B;預設設定，即&#x200B;**發佈**&#x200B;存放庫。

   ![](assets/aem-admin-settings-2.png)

1. 輸入&#x200B;**[!UICONTROL 名稱]**&#x200B;和&#x200B;**[!UICONTROL 描述]**。

1. 選擇您的設定：

   +++ 僅作者設定

   當Journey Optimizer應僅從Adobe Experience Manager **作者**&#x200B;環境中讀取內容片段時，選取&#x200B;**[!UICONTROL 僅作者設定]**。 不支援從作者復寫到發佈和即時發佈更新。

   ![](assets/aem-admin-settings-3.png)

   +++

   +++ 發佈執行個體設定

   1. 選取&#x200B;**[!UICONTROL 發佈執行個體設定]**&#x200B;以開啟發佈執行個體設定。

      ![](assets/aem-admin-settings-4.png)

   1. 選擇性地啟用&#x200B;**[!UICONTROL 傳送Token至發佈執行個體]**，以便將服務認證包含在對發佈執行個體的要求中。

   1. 貼上有效的&#x200B;**[!UICONTROL 服務認證JSON]**&#x200B;以進行驗證。

   1. 如果您的組織無法連線至預設AEM發佈主機(`publish-XX-XX.adobeaemcloud.com`)來擷取內容，可選擇提供自訂網域。

      ![](assets/aem-admin-settings-5.png)

   +++

1. 完成執行個體設定後，請挑選內容片段以確認整合可正常運作。

   ![](assets/aem-admin-settings-7.png)

1. 在&#x200B;**內容警告器**&#x200B;視窗中，選取您要測試的片段，然後按一下&#x200B;**[!UICONTROL 選取]**。

1. 按一下「**[!UICONTROL 儲存]**」。

1. 當您儲存並選取測試內容片段時，驗證會自動執行。 如果驗證失敗，會顯示錯誤清單，以便您修正設定。

   ![](assets/aem-admin-settings-8.png)

1. 若要編輯或停用此存放庫整合，請從&#x200B;**[!UICONTROL AEM整合]**&#x200B;功能表存取您先前建立的設定。

儲存此設定時，Journey Optimizer會將該存放庫的設定儲存在目前的沙箱中。 然後，在&#x200B;**內容建議程式**&#x200B;選取器中瀏覽及選取內容時，您可以使用該存放庫及其設定。

