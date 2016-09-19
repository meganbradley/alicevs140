---
title: "ON_PROPNOTIFY"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 512c824e-ab5f-4880-8c5a-cac308e94b57
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ON_PROPNOTIFY
Use the `ON_PROPNOTIFY` macro to define an event sink map entry for handling property notifications from an OLE control.  
  
## Syntax  
  
```  
  
ON_PROPNOTIFY(  
theClass  
,   
id  
,   
dispid  
,   
pfnRequest  
,   
pfnChanged )  
```  
  
#### Parameters  
 `theClass`  
 The class to which this event sink map belongs.  
  
 `id`  
 The control ID of the OLE control.  
  
 `dispid`  
 The dispatch ID of the property involved in the notification.  
  
 `pfnRequest`  
 Pointer to a member function that handles the **OnRequestEdit** notification for this property. This function should have a **BOOL** return type and a **BOOL\*** parameter. This function should set the parameter to **TRUE** to allow the property to change and **FALSE** to disallow. The function should return **TRUE** to indicate the notification was handled; otherwise **FALSE**.  
  
 `pfnChanged`  
 Pointer to a member function that handles the **OnChanged** notification for this property. The function should have a **BOOL** return type and a **UINT** parameter. The function should return **TRUE** to indicate that notification was handled; otherwise **FALSE**.  
  
## Remarks  
 The `vtsParams` argument is a space-separated list of values from the **VTS_** constants. One or more of these values separated by spaces (not commas) specifies the function's parameter list. For example:  
  
 [!CODE [NVC_MFCAutomation#11](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCAutomation#11)]  
  
 specifies a list containing a short integer followed by a **BOOL**.  
  
 For a list of the **VTS_** constants, see [EVENT_CUSTOM](../vs140/EVENT_CUSTOM.md).  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [ON_EVENT_RANGE](../vs140/ON_EVENT_RANGE.md)   
 [ON_PROPNOTIFY_RANGE](../vs140/ON_PROPNOTIFY_RANGE.md)