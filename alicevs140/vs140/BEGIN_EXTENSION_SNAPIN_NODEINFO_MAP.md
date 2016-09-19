---
title: "BEGIN_EXTENSION_SNAPIN_NODEINFO_MAP"
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
ms.assetid: 04526ef9-2080-4629-ae9b-ff1d4686a2c3
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# BEGIN_EXTENSION_SNAPIN_NODEINFO_MAP
Marks the beginning of the snap-in extension data class map.  
  
## Syntax  
  
```  
  
BEGIN_EXTENSION_SNAPIN_NODEINFO_MAP( classname )  
```  
  
#### Parameters  
 *classname*  
 [in] The name of the snap-in extension data class.  
  
## Remarks  
 Start your snap-in extension map with the `BEGIN_EXTENSION_SNAPIN_NODEINFO_MAP` macro, add entries for each of your snap-in extension data types with the [EXTENSION_SNAPIN_NODEINFO_ENTRY](../vs140/EXTENSION_SNAPIN_NODEINFO_ENTRY.md) macro, and complete the map with the [END_EXTENSION_SNAPIN_NODEINFO_MAP](../vs140/END_EXTENSION_SNAPIN_NODEINFO_MAP.md) macro.  
  
## Example  
 [!CODE [NVC_ATL_Windowing#105](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#105)]  
  
## Requirements  
 **Header:** atlsnap.h  
  
## See Also  
 [Snap-In Object Macros](../vs140/Snap-In-Object-Macros.md)   
 [Macros](../vs140/ATL-Macros.md)   
 [END_EXTENSION_SNAPIN_NODEINFO_MAP](../vs140/END_EXTENSION_SNAPIN_NODEINFO_MAP.md)   
 [EXTENSION_SNAPIN_NODEINFO_ENTRY](../vs140/EXTENSION_SNAPIN_NODEINFO_ENTRY.md)   
 [EXTENSION_SNAPIN_DATACLASS](../vs140/EXTENSION_SNAPIN_DATACLASS.md)