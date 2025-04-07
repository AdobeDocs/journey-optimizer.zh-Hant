---
title: 使用電子郵件垃圾郵件報告
description: 瞭解如何使用電子郵件垃圾郵件報告。
feature: Preview
role: User
level: Beginner
exl-id: 9ab43b14-41cf-49f1-bdcf-6fee58db5000
source-git-commit: b6fd60b23b1a744ceb80a97fb092065b36847a41
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 17%

---

# 垃圾郵件報告 {#spam-report}

>[!CONTEXTUALHELP]
>id="ajo_simulate_spam_report"
>title="垃圾郵件報告"
>abstract="您可以使用垃圾郵件報告來檢查電子郵件內容的垃圾郵件評分。該分數表示 ISP 或信箱提供者是否會將您的郵件視為垃圾郵件。分數越低越好。如果您的電子郵件內容得分高於 2，您應該考慮修正導致測試失敗的問題。"

您可以在專用的垃圾郵件報告中檢查您的電子郵件內容垃圾郵件評分。 使用[SpamAssassin](https://spamassassin.apache.org/){target="_blank"}，Adobe Journey Optimizer可以測試您的電子郵件內容，並提供分數以指出ISP或信箱提供者是否將其視為垃圾郵件。

在編輯或預覽您的電子郵件內容時，**[!UICONTROL 垃圾郵件報告]**&#x200B;按鈕會提供評分和建議以提高所列每個個別專案的分數。

此功能可讓您判斷郵件在接收時是否會被反垃圾郵件工具視為垃圾郵件，並據此採取行動。 許多電子郵件收件匣提供者使用工具作為其垃圾郵件篩選流程的一部分。 傳送分數不佳的電子郵件可能會嚴重影響您的傳遞能力。

若要存取&#x200B;**[!UICONTROL 垃圾郵件報告]**，請遵循下列步驟。

1. 在&#x200B;**[!UICONTROL 模擬]**&#x200B;畫面中，按一下&#x200B;**[!UICONTROL 垃圾郵件報告]**&#x200B;按鈕。

   ![](assets/spam-report-button.png)

<!--
    You can also open the [Email Designer](../email/content-from-scratch.md), click the **[!UICONTROL More]** button and select **[!UICONTROL Check spam score]** from the menu.

    ![](assets/spam-report-check-score.png)
-->

1. 系統會自動執行反垃圾郵件檢查，**[!UICONTROL 垃圾郵件報告]**&#x200B;視窗會顯示結果。 它會顯示您的內容在正文版面配置、結構、影像大小、垃圾郵件觸發字詞（如果有的話）等方面的表現。

   ![](assets/spam-report-high-score.png)

1. 檢查每個專案的分數和說明。

   分數越低越好。如果分數高於5，則會顯示警告：指出某些訊息在收到時可能會遭到封鎖或標籤為垃圾訊息。 最佳實務是讓分數低於2。

   >[!NOTE]
   >
   >垃圾郵件分數是透過[SpamAssassin](https://spamassassin.apache.org/){target="_blank"}衍生，而且規則不屬於Adobe。 如需這些規則的詳細資訊，請參閱SpamAssassin檔案。
   >

1. 根據該評分，如果您認為某些元素可以改善，請在[電子郵件Designer](../email/content-from-scratch.md)中編輯您的內容並進行必要的更新。

1. 完成變更後，請瀏覽回&#x200B;**[!UICONTROL 垃圾郵件報告]**&#x200B;畫面以確保您的分數已改善。

   ![](assets/spam-report-low-score.png)

<!--You can also check the message's alerts for warnings on potential risk of spam detection. Follow the steps below.

1. Click the **[!UICONTROL Alerts]** button on top right of the screen. [Learn more about email alerts](../email/create-email.md#check-email-alerts)

1. If **[!UICONTROL Spam checker alert]** is displayed, you should check your content for a potential risk of spam using the **[!UICONTROL Spam report]** feature as detailed above.

    ![](assets/spam-report-alert.png)
-->
