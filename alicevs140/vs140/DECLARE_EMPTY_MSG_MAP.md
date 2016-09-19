---
title: "DECLARE_EMPTY_MSG_MAP"
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
ms.topic: reference
ms.assetid: fa78c82a-fb48-433c-85dc-a253e40ba07a
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# DECLARE_EMPTY_MSG_MAP
Declares an empty message map.  
  
## Syntax  
  
```  
  
DECLARE_EMPTY_MSG_MAP( )  
  
```  
  
## Remarks  
 `DECLARE_EMPTY_MSG_MAP` is a convenience macro that calls the macros [BEGIN_MSG_MAP](../vs140/BEGIN_MSG_MAP.md) and [END_MSG_MAP](../vs140/END_MSG_MAP.md) to create an empty message map:  
  
 [!CODE [NVC_ATL_Windowing#122](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#122)]  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [Message Map Macros](../vs140/Message-Map-Macros--ATL-.md)   
 [Macros](../vs140/ATL-Macros.md)