---
title: "EXTENSION_SNAPIN_NODEINFO_ENTRY"
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
ms.assetid: ad0757c7-db65-49d2-b148-36d7a90832ec
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# EXTENSION_SNAPIN_NODEINFO_ENTRY
Adds a snap-in extension data class to the snap-in extension data class map.  
  
## Syntax  
  
```  
  
      EXTENSION_SNAPIN_NODEINFO_ENTRY(   
   dataClass    
)  
```  
  
#### Parameters  
 `dataClass`  
 [in] The data class of the snap-in extension.  
  
## Remarks  
 Start your snap-in extension data class map with the [BEGIN_EXTENSION_SNAPIN_NODEINFO_MAP](../vs140/BEGIN_EXTENSION_SNAPIN_NODEINFO_MAP.md) macro, add entries for each of your snap-in extension data types with the `EXTENSION_SNAPIN_NODEINFO_ENTRY` macro, and complete the map with the [END_EXTENSION_SNAPIN_NODEINFO_MAP](../vs140/END_EXTENSION_SNAPIN_NODEINFO_MAP.md) macro.  
  
## Example  
 See the example for [BEGIN_EXTENSION_SNAPIN_NODEINFO_MAP](../vs140/BEGIN_EXTENSION_SNAPIN_NODEINFO_MAP.md).  
  
## Requirements  
 **Header:** atlsnap.h  
  
## See Also  
 [Snap-In Object Macros](../vs140/Snap-In-Object-Macros.md)   
 [Macros](../vs140/ATL-Macros.md)   
 [BEGIN_EXTENSION_SNAPIN_NODEINFO_MAP](../vs140/BEGIN_EXTENSION_SNAPIN_NODEINFO_MAP.md)   
 [END_EXTENSION_SNAPIN_NODEINFO_MAP](../vs140/END_EXTENSION_SNAPIN_NODEINFO_MAP.md)   
 [EXTENSION_SNAPIN_DATACLASS](../vs140/EXTENSION_SNAPIN_DATACLASS.md)