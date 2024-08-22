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
source-git-commit: b9208544b08b474db386cce3d4fab0a4429a5f54
workflow-type: tm+mt
source-wordcount: '696'
ht-degree: 9%

---

# 排除原因 {#exclusion-list}

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
| PushNoValidTokenFoundForApps | 050031 | 推播 | 在設定中找不到目標應用程式的有效權杖時，會產生排除事件。 |
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
| WebNoVariantDefined | 050041 | Web | 若未定義網頁訊息的變體，則會產生排除事件。 |
| WebNoMessageFoundForTreatment | 050042 | Web | 當為訊息啟用實驗且找不到符合條件的處理時，會產生排除事件。 |
