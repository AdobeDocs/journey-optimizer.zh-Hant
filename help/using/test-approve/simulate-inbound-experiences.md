---
title: 模擬傳入動作
description: 瞭解如何在啟用前在Action行銷活動中模擬傳入體驗。
feature: Campaigns, Preview
topic: Content Management
role: User
level: Beginner
badge: label="Private Beta" type="Informative"
hide: true
exl-tag: PrivateBeta
source-git-commit: 916b5875a96eae7b0a4aca86fe35022f21841dd8
workflow-type: tm+mt
source-wordcount: '448'
ht-degree: 2%
---

# 模擬傳入體驗 {#simulate-inbound-experiences}

>[!BEGINSHADEBOX]

**在此頁面上：**&#x200B;在模擬使用者上線之前，驗證傳入動作行銷活動體驗，包括連結和QR預覽、模擬行為和金鑰限制。

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>此功能目前在Private Beta中。 如欲請求存取權，請和您的 Adobe 代表聯絡。

## 概觀 {#inbound-simulation-overview}

傳入體驗模擬可讓您在行銷活動上線之前，驗證具有模擬使用者的&#x200B;**動作行銷活動**&#x200B;的個人化傳入體驗。 用它來驗證目標、決策、轉譯內容，以及排除網頁和行動預覽路徑中的行為。

當模擬模式啟動時，行銷活動會進入&#x200B;**[!UICONTROL 模擬]**&#x200B;狀態。 您可以在模擬保持作用中時導覽離開並稍後返回，且行銷活動內容和設定會鎖定以進行編輯（類似於已發佈狀態）。 模擬體驗不會公開給您的生產對象。

如需完整的行銷活動檢閱流程，包括內容預覽和模擬內容，請參閱[檢閱並啟用動作行銷活動](../campaigns/review-activate-campaign.md)。

## 進入並執行模擬模式 {#enter-simulation-mode}

若要進入模擬模式，請執行下列動作：

1. 在動作行銷活動中，存取&#x200B;**[!UICONTROL 檢閱以啟動]**&#x200B;介面，然後選取&#x200B;**[!UICONTROL 模擬動作]**&#x200B;標籤。

   ![](assets/simulation-mode-enter.png)

1. 使用下列其中一個可用方法，選取您要用於模擬的模擬使用者：

   * **[!UICONTROL 瀏覽詳細目錄]** — 選取先前建立的模擬使用者。
   * **[!UICONTROL 從表單]**&#x200B;建立 — 依欄位建立模擬使用者欄位。
   * **[!UICONTROL 從JSON建立]** — 匯入JSON檔案模擬的使用者設定檔裝載。

   ![](assets/simulation-mode-ui.png)

   如需建立和管理模擬使用者的詳細資訊，請參閱[建立和管理模擬使用者](../building-journeys/simulate-journey.md#test-users)。

1. 選取或建立模擬使用者後，它們會顯示在中央窗格中。 對於每個使用者，您可以檢視詳細資訊、更新使用者資訊，或從模擬清單中移除使用者。

   ![](assets/simulation-mode-users.png)

1. 若要為每個使用者產生模擬輸出，請按一下&#x200B;**[!UICONTROL 產生連結]**&#x200B;按鈕。 這會產生：

   * 可共用的URL，用於預覽所選使用者轉譯的傳入體驗。
   * 行動裝置預覽情境的QR碼。

1. 對於每個模擬的使用者，使用產生的控制項來驗證體驗：

   ![](assets/simulation-mode-generate.png)

   | 按鈕 | 作用 |
   | --- | --- |
   | ![開啟連結按鈕](assets/simulation-action-open.png) | 在瀏覽器中開啟剛才產生的連結，即可預覽該模擬使用者的傳入體驗。 |
   | ![複製連結按鈕](assets/simulation-action-copy.png) | 複製產生的連結，以便共用或貼到其他瀏覽器或裝置。 |
   | ![QR碼按鈕](assets/simulation-action-qr.png) | 開啟QR碼（如果頻道可以使用），選取&#x200B;**[!UICONTROL iOS]**&#x200B;或&#x200B;**[!UICONTROL Android]**，使用裝置相機掃描該碼，然後在出現提示時輸入顯示的碼。 |
   | ![其他動作按鈕](assets/simulation-action-more.png) | 開啟其他選項以&#x200B;**[!UICONTROL 開啟保證工作階段]**&#x200B;或&#x200B;**[!UICONTROL 新的保證工作階段]**，並在Assurance使用者介面中繼續疑難排解。 |

1. 您可以隨時離開模擬模式，方法是按一下行銷活動動作列中的&#x200B;**[!UICONTROL 停止模擬]**，例如，如果您需要返回並編輯行銷活動。
