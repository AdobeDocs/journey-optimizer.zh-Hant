---
solution: Journey Optimizer
product: journey optimizer
title: 在登錄頁面中使用自訂JavaScript
description: 了解如何在Journey Optimizer中設計登錄頁面的內容
feature: Landing Pages
topic: Content Management
role: User
level: Beginner
keywords: 登陸，登陸頁面，javascript，程式碼
exl-id: 2a7ebead-5f09-4ea5-8f00-8b5625963290
source-git-commit: c0afa3e2bc6dbcb0f2f2357eebc04285de8c5773
workflow-type: tm+mt
source-wordcount: '564'
ht-degree: 2%

---

# 在登錄頁面中使用自訂JavaScript {#lp-custom-js}

您可以使用自訂JavaScript來定義登錄頁面內容。 例如，如果您需要執行進階樣式，或想要將自訂行為新增至登錄頁面，您可以建立自己的控制項，並在 [!DNL Journey Optimizer].

## 將JavaScript程式碼插入登錄頁面

若要將自訂JavaScript插入登陸頁面內容，您可以執行下列操作：

* 開始建立內容時，請匯入現有的HTML內容，並選取包含自訂JavaScript程式碼的檔案。 了解如何匯入內容 [在本節](../email/existing-content.md).

* 從草稿開始或從儲存的範本設計您的登錄頁面。 拖放 **[!UICONTROL HTML]** 內容元件並顯示原始碼，以將您的JavaSCript新增至元件。 了解如何在 [本節](../email/content-components.md#HTML). <!--You can also simply switch the whole landing page content to code view and enter or paste your JavaScript code.-->

   ![](assets/lp_designer-html-component.png)

* 直接在內容設計器中輸入或貼上JavaScript程式碼。 了解如何編寫您自己的內容 [在本節](../email/code-content.md).

>[!NOTE]
>
>當 [預覽登錄頁面](create-lp.md#test-landing-page).

若要正確顯示登錄頁面，請使用下列語法，如以下各節所述。

## 程式碼初始化

若要初始化JavaScript程式碼，您必須使用 `lpRuntimeReady` 事件。 成功初始化程式庫後，將觸發此事件。 回呼將使用 `lpRuntime` 物件以公開程式庫方法和鈎點。

`LpRuntime` 代表「登錄頁面執行階段」。 此物件是主要程式庫識別碼。 它會公開鈎點、表單提交方法，以及可用於自訂JavaScript的其他公用程式方法。

**範例：**

```
if(window.lpRuntime){
    init(window.lpRuntime);
}else{
    window.addEventListener('lpRuntimeReady',function(e){
        init(e.detail);
    });
}
 
function init(lpRuntime){
    // Enter custom JavaScript here using methods from lpRuntime.
}
```

## 勾點

使用鈎點，您可以在表單提交的生命週期期間附加方法。 例如，您可以在實際提交表單之前，使用鈎點執行某些表單驗證。

以下是您可使用的鈎點：

| 名稱 | 說明 |
|--- |--- |
| addBeforeSubmitHook | 在提交表單前呼叫的自訂連結。 傳回true以繼續提交，否則傳回false以封鎖提交。 |
| addOnFailureHook | 在表單提交失敗時呼叫的自訂連結。 |
| addOnSuccessHook | 要在成功提交表單時呼叫的自訂連結。 |

**範例：**

```
//LpRuntime hooks
lpRuntime.hooks.addBeforeSubmitHook(function(){
    // Add your validation logic here.
});
```

## 自訂表單提交

下列方法可用來執行自訂表單提交。

>[!NOTE]
>
>由於表單提交是由自訂JavaScript處理，因此必須設定全域變數以明確停用預設提交 `disableDefaultFormSubmission` to `true`.

| 名稱 | 說明 |
|--- |--- |
| submitForm | 此方法會提交表單，並處理貼文提交流程。 |
| submitFormPartial | 此方法也會提交表單，但會略過貼文提交流程。 例如，如果您已設定成功提交成功頁面後重新導向，則在提交部分表單時不會進行重新導向。 |

**範例：**

```
//LpRuntime methods
window.disableDefaultFormSubmission = true        // Flag to disable the default submission flow.
 
lpRuntime.submitForm(formSubmissionData);         // This will trigger the default form submission handling like redirecting to error or success page.
  
lpRuntime.submitFormPartial(formSubmissionData,{   // This will not trigger the default submission handling.
    beforeSubmit : callback,
    onFailure : failureCallback,                   // Custom onFailureCallback - will be used in partial submission of form.
    onSuccess : successCallback                    // Custom onSuccessCallback - will be used in partial submission of form.
})
```

## 實用程式函式

| 名稱 | 說明 |
|--- |--- |
| getFormData | 此方法可用來取得 `formData` 以JSON物件的形式。 此物件可傳遞至 `submitForm` 提交表單。 |

**範例：**

```
let formData = lpRuntime.getFormData();                           // Method to generate formdata
 
lpRuntime.submitForm(formData);
```

## 使用案例

### 使用案例1:在提交表單前添加驗證

```
<html>
<body>
// Enter HTML body here.
  
<script>
        if(window.lpRuntime){
          console.log('got runtime',lpRuntime);
          init(window.lpRuntime);
        }else{
          window.addEventListener('lpRuntimeReady',function(e){
            init(window.lpRuntime);
          });
        }
        
  
      // Here validate the function is checking if the checkbox is selected. This method should return true if you want form submission.
      function validateForm(){
        return document.querySelector('.spectrum-Checkbox-input').checked;
      }    
  
      function init(lpRuntime){
          lpRuntime.hooks.addBeforeSubmitHook(function(){
              return validateForm(); // This method should return true if you want to proceed with submission.
          })
      }
  
</script>  
  
</body>
</html>
```

### 使用案例2:部分表單提交

例如，您的表單在頁面上有多個核取方塊。 勾選任何核取方塊時，您會希望將此資料儲存至後端，而不等待使用者按一下提交按鈕。

```
<html>
<body>
    <form>
        <input type='checkbox' value="1" name="name1"/>
        <input type='checkbox' value="2" name="name2"/>
        <input type='checkbox' value="3" name="name3"/>
        <input type='checkbox' value="4" name="name4"/>
    </form>
  
<script>
      window.disableDefaultFormSubmission=true;
 
      window.addEventListener('lpRuntimeReady',function(e){        
        init(e.detail)
      }
 
     function init(lpRuntime){
        window.getElementByTagName('input').addEventListener('change',function(e){
            let formData = lpRuntime.getFormData();
            lpRuntime.submitFormPartial(formData);
        })
      }
    </script>
  
</body>
</html>
```

### 使用案例3:自訂分析標籤

使用JavaScript，您可以新增輸入欄位的監聽器，並附加自訂分析呼叫觸發器。

```
<html>
<body>
    <form>
        <input type='checkbox' value="1" name="name1"/>
        <input type='checkbox' value="2" name="name2"/>
        <input type='checkbox' value="3" name="name3"/>
        <input type='checkbox' value="4" name="name4"/>
    </form>
  
<script>
      window.disableDefaultFormSubmission=false;  
 
      window.addEventListener('lpRuntimeReady',function(e){        
        init(e.detail)
      }
 
     function init(lpRuntime){
         window.getElementByTagName('input').addEventListener('change',function(e){
            //trigger analytics events
        })
      }
        
    </script>
  
</body>
</html>
```

### 使用案例4:動態表單

```
<html>
<body>
    <form>
        <input type='checkbox' value="1" name="name1"/>
        <div class="hiddenInput hidden">
            <input type='text' name="name2"/>
        </div>
    </form>
  
<script>
      window.disableDefaultFormSubmission=false;     
 
      window.addEventListener('lpRuntimeReady',function(e){        
        init(e.detail)
      }
 
      function init(lpRuntime){
        window.getElementByTagName('input').addEventListener('change',function(e){
            document.querySelector('.hiddenInput').toggleClass('hidden');
        })
      }
        
    </script>
  
</body>
</html>
```
