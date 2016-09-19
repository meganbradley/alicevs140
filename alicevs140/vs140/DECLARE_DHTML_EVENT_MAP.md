---
title: "DECLARE_DHTML_EVENT_MAP"
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
ms.assetid: fb98ae1f-0abe-486b-8047-5af3c6b70c47
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# DECLARE_DHTML_EVENT_MAP
Declares a DHTML event map in a class definition.  
  
## Syntax  
  
```  
  
DECLARE_DHTML_EVENT_MAP( )  
  
```  
  
## Remarks  
 This macro is to be used in the definition of [CDHtmlDialog](../vs140/CDHtmlDialog-Class.md)-derived classes.  
  
 Use [BEGIN_DHTML_EVENT_MAP](../vs140/BEGIN_DHTML_EVENT_MAP.md) or [BEGIN_DHTML_EVENT_MAP_INLINE](../vs140/BEGIN_DHTML_EVENT_MAP_INLINE.md) to implement the map.  
  
 [DECLARE_DHTML_EVENT_MAP](#vcrefdeclare_dhtml_event_map_crosslib) declares the following function:  
  
 `virtual const DHtmlEventMapEntry* GetDHtmlEventMap( );`  
  
## Requirements  
 **Header:** afxdhtml.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [DHTML Event Maps](../vs140/DHTML-Event-Maps.md)