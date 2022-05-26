---
title: 在登錄頁中使用自定義JavaScript
description: 瞭解如何設計Journey Optimizer登錄頁的內容
feature: Landing Pages
topic: Content Management
role: User
level: Beginner
source-git-commit: f4b3a9de47e724f7b23df8a02b8106c131cf1b12
workflow-type: tm+mt
source-wordcount: '558'
ht-degree: 2%

---

# 在登錄頁中使用自定義JavaScript {#lp-custom-js}

可以使用自定義JavaScript定義登錄頁內容。 例如，如果需要執行高級樣式，或要向登錄頁添加自定義行為，則可以構建自己的控制項並在 [!DNL Journey Optimizer]。

## 將JavaScript代碼插入登錄頁

要將自定義JavaScript插入登錄頁內容，可以執行以下操作：

* 在開始建立內容時導入現有HTML內容，並選擇包含自定義JavaScript代碼的檔案。 瞭解如何導入內容 [此部分](../design/existing-content.md)。

* 從頭開始或從保存的模板中設計登錄頁。 拖放 **[!UICONTROL HTML]** 內容元件並顯示原始碼，以將JavaSCript添加到元件中。 瞭解如何使用HTML元件 [此部分](../design/content-components.md#HTML)。 <!--You can also simply switch the whole landing page content to code view and enter or paste your JavaScript code.-->

   ![](assets/lp_designer-html-component.png)

* 將JavaScript代碼直接輸入或貼上到內容設計器中。 瞭解如何編碼您自己的內容 [此部分](../design/code-content.md)。

>[!NOTE]
>
>當前無法在 [預覽登錄頁](create-lp.md#test-landing-page)。

要正確顯示登錄頁，請使用以下語法（如下各節所述）。

## 代碼初始化

要初始化JavaScript代碼，必須使用 `lpRuntimeReady` 的子菜單。 成功初始化庫後將觸發此事件。 將使用 `lpRuntime` 對象，用於公開庫方法和掛接。

`LpRuntime` 表示「登錄頁運行時」。 此對象是主庫標識符。 它將公開可在自定義JavaScript中使用的掛接、表單提交方法和其他實用方法。

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

使用掛接，可以在表單提交的生命週期中附加方法。 例如，在實際提交表單之前，可以使用掛接執行某些表單驗證。

以下是您可以使用的掛接：

| 名稱 | 說明 |
|--- |--- |
| addBeforeSubmitHook | 在提交表單之前調用的自定義掛接。 返回true以繼續提交，否則返回false以阻止提交。 |
| addBeforeSubmitHook | 在失敗的表單提交時調用的自定義掛接。 |
| addOnSuccessHook | 在成功提交表單時調用的自定義掛接。 |

**範例：**

```
//LpRuntime hooks
lpRuntime.hooks.addBeforeSubmitHook(function(){
    // Add your validation logic here.
});
```

## 自定義表單提交

下面列出的方法用於執行自定義表單提交。

>[!NOTE]
>
>由於表單提交由自定義JavaScript處理，因此需要通過設定全局變數來顯式禁用預設提交 `disableDefaultFormSubmission` 至 `true`。

| 名稱 | 說明 |
|--- |--- |
| 提交表單 | 此方法將提交表單，並處理後提交流程。 |
| submitFormPartial | 此方法還將提交表單，但將跳過後提交流程。 例如，如果您已將重定向配置為成功提交後的成功頁面，則在提交部分表單時不會發生重定向。 |

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
| getFormData | 該方法可用於 `formData` 的形式。 此對象可以傳遞到 `submitForm` 的子菜單。 |

**範例：**

```
let formData = lpRuntime.getFormData();                           // Method to generate formdata
 
lpRuntime.submitForm(formData);
```

## 使用案例

### 用例1:在提交表單之前添加驗證

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

### 用例2:部分表單提交

例如，您的表單在頁面上具有多個複選框。 選中任何複選框時，您希望此資料保存到後端，而不等待用戶按一下提交按鈕。

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

### 用例3:自定義分析標籤

使用JavaScript，您可以添加輸入欄位的偵聽器並附加自定義分析調用觸發器。

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

### 用例4:動態窗體

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
