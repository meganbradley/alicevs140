---
title: "DHTML_EVENT_AXCONTROL"
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
ms.assetid: b20f8e2a-e007-4f52-a1b2-e27e307a7127
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# DHTML_EVENT_AXCONTROL
Handles the event identified by `dispid` fired by the ActiveX control identified by `controlName`.  
  
## Syntax  
  
```  
  
DHTML_EVENT_AXCONTROL(  
dispid  
,   
controlName  
,   
memberFxn  
 )  
  
```  
  
#### Parameters  
 `dispid`  
 The dispatch ID of the event to be handled.  
  
 `controlName`  
 An `LPCWSTR` holding the HTML ID of the control firing the event.  
  
 `memberFxn`  
 The handler function for the event.  
  
## Remarks  
 Use this macro to add an entry to the [DHTML event map](../vs140/BEGIN_DHTML_EVENT_MAP_INLINE.md) in your class.  
  
## Requirements  
 **Header:** afxdhtml.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [DHTML Event Maps](../vs140/DHTML-Event-Maps.md)   
 [CDHtmlDialog Class](../vs140/CDHtmlDialog-Class.md)