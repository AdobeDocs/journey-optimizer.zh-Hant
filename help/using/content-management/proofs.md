---
title: 傳送電子郵件校樣
description: 瞭解如何傳送電子郵件校樣。
feature: Preview, Proofs
role: User
level: Beginner
exl-id: e742c04e-2987-4466-84af-bdaf4d714552
source-git-commit: 10eaebc1d24eae4a0a149822d31ff92509d1e6f8
workflow-type: tm+mt
source-wordcount: '355'
ht-degree: 13%

---

# 使用測試設定檔資料傳送校樣 {#send-proofs}

校樣是一種特定訊息，可讓您在將訊息傳送至主要客群之前先測試訊息。校樣的收件者負責核准訊息：轉譯、內容、個人化設定、設定。

>[!NOTE]
>
>[!DNL Journey optimizer]也可讓您使用從CSV / JSON檔案上傳或手動新增的範例輸入資料，預覽和傳送校樣，以測試內容的不同變體。 [瞭解如何模擬內容變化](../test-approve/simulate-sample-input.md)

若要使用測試設定檔資料傳送電子郵件校樣，您必須先選取[測試設定檔](test-profiles.md)。 接著，請遵循下列步驟：

1. 在&#x200B;**[!UICONTROL 模擬]**&#x200B;畫面中，按一下&#x200B;**[!UICONTROL 傳送校樣]**&#x200B;按鈕。

   ![](../email/assets/send-proof-button.png)

1. 在&#x200B;**[!UICONTROL 傳送校樣]**&#x200B;視窗中，輸入收件者的電子郵件，然後按一下&#x200B;**[!UICONTROL 新增]**&#x200B;以傳送校樣給您自己或您組織的成員。

   請注意，您最多可以為校樣傳遞新增10個收件者。

   ![](../email/assets/send-proof-add.png)

1. 選取&#x200B;**測試設定檔**，以用來個人化郵件內容。

   每個校樣收件者收到的訊息數量與所選測試設定檔數量相同。 例如，如果您新增了5封收件者電子郵件並選取了10個測試設定檔，您將會傳送50封校樣訊息，而每位收件者都會收到其中10封。

1. 如有需要，您可以在校樣的主旨行新增前置詞。 僅限英數字元和特殊字元，例如。- _ ( ) [ 允許]做為主旨行的前置詞。

1. 按一下&#x200B;**[!UICONTROL 傳送證明]**。

   ![](../email/assets/send-proof-select.png)

1. 返回&#x200B;**[!UICONTROL 模擬]**&#x200B;畫面，按一下&#x200B;**[!UICONTROL 檢視校樣]**&#x200B;按鈕以檢查狀態。

   ![](../email/assets/send-proof-view.png)

建議在每次修改訊息內容後傳送校樣。

>[!NOTE]
>
>在傳送的校樣中，指向映象頁面的連結未啟用。 它僅在最終訊息中啟用。
>
>Assets/影像在任何片段/內嵌訊息中的首次發佈後，最多可在2年（730天）的傳遞內容或校訂內容中存取。 在此到期日後（730天後的任何時間）必須重新發佈，才能在隨後2年內可供存取。 在首次發佈後730天內完成的任何重新發佈，都不會將資產/影像的到期日延長至接下來的730天。
