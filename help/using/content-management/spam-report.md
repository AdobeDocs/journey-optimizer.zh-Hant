---
title: 使用垃圾郵件報告
description: 瞭解如何使用垃圾郵件報告。
feature: Preview
role: User
level: Beginner
hide: true
hidefromtoc: true
source-git-commit: b6872806b3961bb2afbfc03999d984384492cc6d
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 2%

---

# 使用垃圾郵件報告 {#spam-report}

>[!AVAILABILITY]
>
>垃圾郵件報告功能目前僅供特定使用者測試版。 若要加入 Beta 版計畫，請連絡 Adobe 客戶服務。

[!DNL Journey Optimizer] 可讓您檢查內容對抗垃圾郵件篩選的表現，並確保您的訊息進入客戶的收件匣，而非垃圾郵件。

>[!CAUTION]
>
>* 此功能目前僅適用於電子郵件頻道。
>
>* 目前，垃圾郵件報告分析只能對英文內容執行。

編輯或預覽內容時， **[!UICONTROL 垃圾郵件報告]** 選項提供評分和建議，以改善所列每個個別專案的分數。

這可讓您判斷郵件在接收時是否會被反垃圾郵件工具視為垃圾郵件，如果不是這種情況，則採取動作。

>[!CAUTION]
>
>「垃圾訊息」報告僅提供指示和警告。 請注意，如果垃圾郵件報告指出您的內容被視為垃圾郵件，則不會阻止您傳送郵件。 您可以選擇根據分數和建議的改進內容採取行動。

若要使用 **[!UICONTROL 垃圾郵件報告]** 功能，請遵循下列步驟。

<!--For example spam scoring tool can tell that there are too many Images compared to the text. Retailers tend to do this even though the spam score gets worse because the content is more engaging.-->

<!--Michael, who is a marketer with NIKE works along with Tara from testing team to ensure that the emails being sent as part of the campaign/journey don't get categorised as SPAM.

They need an integration within AJO's marketing system to show how the curated content is doing against different SPAM compliance pillars like for SPAM trigger words, HTML Body content and layout, subject line etc.

They should be able to get scores for each individual items as shown by market standard SPAM filtering tools like Spam Assassin, Symantec etc.

They should also get suggestions on how to improve the score better to be confident that the messages don't get categorised as spam.-->

1. 從 **[!UICONTROL 模擬]** 熒幕，按一下 **[!UICONTROL 垃圾郵件報告]** 按鈕。

   ![](assets/spam-report-button.png)

<!--
    You can also open the [Email Designer](../email/content-from-scratch.md), click the **[!UICONTROL More]** button and select **[!UICONTROL Check spam score]** from the menu.

    ![](assets/spam-report-check-score.png)
-->

1. 系統會自動執行反垃圾郵件檢查，並且 **[!UICONTROL 垃圾郵件報告]** 視窗會顯示結果。 它會顯示您的內容在正文版面配置、結構、影像大小、垃圾郵件觸發字詞（如果有的話）等方面的表現。

   ![](assets/spam-report-high-score.png)

1. 檢查每個專案的分數和說明。

   如果分數高於5，則會顯示警告。 這表示有些訊息在收到時可能會遭到反垃圾郵件工具封鎖或標示為垃圾郵件。

1. 根據該得分，如果您認為某些元素可以改善，請使用移至您的內容 [電子郵件設計工具](../email/content-from-scratch.md) 並進行所需的更新。

1. 完成變更後，請返回 **[!UICONTROL 垃圾郵件報告]** 畫面以確保您的分數已改善。

   ![](assets/spam-report-low-score.png)

<!--You can also check the message's alerts for warnings on potential risk of spam detection. Follow the steps below.

1. Click the **[!UICONTROL Alerts]** button on top right of the screen. [Learn more on email alerts](../email/create-email.md#check-email-alerts)

1. If **[!UICONTROL Spam checker alert]** is displayed, you should check your content for a potential risk of spam using the **[!UICONTROL Spam report]** feature as detailed above.

    ![](assets/spam-report-alert.png)
-->



