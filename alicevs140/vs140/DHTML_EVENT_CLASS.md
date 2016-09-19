---
title: "DHTML_EVENT_CLASS"
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
ms.assetid: 9edb5a0c-533d-44fb-9dee-41b017830a74
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# DHTML_EVENT_CLASS
Handles (at the document level) an event identified by `dispid` originated by any HTML element with the CSS class identified by `elemName`.  
  
## Syntax  
  
```  
  
DHTML_EVENT_CLASS(  
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
 An `LPCWSTR` holding the CSS class of the HTML elements sourcing the event.  
  
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