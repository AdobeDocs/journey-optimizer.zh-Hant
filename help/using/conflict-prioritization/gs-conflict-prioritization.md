---
title: 衝突管理與優先順序
description: 瞭解如何善用 Journey Optimizer 衝突與優先順序工具。
role: User
level: Beginner
exl-id: 9dc0cd89-d29a-42d2-a73f-d95f9c39c86e
source-git-commit: 6da1d9a3edb8a30b8f13fd0cb6a138f22459ad00
workflow-type: tm+mt
source-wordcount: '622'
ht-degree: 28%

---

# 衝突管理與優先順序 {#conflict-prioritization}

## 衝突管理與優先順序工具 {#tools}

請在 Journey Optimizer 中，管理行銷活動和歷程流量和時間非常重要，才能避免過多的互動，給客戶帶來負擔。Journey Optimizer 提供多種衝突管理和排定優先順序工具。

這些工具可用於行銷活動和單一、客群資格和閱讀客群歷程旅程。

利用這些工具，您就可以確保一切更加順暢，行銷工作更有針對性，也能在正確的時間，傳遞正確的訊息，同時避免衝突和超載。

### 衝突偵測工具

使用&#x200B;**衝突偵測工具**，您可以識別歷程與行銷活動中的潛在重疊。 這非常重要，因為同時有太多通訊可能會導致客戶疲勞。 Journey Optimizer 可讓您監控時間軸、對象重疊以及頻道設定等元素。 透過及早識別衝突，您可以調整行銷活動，以避免同時使用多則訊息轟炸客戶。

➡️ [瞭解如何偵測歷程與行銷活動中的潛在衝突](conflicts.md)

### 優先順序分數

**優先順序分數**&#x200B;可協助您控制當客戶符合多個通訊的資格時，哪些行銷活動或歷程優先。 這對於傳入頻道 (例如網頁和行動裝置) 特別有用，因為這類頻道在任何指定時間都只能顯示一個行銷活動。 透過指派每個歷程或行銷活動的優先順序分數，您可以確保最重要的訊息會先傳遞。

➡️ [瞭解如何將優先順序分數指派給歷程與行銷活動](priority-scores.md)

### 規則集

規則集可讓您&#x200B;**將多個規則**&#x200B;分組為規則集，並將其套用至您選擇的歷程和行銷活動。 這提供了更精細的精細度，以限制客戶在特定時間範圍內可以進入的頻率及歷程數，或根據通訊型別控制使用者接收訊息的頻率。

* **歷程上限與仲裁**

  規則集可讓您限制客戶在特定時間範圍內可輸入的歷程次數和頻率。 您也可以設定規則以限制設定檔的歷程專案數，或限制客戶可同時註冊的歷程數。

  此外，您可以使用仲裁設定來決定如果客戶符合多個歷程的資格，應輸入哪個歷程，並使用優先順序分數來決定最佳配適度。

  ➡️ [瞭解如何使用歷程上限和仲裁](journey-capping.md)

* **依據頻道和通訊型別的頻率限定**

  您也可以使用規則集，依通訊型別（例如「銷售」、「促銷」）設定頻率上限，以防止訊息相似的客戶超載。 您可以橫跨多個管道來控制頻率，自動排除過度請求的設定檔，以便確保帶來更美好的客戶體驗。

  ➡️ [瞭解如何依據頻道和通訊型別設定頻率上限](../conflict-prioritization/channel-capping.md)

## 護欄和限制

* **行銷活動和優先順序分數** — 在行銷活動中，優先順序分數僅適用於&#x200B;**網頁**、**應用程式內**&#x200B;和&#x200B;**程式碼型**&#x200B;傳入頻道。

* **設定檔計數器更新延遲**

  客戶進入歷程後，最長可能需要20分鐘的時間才會更新設定檔計數器值。

  如果設定檔在短時段內輸入兩個歷程，則第二個歷程可能無法正確識別已達到頻率上限，這可能會讓設定檔輸入兩個歷程。

* **歷程專案上限的名稱空間優先順序**

  只有在歷程中選取的名稱空間是沙箱中定義的最高優先順序名稱空間時，才支援專案上限。 如果尚未明確設定名稱空間優先順序，預設的最高優先順序為電子郵件。

* **在對象資格歷程中同時啟用**

  當同一個對象資格事件啟用多個對象資格歷程時，專案上限的計數將不準確。 如果計數低於上限，歷程將繼續仲裁，但將無法取得同步啟用的最新計數。
