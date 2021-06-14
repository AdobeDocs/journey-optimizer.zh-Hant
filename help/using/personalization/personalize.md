---
title: 在 Journey Optimizer 中個人化內容
description: 開始使用個人化
feature: 個性化
topic: 個性化
role: Data Engineer
level: Beginner
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 50%

---

# 開始使用個人化{#add-personalization}

![](../assets/do-not-localize/badge.png)

探索Journey Optimier個人化功能，運用您擁有的關於他/她的資料和資訊，將訊息調整為每個特定收件者。 這可以是他的名字，他的興趣，他住的地方，他買的東西，等等。

Journey Optimizer 使用以 Handlebars 為基礎的&#x200B;**內嵌**&#x200B;簡單個人化語法，可讓您建立包含雙大括號&#x200B;**{{}}**&#x200B;之內容的運算式。 您可以在相同的內容或欄位中新增多個運算式，不受限制。 進一步了解[個人化語法](personalization-syntax.md)。

根據由 Adobe Experience Platform 定義的 **XDM 個人設定檔**&#x200B;方案管理的設定檔資料進行個人化。 有關詳細資訊，請參閱 [Adobe Experience Platform 資料模型 (XDM) 文件](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hant)。

>[!CAUTION]
>**XDM個別設定檔**&#x200B;結構是您唯一可用來個人化Journey Optimizer中內容的結構。

**範例：**

```
Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}

Hello {{profile.person.gender}} {{profile.person.name.fullName}}
```

處理訊息（電子郵件和推播）時，Journey Optimizer會以Experience Cloud平台資料庫中包含的資料取代運算式。

```
Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}} becomes “Hello John Doe”.
```
