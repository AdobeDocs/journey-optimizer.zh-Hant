---
solution: Journey Optimizer
product: journey optimizer
title: 關於 Adobe Experience Platform 客群
description: 了解如何使用 Adobe Experience Platform 客群
feature: Audiences, Profiles
topic: Content Management
role: User
level: Beginner
exl-id: 71c652ba-f38f-452c-9c1b-dcd728307baf
TQID: https://experienceleague.adobe.com/HkybhydJwQDHVEXCKM5o16ZNeiBk-n9mogm-2pwFKus
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: baecb07f-ce89-4ebb-9cd9-0f7c053f944f
subfeature_v2:
  - id: f42b4d14-fe8a-428b-b62e-e7995eaab1b3
  - id: b32bb433-f8c6-4931-8e52-e657230a3bf2
  - id: e95b6013-acbe-46e9-a3b5-b80e14088d7d
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
source-git-commit: a51edc00631334874d111d8350ee7b0eb8e81aa5
workflow-type: tm+mt
source-wordcount: 177
ht-degree: 9%

---

# 自訂上傳 {#custom-upload}

>[!BEGINSHADEBOX]

**在此頁面上：**&#x200B;瞭解如何使用Adobe Experience Platform對象入口網站，從CSV檔案匯入對象，並將其識別屬性對應至客戶設定檔。

>[!ENDSHADEBOX]

Adobe Experience Platform對象入口網站可讓您使用CSV檔案匯入對象。

在自訂上傳程式期間，指定要用作身分的CSV屬性，以及它對應到的設定檔身分。 這會在對象資料和設定檔之間建立連結。 如果CSV檔案包含在設定檔中找不到的身分值，則會建立具有該身分值的新設定檔。

>[!NOTE]
>
>對於自訂上傳對象，如果循環歷程中啟用了「增量讀取」，則設定檔僅在第一次循環時擷取，因為這些對象已修正。

![](assets/import-audience.png)

Adobe Experience Platform [Segmentation Service檔案](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/segmentation/ui/audience-portal#import-audience){target="_blank"}提供了有關如何匯入對象的詳細資訊。

瞭解如何在影片中以CSV格式上傳對象：

>[!VIDEO](https://video.tv.adobe.com/v/3423355?captions=chi_hant&quality=12)
