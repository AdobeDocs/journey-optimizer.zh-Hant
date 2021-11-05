---
title: 在歷程中新增訊息
description: 在歷程中新增訊息
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 4db07a9e-c3dd-4873-8bd9-ac34c860694c
source-git-commit: dc05d88773dc148dc0e5387953f49c4d03b1888f
workflow-type: tm+mt
source-wordcount: '793'
ht-degree: 3%

---

# 在歷程中新增訊息

[!DNL Journey Optimizer] 訊息功能是內建的，您只需要設計內容並發佈訊息即可。 請參閱[本節](../get-started-content.md)。然後，您只需在歷程中新增使用Journey Optimizer設計的推送或電子郵件訊息。

如果您使用協力廠商系統來傳送訊息，則可建立自訂動作。 了解更多資訊 [節](../action/action.md).

## 新增訊息活動

1. 一如既往，從事件或 **讀取區段** 活動。

   ![](../assets/jo-message0.png)

1. 從 **動作** 區段，拖放 **訊息** 活動進入畫布。

   ![](../assets/jo-message1.png)

1. 新增標籤和說明。

   ![](../assets/jo-message2.png)

1. 按一下內部 **訊息** 欄位。 隨即顯示Journey Optimizer中設計的可用訊息清單。 您可以依狀態篩選清單。

   ![](../assets/jo-message3.png)

1. 選擇訊息，然後按一下 **選擇**. 您也可以按一下「 」，直接從此畫面建立新訊息 **建立訊息**.

   ![](../assets/jo-message4-ter.png)

   如果您想檢查訊息，可以按一下 **開啟訊息** 圖示 **訊息** 欄位。 訊息會在新索引標籤中開啟。

   ![](../assets/jo-message4-bis.png)

1. 將後續步驟新增至您的歷程。

## 電子郵件參數和推播參數

此 **[!UICONTROL Email parameters]** 和 **[!UICONTROL Push parameters]** 區段顯示唯讀欄位。 您通常會在建立訊息時執行此設定。 請參閱[本節](../get-started-content.md)。

![](../assets/jo-message4.png)

若要強制指定值，您可以使用 **啟用參數覆蓋** 表徵圖。 此選項可能適用於各種用途：

* 例如，若要測試電子郵件，您可以新增您的電子郵件地址。 發佈歷程後，會傳送電子郵件給您。
* 您可以參考清單訂閱者的電子郵件地址。 看這個 [使用案例](message-to-subscribers-uc.md).

## 傳送時間最佳化{#send-time-optimization}

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_disabled"
>title="關於傳送時間最佳化"
>abstract="Adobe Journey Optimizer的「傳送時間最佳化」功能採用Adobe的AI服務，可根據歷史開啟率和點按率，預測傳送電子郵件或推送訊息的最佳時機，以最大化參與。"

Adobe Journey Optimizer的「傳送時間最佳化」功能採用Adobe的AI服務，可根據歷史開啟率和點按率，預測傳送電子郵件或推送訊息的最佳時機，以最大化參與。 使用我們的機器學習模型來排程每位使用者的個人化傳送時間，以提高訊息的開啟率和點按率。

>[!NOTE]
>
>此功能目前為測試版，僅供測試版客戶使用。 若要加入測試版計畫，請連絡Adobe客戶服務。

「傳送時間最佳化」模型會內嵌您的Adobe Journey Optimizer資料，並查看使用者層級的開啟率（針對電子郵件和推播），然後按一下率（針對電子郵件），以判斷客戶何時最有可能與您的訊息互動。 「傳送時間最佳化」至少需要一個月的訊息追蹤資料，才能提供有根據的建議。 系統會針對每位使用者使用下列分數自動選擇最佳時間：

* 一週中每天最佳的小時數，以最大化參與
* 一週中最佳的一天，以最大化參與
* 一週中最佳日期的最佳小時，以最大化參與

無論您是在說打分還是訓練，模型都會有所不同。 培訓最初每週進行，然後每季進行。 分數最初是每週，然後是每月。

* 訓練 — 用於建立分數的演算法的開發
* 計分 — 根據訓練的模型將分數應用於個別設定檔

此資訊會與使用者的設定檔一起儲存，並在歷程執行時參考，告知Adobe Journey Optimizer何時傳送訊息。

>[!CAUTION]
>
>* 此功能僅適用於啟用追蹤的電子郵件和推播的單通道訊息。
>* 必須發佈訊息。
>* 此功能與突發模式不相容。


### 啟動傳送時間最佳化{#activate-send-time-optimization}

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_email"
>title="啟動傳送時間最佳化"
>abstract="選取適當的選項按鈕，以選擇要最佳化電子郵件開啟次數還是電子郵件點進次數。 您也可以在下一個選項中輸入「傳送」的值，以括弧表示系統使用的傳送時間。"

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_push"
>title="啟動傳送時間最佳化"
>abstract="推送訊息預設為開啟選項，因為點按不適用於推送訊息。 您也可以在下一個選項中輸入「傳送」的值，以括弧表示系統使用的傳送時間。"

透過選取 **傳送時間最佳化** 從Message活動參數切換。

![](../assets/jo-message5.png)

對於電子郵件訊息，請選取適當的選項按鈕，以選擇要最佳化電子郵件開啟次數還是電子郵件點進次數。 推送訊息預設為開啟選項，因為點按不適用於推送訊息。

您也可以為 **在下一個** 選項。 如果選擇「6小時」作為值， [!DNL Journey Optimizer] 會檢查每個使用者設定檔，並在歷程執行時間起六小時內選取最佳傳送時間。
