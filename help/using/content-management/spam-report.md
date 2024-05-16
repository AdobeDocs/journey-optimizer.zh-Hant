---
title: 使用垃圾郵件報告
description: 瞭解如何使用垃圾郵件報告。
feature: Preview
role: User
level: Beginner
badge: label="Beta"
hide: true
hidefromtoc: true
exl-id: 9ab43b14-41cf-49f1-bdcf-6fee58db5000
source-git-commit: 4c1dca7815594bbbf5a2d84682338e8b2d743965
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 0%

---

# 電子郵件垃圾郵件報告 {#spam-report}

[!DNL Journey Optimizer] 可讓您檢查內容對抗垃圾郵件篩選的表現，並確保您的訊息進入客戶的收件匣，而非垃圾郵件。

編輯或預覽電子郵件內容時， **[!UICONTROL 垃圾郵件報告]** 選項提供評分和建議，以改善所列每個個別專案的分數。

這可讓您判斷郵件在接收時是否會被反垃圾郵件工具視為垃圾郵件，如果不是這種情況，則採取動作。 許多電子郵件收件匣提供者使用工具作為其垃圾郵件篩選流程的一部分。 傳送分數不佳的電子郵件可能會嚴重影響您的傳遞能力。


>[!CAUTION]
>
>* 此功能目前僅以私人測試版的形式提供。
>
>* 目前，垃圾郵件報告分析只能對英文內容執行。
>
>* 垃圾郵件報告會提供資訊，不會阻止傳送分數不正確的訊息。

若要存取 **[!UICONTROL 垃圾郵件報告]**，請遵循下列步驟。

1. 從 **[!UICONTROL 模擬]** 熒幕，按一下 **[!UICONTROL 垃圾郵件報告]** 按鈕。

   ![](assets/spam-report-button.png)

<!--
    You can also open the [Email Designer](../email/content-from-scratch.md), click the **[!UICONTROL More]** button and select **[!UICONTROL Check spam score]** from the menu.

    ![](assets/spam-report-check-score.png)
-->

1. 系統會自動執行反垃圾郵件檢查，並且 **[!UICONTROL 垃圾郵件報告]** 視窗會顯示結果。 它會顯示您的內容在正文版面配置、結構、影像大小、垃圾郵件觸發字詞（如果有的話）等方面的表現。

   ![](assets/spam-report-high-score.png)

1. 檢查每個專案的分數和說明。

   分數越低越好。 如果分數高於5，則會顯示警告：指出某些訊息在收到時可能會遭到封鎖或標籤為垃圾訊息。

1. 根據該得分，如果您認為某些元素可以改善，請在中編輯您的內容 [電子郵件設計工具](../email/content-from-scratch.md) 並進行必要的更新。

1. 完成變更後，瀏覽回 **[!UICONTROL 垃圾郵件報告]** 畫面以確保您的分數已改善。

   ![](assets/spam-report-low-score.png)

<!--You can also check the message's alerts for warnings on potential risk of spam detection. Follow the steps below.

1. Click the **[!UICONTROL Alerts]** button on top right of the screen. [Learn more on email alerts](../email/create-email.md#check-email-alerts)

1. If **[!UICONTROL Spam checker alert]** is displayed, you should check your content for a potential risk of spam using the **[!UICONTROL Spam report]** feature as detailed above.

    ![](assets/spam-report-alert.png)
-->
