---
title: "DHTML_EVENT_ELEMENT"
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
ms.assetid: 0c463f83-d8ce-490c-add0-d7e082260998
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# DHTML_EVENT_ELEMENT
Handles (at the element identified by `elemName`) an event identified by `dispid`.  
  
## Syntax  
  
```  
  
DHTML_EVENT_ELEMENT(  
dispid  
,   
elemName  
,   
memberFxn  
 )  
  
```  
  
#### Parameters  
 `dispid`  
 The dispatch ID of the event to be handled.  
  
 `elemName`  
 An `LPCWSTR` holding the ID of the HTML element sourcing the event.  
  
 `memberFxn`  
 The handler function for the event.  
  
## Remarks  
 Use this macro to add an entry to the [DHTML event map](../vs140/BEGIN_DHTML_EVENT_MAP_INLINE.md) in your class.  
  
 If this macro is used to handle nonbubbling events, the source of the event will be the element identified by `elemName`.  
  
 If this macro is used to handle bubbling events, the element identified by `elemName` may not be the source of the event (the source could be any element contained by `elemName`).  
  
## Requirements  
 **Header:** afxdhtml.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [DHTML Event Maps](../vs140/DHTML-Event-Maps.md)   
 [CDHtmlDialog Class](../vs140/CDHtmlDialog-Class.md)