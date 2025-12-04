---
solution: Journey Optimizer
product: journey optimizer
title: 排除專案清單
description: 進一步瞭解傳送期間發生的排除
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: a34ba1a8-87d5-4f9c-a181-2f49e74e8f09
source-git-commit: ca6f722c93fffe0cebcddb4f730f23d9a720ef9d
workflow-type: tm+mt
source-wordcount: '868'
ht-degree: 8%

---

# 排除原因 {#exclusion-list}

## 行銷活動報告中排除專案的計算方式

檢視行銷活動報表時，請注意，*排除專案*&#x200B;量度的計算方式如下：

**排除專案=唯一排除專案+重複排除事件**

這表示如果設定檔被多次排除（例如，由於相同設定檔有多個排除事件），則每個事件都會計入排除總數。 因此，*已傳遞*&#x200B;和&#x200B;*排除專案*&#x200B;的總和可能會超過原始目標對象規模。 此行為是預期行為，反映系統中追蹤排除事件的方式。

**範例：**

- 目標對象： 94,000個設定檔
- 送達：69,000個
- 排除專案： 37,000 （包含重複的排除事件）
- 總計（已送達+排除專案）：106,000

總計超過目標對象，因為重複的排除事件會包含在排除計數中。

如需特定排除原因的詳細資訊，請參閱下表。

## 排除原因清單

| 排除原因 | 錯誤代碼 | Channel | 說明 |
|-|-|-|-|
| RuntimeDispatchError | 050301 | 所有管道 | 任何執行階段傳送錯誤的一般排除事件。 |
| RuntimeRenderingError | 050302 | 所有管道 | 任何執行階段轉譯錯誤的一般排除事件。 |
| 實驗的NamespaceError | 050017 | 所有管道 | 當實驗中的名稱空間與設定檔的名稱空間不同時，會產生排除事件。 |
| ExperimentationHoldoutExclusion | 050018 | 所有管道 | 當實驗的合格處理為「保留」時，會產生此排除事件。 |
| ExcludedForControlRules | 050002 | 所有管道 | 當傳送目前的訊息導致違反控制規則（例如一個月內允許的電子郵件數量）時，會產生此排除事件。 |
| DirectMailNoVariantDefined | 050062 | 直接郵件 | 未定義直接郵件變體時，會產生排除事件。 |
| DirectMailNoMessageFoundForTreatment | 050061 | 直接郵件 | 當為訊息啟用實驗且找不到符合條件的處理時，會產生排除事件。 |
| EmailNoConsent | 050101 | 電子郵件 | 當使用者選擇退出接收行銷電子郵件時，會產生排除事件。 |
| 已禁止 | 050107 | 電子郵件 | 由於隱藏原因之一而排除。 |
| 電子郵件已隱藏 | 050102 | 電子郵件 | 抑制目標電子郵件時會產生排除事件。 |
| 已隱藏的網域 | 050105 | 電子郵件 | 抑制目標電子郵件的網域時，會產生排除事件。 |
| 不允許 | 050108 | 電子郵件 | 當啟用允許清單並將目標電子郵件從允許清單中排除時，會產生排除事件。 |
| EmailNotAllowed | 050103 | 電子郵件 | 當啟用允許清單並將目標電子郵件從允許清單中排除時，會產生排除事件。 |
| DomainNotAllowed | 050106 | 電子郵件 | 當啟用允許清單並將目標電子郵件的網域從允許清單中排除時，會產生排除事件。 |
| EmailNoSubscriberIdFoundInProfile | 050025 | 電子郵件 | 在訂閱電子郵件的設定檔中找不到subscriberId時，會產生排除事件。 |
| EmailNoAddressFoundInProfile | 050020 | 電子郵件 | 在執行位址中找不到電子郵件地址時，會產生排除事件。 |
| EmailNoAddressDefinedInPreset | 050021 | 電子郵件 | 未在設定中定義執行位址時，會產生排除事件。 |
| EmailNoVariantDefined | 050026 | 電子郵件 | 未在電子郵件訊息中定義變體時，會產生排除事件。 |
| EmailNoMessageFoundForTreatment | 050027 | 電子郵件 | 當為訊息啟用實驗且找不到符合條件的處理時，會產生排除事件。 |
| EmailFormatAddress | 050024 | 電子郵件 | 當電子郵件包含格式錯誤的地址時，會產生排除事件。 |
| InAppNoVariantDefined | 050041 | 應用程式內 | 若未定義應用程式內訊息的變體，則會產生排除事件。 |
| InAppNoMessageFoundForTreatment | 050042 | 應用程式內 | 當為訊息啟用實驗且找不到符合條件的處理時，會產生排除事件。 |
| PushNoTokenFoundInProfile | 050030 | 推播 | 設定檔沒有推播權杖時，會產生排除事件。 |
| PushNoValidTokenFoundForApps | 050031 | 推播 | 在設定中找不到目標應用程式的有效權杖時，會產生排除事件。 **重要：**&#x200B;使用生產憑證時，使用者設定檔中的`pushNotificationDetails.platform`屬性必須設定為`apns`。 如果使用沙箱憑證，請將其設為`apnsSandbox`。 platform屬性和憑證型別不符將觸發此排除。 |
| PushMalformProfile | 050034 | 推播 | 設定檔中的pushNotificationDetails格式錯誤時，會產生排除事件。 |
| PushNoConsent | 050111 | 推播 | 當使用者選擇退出行銷推播通知時，會產生排除事件。 |
| PushNoApplicationDefinedInPreset | 050033 | 推播 | 當設定不含任何目標應用程式時，會產生排除事件。 |
| PushNoVariantDefined | 050035 | 推播 | 若未定義變體，則會產生排除事件。 |
| PushNoMessageFoundForTreatment | 050036 | 推播 | 當為訊息啟用實驗且找不到符合條件的處理時，會產生排除事件。 |
| SMSNoConsent | 050104 | 簡訊 | 當使用者選擇退出行銷簡訊時，會產生排除事件。 |
| SMSFromNumberNotDefinedInPreset | 050152 | 簡訊 | 若設定中未定義「FromNumber」，則會產生排除事件。 |
| SMSNoToNumberDefinedInProfile | 050153 | 簡訊 | 若設定中未定義「ToNumber」，則會產生排除事件。 |
| SMSNoVariantDefined | 050154 | 簡訊 | 若未定義變體，則會產生排除事件。 |
| SMSNoMessageFoundForTreatment | 050155 | 簡訊 | 當為訊息啟用實驗且找不到符合條件的處理時，會產生排除事件。 |
| WebNoVariantDefined | 050041 | 網頁 | 若未定義網頁訊息的變體，則會產生排除事件。 |
| WebNoMessageFoundForTreatment | 050042 | 網頁 | 當為訊息啟用實驗且找不到符合條件的處理時，會產生排除事件。 |
