---
title: "END_DHTML_URL_EVENT_MAP"
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
ms.assetid: cc4b8972-648d-4b13-a81f-bef6e52356d3
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# END_DHTML_URL_EVENT_MAP
Marks the end of a DHTML and URL event map.  
  
## Syntax  
  
```  
  
END_DHTML_URL_EVENT_MAP(  
className  
)  
  
```  
  
#### Parameters  
 `className`  
 The name of the class containing the event map. This class should derive directly or indirectly from [CMultiPageDHtmlDialog](../vs140/CMultiPageDHtmlDialog-Class.md). This should match `className` in the corresponding [BEGIN_DHTML_URL_EVENT_MAP](../vs140/BEGIN_DHTML_URL_EVENT_MAP.md) macro.  
  
## Example  
 See the example in [BEGIN_DHTML_URL_EVENT_MAP](../vs140/BEGIN_DHTML_URL_EVENT_MAP.md).  
  
## Requirements  
 **Header:** afxdhtml.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [Multipage DHTML and URL Event Maps (NIB)](assetId:///2a7332f0-79d7-46e4-b816-0a618c46777a)