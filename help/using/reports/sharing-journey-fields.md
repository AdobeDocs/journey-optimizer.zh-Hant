---
solution: Journey Optimizer
product: journey optimizer
title: 歷程欄位
description: 歷程欄位
feature: Journeys, Reporting
topic: Content Management
role: Developer, Admin
level: Experienced
exl-id: 177b4a97-c757-40ca-a190-fbd88169e5e2
TQID: https://experienceleague.adobe.com/dpQ6PEm-afX4PZuWSPrpAWDH7yBhUKZHZRF134VehAg
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
subfeature_v2:
  - id: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 130
ht-degree: 6%

---

# 歷程欄位 {#sharing-journey-fields}

此欄位群組用於&#x200B;**歷程**&#x200B;結構描述（與&#x200B;**journeyStepEvent**&#x200B;相關）。 它包含下列欄位。


>[!NOTE]
>
>在本節[&#128279;](../building-journeys/expression/journey-properties.md#journey-properties-fields)中進一步瞭解歷程屬性。


## journeyID {#journeyid-field}

主要歷程的ID。

型別：字串

## journeyVersionID {#journeyversionid-field}

歷程版本的ID。 此ID代表歷程的身分。

型別：字串

## 名稱 {#name-field}

歷程的名稱。

型別：字串

>[!NOTE]
>
>歷程名稱可用來將歷程執行資料與報告資料集連結。 如果您重新命名歷程，請確定新名稱與您報表資料集中的名稱相符，以維持準確的報告。 不相符可能會導致報表資料無法如預期顯示。 深入瞭解[疑難排解遺失的報告資料](../building-journeys/report-journey.md#troubleshooting-missing-data)。

## 說明 {#description-field}

歷程的說明。

型別：字串

## version {#version-field}

版本，表示為`major`.`minor`

型別：字串
