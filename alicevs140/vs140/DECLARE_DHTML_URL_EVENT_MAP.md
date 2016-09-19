---
title: "DECLARE_DHTML_URL_EVENT_MAP"
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
ms.assetid: 03d80959-334f-44ef-b3e3-b422dca2a92f
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# DECLARE_DHTML_URL_EVENT_MAP
Declares a DHTML and URL event map in a class definition.  
  
## Syntax  
  
```  
  
DECLARE_DHTML_URL_EVENT_MAP( )  
  
```  
  
## Remarks  
 This macro is to be used in the definition of [CMultiPageDHtmlDialog](../vs140/CMultiPageDHtmlDialog-Class.md)-derived classes.  
  
 A DHTML and URL event map contains [embedded DHTML event maps](../vs140/BEGIN_EMBED_DHTML_EVENT_MAP.md) and [URL event entries](../vs140/BEGIN_URL_ENTRIES.md) to map DHTML events to handlers on a per-page basis. Use [BEGIN_DHTML_URL_EVENT_MAP](../vs140/BEGIN_DHTML_URL_EVENT_MAP.md) to implement the map.  
  
## Requirements  
 **Header:** afxdhtml.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [Multipage DHTML and URL Event Maps (NIB)](assetId:///2a7332f0-79d7-46e4-b816-0a618c46777a)