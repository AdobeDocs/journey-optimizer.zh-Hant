---
title: 在Journey Optimizer個人化內容
description: 個人化快速入門
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 5%

---

# 快速入門 {#add-personalization}

![](../assets/do-not-localize/badge.png)

在Journey Optimizer，個人化是指利用您擁有的有關他的資料和資訊，將訊息鎖定在特定訂閱者的動作。 這可以是他的名字、興趣、居住地等等。

Journey Optimizer使用&#x200B;**inline**&#x200B;以Handlebars為基礎的簡單個人化語法，可讓您建立包含雙大括弧&#x200B;**{{}}**&#x200B;之內容的運算式。 您可以在相同的內容或欄位中新增多個運算式，不受限制。 請參閱[個人化語法](personalization-syntax.md)。

個人化基於由Adobe Experience Platform定義的&#x200B;**XDM單個配置檔案**&#x200B;架構管理的配置檔案資料。 有關詳細資訊，請參閱[Adobe Experience Platform資料模型(XDM)文檔](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hant)。

>[!CAUTION]
>**XDM Individual Profile**&#x200B;架構是您唯一可用來個人化Journey Optimizer地區內容的架構。

**範例:**

```
Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}

Hello {{profile.person.gender}} {{profile.person.name.fullName}}
```

在&#x200B;**消息處理**（電子郵件和推送）期間，表達式將替換為Experience Cloud平台資料庫中包含的資料。

```
Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}} becomes “Hello John Doe”.
```
