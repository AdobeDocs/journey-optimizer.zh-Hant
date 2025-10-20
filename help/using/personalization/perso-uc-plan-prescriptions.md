---
title: 範本Personalization範例
description: Journey Optimizer Personalization範例
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
exl-id: 832b0bfa-ec74-4b1d-ad85-d4e4ea2f8863
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 3%

---

# 健康計劃處方電子郵件 {#plan-prescription}

設定檔包含健康計畫，而每個計畫都包含處方。 處方有各種狀態，例如「就緒」、「召回」或「已接受」。

在此使用案例中，我們希望傳送一封電子郵件給每個設定檔，包括所有準備好取用或召回的處方。 按一下底下的每個標籤，以取得關於用於實作此使用案例的語法的詳細資訊。

>[!BEGINTABS]

>[!TAB 已轉譯的訊息]

<p>嗨，John Doe，</p>
<p>以下是已準備好取貨或已被召回的處方：</p>

**健康情況計畫A**

<ul>

<li>
      <strong>處方識別碼：</strong> pres1<br>
      <strong>名稱：</strong>藥物A<br>
      <strong>狀態：</strong>就緒
   </li>

<li>
      <strong>處方識別碼：</strong> pres2<br>
      <strong>名稱：</strong>藥物B<br>
      <strong>狀態：</strong>回收
   </li>

</ul>

**健康情況計畫B**

<ul>

<li>
      <strong>處方識別碼：</strong> pres4<br>
      <strong>名稱：</strong>藥物D<br>
      <strong>狀態：</strong>就緒
   </li>

</ul>

>[!TAB HTML範本]

```html
<p>Hi {{profile.person.firstName}} {{profile.person.lastName}},</p>
<p>Here are the prescriptions that are either ready for pick up or have been recalled:</p>
{{#each profile.plans as |plan|}}
<h3>{{plan.name}}</h3>
<ul>
   {{#each plan.prescriptions as |prescription|}}
   {%#if prescription.state = "ready" or prescription.state = "recall"%}
   <li>
      <strong>Prescription ID:</strong> {{prescription.prescription_id}}<br>
      <strong>Name:</strong> {{prescription.name}}<br>
      <strong>State:</strong> {{prescription.state}}
   </li>
   {%/if%}
   {{/each}}
</ul>
{{/each}}
```

>[!TAB 設定檔資料]

```javascript
{
  "profile": {
    "person": {
      "firstName": "John",
      "lastName": "Doe"
    },
    "plans": [
      {
        "planId": "plan1",
        "name": "Health Plan A",
        "prescriptions": [
          {
            "prescription_id": "pres1",
            "name": "Medication A",
            "state": "ready"
          },
          {
            "prescription_id": "pres2",
            "name": "Medication B",
            "state": "recall"
          }
        ]
      },
      {
        "planId": "plan2",
        "name": "Health Plan B",
        "prescriptions": [
          {
            "prescription_id": "pres3",
            "name": "Medication C",
            "state": "picked up"
          },
          {
            "prescription_id": "pres4",
            "name": "Medication D",
            "state": "ready"
          }
        ]
      }
    ]
  }
}
```

>[!ENDTABS]
