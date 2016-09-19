---
title: "SNAPINTOOLBARID_ENTRY"
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
ms.assetid: 9f7ea84b-4c34-4abd-8430-77b78a292cb7
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# SNAPINTOOLBARID_ENTRY
Use this macro to enter a toolbar ID into the Snap-In object's toolbar ID map.  
  
## Syntax  
  
```  
  
      SNAPINTOOLBARID_ENTRY(   
   id    
)  
```  
  
#### Parameters  
 `id`  
 [in] Identifies the toolbar control.  
  
## Remarks  
 The [BEGIN_SNAPINTOOLBARID_MAP](../vs140/BEGIN_SNAPINTOOLBARID_MAP.md) macro marks the beginning of the toolbar ID map; the [END_SNAPINTOOLBARID_MAP](../vs140/END_SNAPINTOOLBARID_MAP.md) macro marks the end.  
  
## Example  
 See the example for [BEGIN_SNAPINTOOLBARID_MAP](../vs140/BEGIN_SNAPINTOOLBARID_MAP.md).  
  
## Requirements  
 **Header:** atlsnap.h  
  
## See Also  
 [Snap-In Object Macros](../vs140/Snap-In-Object-Macros.md)   
 [Macros](../vs140/ATL-Macros.md)