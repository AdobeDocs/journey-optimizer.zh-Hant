---
solution: Journey Optimizer
product: journey optimizer
title: 在登入頁面中使用自訂JavaScript
description: 瞭解如何在Journey Optimizer中設計登入頁面的內容
feature: Landing Pages
topic: Content Management
role: Developer
level: Experienced
keywords: 登陸，登陸頁面， javascript，程式碼
exl-id: 2a7ebead-5f09-4ea5-8f00-8b5625963290
source-git-commit: 8579acfa881f29ef3947f6597dc11d4c740c3d68
workflow-type: tm+mt
source-wordcount: '568'
ht-degree: 2%

---

# 在登入頁面中使用自訂JavaScript {#lp-custom-js}

您可以使用自訂JavaScript來定義登入頁面內容。 例如，如果您需要執行進階樣式，或想要將自訂行為新增至登入頁面，您可以建置自己的控制項，並在[!DNL Journey Optimizer]中執行。

## 將JavaScript程式碼插入登陸頁面

若要將自訂JavaScript插入登入頁面內容，您可以執行下列作業：

* 開始建立您的內容時匯入現有的HTML內容，並選取包含自訂JavaScript程式碼的檔案。 在本節[中瞭解如何匯入內容](../email/existing-content.md)。

* 從頭開始設計您的登入頁面，或是從儲存的範本進行設計。 將&#x200B;**[!UICONTROL HTML]**&#x200B;內容元件拖放至畫布中，並顯示原始程式碼，以將您的JavaScript新增至元件中。 在[本節](../email/content-components.md#HTML)中瞭解如何使用HTML元件。<!--You can also simply switch the whole landing page content to code view and enter or paste your JavaScript code.-->

  ![](assets/lp_designer-html-component.png)

* 直接在內容設計工具中輸入或貼上JavaScript程式碼。 在本節[中瞭解如何編碼您自己的內容](../email/code-content.md)。

>[!NOTE]
>
>目前當您在[預覽登入頁面](create-lp.md#test-landing-page)時，無法顯示JavaScript正在執行中。

若要正確顯示登入頁面，請依照下列各節所述使用下列語法。

## 程式碼初始化

若要將JavaScript程式碼初始化，您必須使用`lpRuntimeReady`事件。 成功初始化程式庫後，將會觸發此事件。 將使用`lpRuntime`物件執行回呼，以公開程式庫方法與掛接。

`LpRuntime`代表「登陸頁面執行階段」。 此物件是主要程式庫識別碼。 它會公開鉤點、表單提交方法，以及可用於自訂JavaScript的其他公用程式方法。

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

使用勾點，您可以在表單提交的生命週期中附加方法。 例如，您可以使用勾點在表單實際提交之前執行某些表單驗證。

以下是您可以使用的鉤點：

| 名稱 | 說明 |
|--- |--- |
| addBeforeSubmitHook | 在提交表單前要呼叫的自訂連結。 傳回true以繼續提交，否則傳回false以封鎖提交。 |
| addOnFailureHook | 要在失敗的表單提交上呼叫的自訂連結。 |
| Addonsuccessfhook | 在成功提交表單時要呼叫的自訂連結。 |

**範例：**

```
//LpRuntime hooks
lpRuntime.hooks.addBeforeSubmitHook(function(){
    // Add your validation logic here.
});
```

## 自訂表單提交

下列方法用於執行自訂表單提交。

>[!NOTE]
>
>由於表單提交是由自訂JavaScript所處理，因此需要透過將全域變數`disableDefaultFormSubmission`設定為`true`來明確停用預設提交。

| 名稱 | 說明 |
|--- |--- |
| submitform | 此方法會提交表單，並處理貼文提交流程。 |
| submitFormPart | 此方法也會提交表單，但會略過貼文提交流程。 例如，如果您已設定在提交成功後重新導向至成功頁面，則在提交部分表單時不會發生該重新導向。 |

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

## 公用程式函式

| 名稱 | 說明 |
|--- |--- |
| getFormData | 此方法可用來取得JSON物件形式的`formData`。 此物件可傳遞至`submitForm`以提交表單。 |

**範例：**

```
let formData = lpRuntime.getFormData();                           // Method to generate formdata
 
lpRuntime.submitForm(formData);
```

## 使用案例

### 使用案例1：在提交表單前新增驗證

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

### 使用案例2：部分表單提交

例如，您有一個表單在頁面上具有多個核取方塊。 核取任何核取方塊時，您想要將此資料儲存到後端，而不等待使用者按一下提交按鈕。

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

### 使用案例3：自訂分析標籤

您可以使用JavaScript新增輸入欄位的監聽器，並附加自訂分析呼叫觸發程式。

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

### 使用案例4：動態表單

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
