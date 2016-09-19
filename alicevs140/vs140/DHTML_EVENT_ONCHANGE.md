---
title: "DHTML_EVENT_ONCHANGE"
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
ms.assetid: d1f9a85e-8a8e-41f2-bbd9-b31cd5c81e9c
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# DHTML_EVENT_ONCHANGE
Handles (at the element level) the `onchange` event. This is a nonbubbling event.  
  
## Syntax  
  
```  
  
DHTML_EVENT_ONCHANGE(  
elemName  
,   
memberFxn  
 )  
  
```  
  
#### Parameters  
 `elemName`  
 An `LPCWSTR` holding the ID of the HTML element sourcing the event.  
  
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