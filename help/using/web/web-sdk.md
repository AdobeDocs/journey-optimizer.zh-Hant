---
title: 搭配使用Adobe Journey Optimizer與Experience Platform Web SDK
description: 瞭解如何使用Adobe Journey Optimizer在Experience Platform Web SDK呈現個人化內容
feature: Web Channel
topic: Content Management
role: Developer
level: Intermediate
keywords: ajo；ajo網頁；adobe journey optimizer；renderDecisions；介面；決定；主張；範圍；結構
source-git-commit: 2ab7c7b767f2f04cb4519d203d92f7f7d4611540
workflow-type: tm+mt
source-wordcount: '406'
ht-degree: 2%

---

# 搭配[!DNL Experience Platform Web SDK]使用[!DNL Adobe Journey Optimizer]

[!DNL Adobe Experience Platform] [!DNL Web SDK]可以傳送並轉譯在[!DNL Adobe Journey Optimizer]中管理的個人化體驗至Web Channel。 您可以使用WYSIWYG編輯器[!DNL Adobe Journey Optimizer] [Web Channel](get-started-web.md)或非視覺化介面[程式碼型體驗管道](../code-based/get-started-code-based.md)，來建立、啟用及傳遞您的[!DNL Journey Optimizer Web]行銷活動和個人化體驗。

## 術語 {#terminology}

**[!UICONTROL 介面]**：網頁介面是網頁或網頁上的位置，由URI識別，並將傳遞[!DNL Adobe Journey Optimizer]體驗內容。

**[!UICONTROL 主張]**：在[!DNL Adobe Journey Optimizer]中，主張與從[!DNL Journey Optimizer Campaign]中選取的體驗相關。

## 正在啟用[!DNL Adobe Journey Optimizer] {#enable-ajo}

若要開始使用[!DNL Adobe Journey Optimizer]，請遵循下列步驟。

