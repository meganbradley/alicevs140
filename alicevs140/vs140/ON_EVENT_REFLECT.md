---
title: "ON_EVENT_REFLECT"
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
ms.assetid: 35bfd07a-93cd-478e-a4c7-a11be2f38cdc
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ON_EVENT_REFLECT
The `ON_EVENT_REFLECT` macro, when used in the event sink map of an OLE control's wrapper class, receives events fired by the control before they are handled by the control's container.  
  
## Syntax  
  
```  
  
ON_EVENT_REFLECT(  
theClass  
,   
dispid  
,   
pfnHandler  
,   
vtsParams  
 )  
  
```  
  
#### Parameters  
 `theClass`  
 The class to which this event sink map belongs.  
  
 dispid  
 The dispatch ID of the event fired by the control.  
  
 `pfnHandler`  
 Pointer to a member function that handles the event. This function should have a **BOOL** return type and parameter types that match the event's parameters (see `vtsParams`). The function should return **TRUE** to indicate the event was handled; otherwise **FALSE**.  
  
 `vtsParams`  
 A sequence of **VTS_** constants that specifies the types of the parameters for the event. These are the same constants that are used in dispatch map entries such as `DISP_FUNCTION`.  
  
## Remarks  
 The `vtsParams` argument is a space-separated list of values from the **VTS_** constants.  
  
 One or more of these values separated by spaces (not commas) specifies the function's parameter list. For example:  
  
 [!CODE [NVC_MFCAutomation#11](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCAutomation#11)]  
  
 specifies a list containing a short integer followed by a **BOOL**.  
  
 For a list of the **VTS_** constants, see [EVENT_CUSTOM](../vs140/EVENT_CUSTOM.md).  
  
## Requirements  
 **Header:** afxdisp.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [ON_EVENT](../vs140/ON_EVENT.md)   
 [ON_PROPNOTIFY](../vs140/ON_PROPNOTIFY.md)   
 [ON_PROPNOTIFY_REFLECT](../vs140/ON_PROPNOTIFY_REFLECT.md)