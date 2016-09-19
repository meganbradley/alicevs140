---
title: "END_EXTENSION_SNAPIN_NODEINFO_MAP"
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
ms.assetid: f80a16f9-e2bf-4702-ab58-9e36208d4878
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# END_EXTENSION_SNAPIN_NODEINFO_MAP
Marks the end of the snap-in extension data class map.  
  
## Syntax  
  
```  
  
END_EXTENSION_SNAPIN_NODEINFO_MAP( )  
  
```  
  
## Remarks  
 Start your snap-in extension map with the [BEGIN_EXTENSION_SNAPIN_NODEINFO_MAP](../vs140/BEGIN_EXTENSION_SNAPIN_NODEINFO_MAP.md) macro, add entries for each of your extension snap-in data types with the [EXTENSION_SNAPIN_NODEINFO_ENTRY](../vs140/EXTENSION_SNAPIN_NODEINFO_ENTRY.md) macro, and complete the map with the `END_EXTENSION_SNAPIN_NODEINFO_MAP` macro.  
  
## Example  
 See the example for [BEGIN_EXTENSION_SNAPIN_NODEINFO_MAP](../vs140/BEGIN_EXTENSION_SNAPIN_NODEINFO_MAP.md).  
  
## Requirements  
 **Header:** atlsnap.h  
  
## See Also  
 [Snap-In Object Macros](../vs140/Snap-In-Object-Macros.md)   
 [Macros](../vs140/ATL-Macros.md)   
 [BEGIN_EXTENSION_SNAPIN_NODEINFO_MAP](../vs140/BEGIN_EXTENSION_SNAPIN_NODEINFO_MAP.md)   
 [EXTENSION_SNAPIN_NODEINFO_ENTRY](../vs140/EXTENSION_SNAPIN_NODEINFO_ENTRY.md)   
 [EXTENSION_SNAPIN_DATACLASS](../vs140/EXTENSION_SNAPIN_DATACLASS.md)