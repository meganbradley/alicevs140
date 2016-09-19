---
title: "BEGIN_DHTML_URL_EVENT_MAP"
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
ms.assetid: 471ecb6e-d13f-4bad-b787-cf28daf5743b
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# BEGIN_DHTML_URL_EVENT_MAP
Starts the definition of a DHTML and URL event map in a multipage dialog.  
  
## Syntax  
  
```  
  
BEGIN_DHTML_URL_EVENT_MAP( )  
  
```  
  
## Remarks  
 Put `BEGIN_DHTML_URL_EVENT_MAP` in the implementation file of your [CMultiPageDHtmlDialog](../vs140/CMultiPageDHtmlDialog-Class.md)-derived class. Follow it with [embedded DHTML event maps](../vs140/BEGIN_EMBED_DHTML_EVENT_MAP.md) and [URL entries](../vs140/BEGIN_URL_ENTRIES.md), and then close it with [END_DHTML_URL_EVENT_MAP](../vs140/END_DHTML_URL_EVENT_MAP.md). Include the [DECLARE_DHTML_URL_EVENT_MAP](../vs140/DECLARE_DHTML_URL_EVENT_MAP.md) macro within the class definition.  
  
## Example  
 [!CODE [NVC_MFCDocView#196](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#196)]  
  
## Requirements  
 **Header:** afxdhtml.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [Multipage DHTML and URL Event Maps (NIB)](assetId:///2a7332f0-79d7-46e4-b816-0a618c46777a)