---
title: "END_CONNECTION_POINT_MAP"
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
ms.assetid: 807c5233-b58c-49a2-a34f-3b5f4a7b1b82
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# END_CONNECTION_POINT_MAP
Marks the end of the connection point map entries.  
  
## Syntax  
  
```  
  
END_CONNECTION_POINT_MAP( )  
  
```  
  
## Remarks  
 Start your connection point map with the [BEGIN_CONNECTION_POINT_MAP](../vs140/BEGIN_CONNECTION_POINT_MAP.md) macro, add entries for each of your connection points with the [CONNECTION_POINT_ENTRY](../vs140/CONNECTION_POINT_ENTRY.md) macro, and complete the map with the `END_CONNECTION_POINT_MAP` macro.  
  
 For more information about connection points in ATL, see the article [Connection Points](../vs140/ATL-Connection-Points.md).  
  
## Example  
 [!CODE [NVC_ATL_Windowing#128](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#128)]  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [Connection Point Macros](../vs140/Connection-Point-Macros.md)   
 [Macros](../vs140/ATL-Macros.md)