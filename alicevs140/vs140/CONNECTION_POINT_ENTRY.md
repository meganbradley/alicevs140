---
title: "CONNECTION_POINT_ENTRY"
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
ms.assetid: 0a7f3053-6433-49b2-a9b5-8a307e8efe14
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CONNECTION_POINT_ENTRY
Enters a connection point for the specified interface into the connection point map so that it can be accessed.  
  
## Syntax  
  
```  
  
CONNECTION_POINT_ENTRY(   
iid  
 )  
  
```  
  
#### Parameters  
 `iid`  
 [in] The GUID of the interface being added to the connection point map.  
  
## Remarks  
 Connection point entries in the map are used by [IConnectionPointContainerImpl](../vs140/IConnectionPointContainerImpl-Class.md). The class containing the connection point map must inherit from `IConnectionPointContainerImpl`.  
  
 Start your connection point map with the [BEGIN_CONNECTION_POINT_MAP](../vs140/BEGIN_CONNECTION_POINT_MAP.md) macro, add entries for each of your connection points with the `CONNECTION_POINT_ENTRY` macro, and complete the map with the [END_CONNECTION_POINT_MAP](../vs140/END_CONNECTION_POINT_MAP.md) macro.  
  
 For more information about connection points in ATL, see the article [Connection Points](../vs140/ATL-Connection-Points.md).  
  
## Example  
 [!CODE [NVC_ATL_Windowing#120](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#120)]  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [Connection Point Macros](../vs140/Connection-Point-Macros.md)   
 [Macros](../vs140/ATL-Macros.md)