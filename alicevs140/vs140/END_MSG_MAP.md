---
title: "END_MSG_MAP"
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
ms.assetid: 5eaf5b69-6846-4c43-8e9c-be940ca13bee
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# END_MSG_MAP
Marks the end of a message map.  
  
## Syntax  
  
```  
  
END_MSG_MAP( )  
  
```  
  
## Remarks  
 Always use the [BEGIN_MSG_MAP](../vs140/BEGIN_MSG_MAP.md) macro to mark the beginning of a message map. Use [ALT_MSG_MAP](../vs140/ALT_MSG_MAP.md) to declare subsequent alternate message maps.  
  
 Note that there is always exactly one instance of `BEGIN_MSG_MAP` and `END_MSG_MAP`.  
  
 For more information about using message maps in ATL, see [Message Maps](../vs140/Message-Maps--ATL-.md).  
  
## Example  
 The following example shows the default message map and one alternate message map, each containing one handler function:  
  
 [!CODE [NVC_ATL_Windowing#98](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#98)]  
  
 The next example shows two alternate message maps. The default message map is empty.  
  
 [!CODE [NVC_ATL_Windowing#99](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#99)]  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [Message Map Macros](../vs140/Message-Map-Macros--ATL-.md)   
 [Macros](../vs140/ATL-Macros.md)