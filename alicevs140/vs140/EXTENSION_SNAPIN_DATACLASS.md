---
title: "EXTENSION_SNAPIN_DATACLASS"
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
ms.assetid: bb6d0a0e-3984-49d2-a37c-71fc62b10d57
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# EXTENSION_SNAPIN_DATACLASS
Adds a data member to the snap-in extension data class for an **ISnapInItemImpl**-derived class.  
  
## Syntax  
  
```  
  
      EXTENSION_SNAPIN_DATACLASS(   
   dataClass    
)  
```  
  
#### Parameters  
 `dataClass`  
 [in] The data class of the snap-in extension.  
  
## Remarks  
 This class should also be entered into a snap-in extension data class map. Start your snap-in extension data class map with the [BEGIN_EXTENSION_SNAPIN_NODEINFO_MAP](../vs140/BEGIN_EXTENSION_SNAPIN_NODEINFO_MAP.md) macro, add entries for each of your snap-in extension data types with the [EXTENSION_SNAPIN_NODEINFO_ENTRY](../vs140/EXTENSION_SNAPIN_NODEINFO_ENTRY.md) macro, and complete the map with the [END_EXTENSION_SNAPIN_NODEINFO_MAP](../vs140/END_EXTENSION_SNAPIN_NODEINFO_MAP.md) macro.  
  
## Example  
 [!CODE [NVC_ATL_Windowing#105](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#105)]  
  
## Requirements  
 **Header:** atlsnap.h  
  
## See Also  
 [Snap-In Object Macros](../vs140/Snap-In-Object-Macros.md)   
 [Macros](../vs140/ATL-Macros.md)   
 [BEGIN_EXTENSION_SNAPIN_NODEINFO_MAP](../vs140/BEGIN_EXTENSION_SNAPIN_NODEINFO_MAP.md)   
 [EXTENSION_SNAPIN_NODEINFO_ENTRY](../vs140/EXTENSION_SNAPIN_NODEINFO_ENTRY.md)   
 [END_EXTENSION_SNAPIN_NODEINFO_MAP](../vs140/END_EXTENSION_SNAPIN_NODEINFO_MAP.md)