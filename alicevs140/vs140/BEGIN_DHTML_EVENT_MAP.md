---
title: "BEGIN_DHTML_EVENT_MAP"
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
ms.assetid: b54a8c7c-a146-4813-9867-09ba51b36c93
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# BEGIN_DHTML_EVENT_MAP
Marks the beginning of the DHTML event map when placed in the source file for the class identified by `className`.  
  
## Syntax  
  
```  
  
BEGIN_DHTML_EVENT_MAP(  
className  
 )  
  
```  
  
#### Parameters  
 `className`  
 The name of the class containing the DHTML event map. This class should derive directly or indirectly from [CDHtmlDialog](../vs140/CDHtmlDialog-Class.md) and include the [DECLARE_DHTML_EVENT_MAP](../vs140/DECLARE_DHTML_EVENT_MAP.md) macro within its class definition.  
  
## Remarks  
 Add a DHTML event map to your class to provide information to **CDHtmlDialog** that can be used to route events fired by HTML elements or ActiveX controls in a web page to handler functions in your class.  
  
 Place the `BEGIN_DHTML_EVENT_MAP` macro in the class's implementation (.cpp) file followed by `DHTML_EVENT` macros for the events the class is to handle (for example, `DHTML_EVENT_ONMOUSEOVER` for mouseover events). Use the [END_DHTML_EVENT_MAP](../vs140/END_DHTML_EVENT_MAP.md) macro to mark the end of the event map. These macros implement the following function:  
  
 `virtual const DHtmlEventMapEntry* GetDHtmlEventMap();`  
  
## Requirements  
 **Header:** afxdhtml.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [DHTML Event Maps](../vs140/DHTML-Event-Maps.md)   
 [BEGIN_DHTML_EVENT_MAP_INLINE](../vs140/BEGIN_DHTML_EVENT_MAP_INLINE.md)