1. 請詳閱[必要條件](web-prerequisites.md)，尤其是：
   * 設定[!DNL Adobe Experience Cloud Visual Editing Helper]。
   * 在您的[資料流](https://experienceleague.adobe.com/docs/experience-platform/datastreams/overview.html){target="_blank"}中啟用[!DNL Adobe Journey Optimizer]。
   * 啟用[!UICONTROL Edge上的Active-On合併原則]選項。

1. 將`renderDecisions`選項新增至您的事件。 將`renderDecisions`設為`true`，以在網頁表面上自動呈現傳遞的Journey Optimizer內容主張。

   ```javascript
   alloy("sendEvent", {
       ...,
       "renderDecisions": true
   })
   ```

1. 可選擇在事件中指定其他介面。 根據預設，網頁SDK會自動產生目前網頁的網頁表面，並將其納入Edge Network要求中。 如有需要，可在`sendEvent`命令的`personalization.surfaces`選項中，或在Web SDK擴充功能的對應&#x200B;**[!UICONTROL Surfaces]** [[!UICONTROL 傳送事件]動作](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/web-sdk/action-types.html#send-event){target="_blank"}設定中指定這些專案，以便在要求中包含其他介面。

   ```javascript
   alloy("sendEvent", {
       ...
       "personalization": {
           "surfaces": [ "web://my.site.com/about.html", "web://my.site.com/contact.html" ]
       }
   })
   ```

   ![extension-add-surface](assets/extension-add-surface.png)

   事件表面包含在`query.personalization.surfaces`要求欄位中：

   ```json
   {
   "events": [
       {
           "query": {
               "personalization": {
               "schemas": [
                   ...
               ],
               "decisionScopes": [
                   "__view__"
               ],
               "surfaces": [
                   "web://ajostage.weebly.com/"
               ]
               }
           },
           ...
       }
   ]
   }
   ```

1. 如同其他個人化功能，您可以新增&#x200B;**[預先隱藏程式碼片段](https://experienceleague.adobe.com/docs/experience-platform/edge/personalization/manage-flicker.html){target="_blank"}**，以便在擷取體驗時只隱藏頁面的某些部分。

## 呈現個人化內容 {#rendering-personalized-content}

如需呈現個人化內容的詳細資訊，請參閱[Adobe Experience Platform Web SDK檔案](https://experienceleague.adobe.com/docs/experience-platform/edge/personalization/rendering-personalization-content.html){target="_blank"}。

網頁介面的Adobe Journey Optimizer主張的處理方式與`__view__`決定範圍主張類似。 具體來說，當`sendEvent`命令中的`renderDecisions`選項設定為`true`時，這些將會由網頁SDK自動轉譯。

Journey Optimizer內容主張範例：

```json
{
    "scope": "web://ajostage.weebly.com/",
    "scopeDetails": {
        "correlationID": "ccfaf19c-6360-4aea-b464-0cf924db5da7",
        "characteristics": {
            "eventToken": "eyJtZXNzYWdlRXhlY3V0aW9uIjp7Im1lc3NhZ2VFeGVjdXRpb25JRCI6ImEzNDYxYTMzLTc5MjktNGQyNS1hNmMxLTVkYzM2YWY1NzRmMyIsIm1lc3NhZ2VJRCI6ImNjZmFmMTljLTYzNjAtNGFlYS1iNDY0LTBjZjkyNGRiNWRhNyIsIm1lc3NhZ2VUeXBlIjoibWFya2V0aW5nIiwiY2FtcGFpZ25JRCI6IjEzN2JmMzllLWM1ODgtNGI1My1iODQxLTJiMWZiZDYxM2JkYiIsImNhbXBhaWduVmVyc2lvbklEIjoiMTA1NzY1MmEtZWYwNS00YjE3LWExMmUtY2FlOTQyOTFhMWFjIiwiY2FtcGFpZ25BY3Rpb25JRCI6ImViNTlmODQ4LTk5ZDYtNGE1OC05YmU4LTk4MjIxODU0NmYzNiIsIm1lc3NhZ2VQdWJsaWNhdGlvbklEIjoiYzg2NzFjZmItNDdjYS00YTVjLTg4Y2YtNzYwZDFlZjU1MzQyIn0sIm1lc3NhZ2VQcm9maWxlIjp7ImNoYW5uZWwiOnsiX2lkIjoiaHR0cHM6Ly9ucy5hZG9iZS5jb20veGRtL2NoYW5uZWxzL3dlYiIsIl90eXBlIjoiaHR0cHM6Ly9ucy5hZG9iZS5jb20veGRtL2NoYW5uZWwtdHlwZXMvd2ViIn0sIm1lc3NhZ2VQcm9maWxlSUQiOiI2YTViY2I3ZC02MmYxLTQ5NDItODRkMC02MzE5ZjM5Zjk1ZGUifX0="
        },
        "decisionProvider": "AJO",
        "activity": {
            "id": "137bf39e-c588-4b53-b841-2b1fbd613bdb#eb59f848-99d6-4a58-9be8-982218546f36"
        }
    },
    "id": "002321c0-dff5-4153-b171-a9dfb70b9750",
    "items": [
        {
            "schema": "https://ns.adobe.com/personalization/dom-action",
            "data": {
                "uiData": {
                    "tagType": "Text",
                    "actionType": "changed"
                },
                "content": "Welcome AJO!",
                "prehidingSelector": "#wsite-content > DIV:nth-of-type(2) > DIV:nth-of-type(1) > DIV:nth-of-type(1) > DIV:nth-of-type(1) > DIV:nth-of-type(1) > DIV:nth-of-type(3) > FONT:nth-of-type(1) > SPAN:nth-of-type(1)",
                "type": "setHtml",
                "selector": "#wsite-content > DIV.wsite-section-wrap:eq(1) > DIV.wsite-section:eq(0) > DIV.wsite-section-content:eq(0) > DIV.container:eq(0) > DIV.wsite-section-elements:eq(0) > DIV.paragraph:eq(0) > FONT:nth-of-type(1) > SPAN:nth-of-type(1)"
            },
            "id": "0a522f66-9e6a-4ded-b1d0-e9167f103290"
        }
    ]
}
```

## 除錯 {#debugging}

若要偵錯Adobe Journey Optimizer個人化實作，請使用[Web SDK偵錯](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/debugging.html){target="_blank"}。 使用[[!DNL Adobe Experience Platform Assurance]](https://developer.adobe.com/client-sdks/documentation/platform-assurance/)進行疑難排解時，有[!DNL Adobe Journey Optimizer]個偵錯追蹤可供使用。 檢查具有`AJO:`首碼的事件。

![assurance-ajo-trace](assets/assurance-ajo-trace.png)
