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
source-git-commit: 6961a07e2874f9beb76a9beaebb29997d114d8e7
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 6%

---

# 歷程欄位 {#sharing-journey-fields}

此欄位群組用於&#x200B;**歷程**&#x200B;結構描述（與&#x200B;**journeyStepEvent**&#x200B;相關）。 它包含下列欄位。


>[!NOTE]
>
>在本節[中進一步瞭解歷程屬性](../building-journeys/expression/journey-properties.md#journey-properties-fields)。


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

## 版本 {#version-field}

版本，表示為`major`.`minor`

型別：字串
