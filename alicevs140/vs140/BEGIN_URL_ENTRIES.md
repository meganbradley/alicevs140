---
title: "BEGIN_URL_ENTRIES"
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
ms.assetid: 028d4de7-3e2b-48b6-8e3e-7774df6bf380
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# BEGIN_URL_ENTRIES
Starts the definition of a URL event entry map in a multipage dialog.  
  
## Syntax  
  
```  
  
BEGIN_URL_ENTRIES(  
className )  
```  
  
#### Parameters  
 `className`  
 The name of the class containing the URL event entry map. This class should derive directly or indirectly from [CMultiPageDHtmlDialog](../vs140/CMultiPageDHtmlDialog-Class.md). The URL event entry map must be inside a [DHTML and URL event map](../vs140/BEGIN_DHTML_URL_EVENT_MAP.md)).  
  
## Remarks  
 Because a multipage DHTML dialog consists of multiple HTML pages, URL event entries are used to map URLs or HTML resources to corresponding [embedded DHTML event maps](../vs140/BEGIN_EMBED_DHTML_EVENT_MAP.md). Put `URL_EVENT_ENTRY` macros between `BEGIN_URL_ENTRIES` and [END_URL_ENTRIES](../vs140/END_URL_ENTRIES.md) macros.  
  
## Example  
 See the example in [BEGIN_DHTML_URL_EVENT_MAP](../vs140/BEGIN_DHTML_URL_EVENT_MAP.md).  
  
## Requirements  
 **Header:** afxdhtml.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [Multipage DHTML and URL Event Maps (NIB)](assetId:///2a7332f0-79d7-46e4-b816-0a618c46777a)