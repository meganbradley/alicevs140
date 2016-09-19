---
title: "CMap::CMap"
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
ms.assetid: 3808d760-ffef-4b5d-9281-ccf65b6a1ccf
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMap::CMap
Constructs an empty map.  
  
## Syntax  
  
```  
  
      CMap(  
   INT_PTR nBlockSize = 10   
);  
```  
  
#### Parameters  
 `nBlockSize`  
 Specifies the memory-allocation granularity for extending the map.  
  
## Remarks  
 As the map grows, memory is allocated in units of `nBlockSize` entries.  
  
## Example  
 [!CODE [NVC_MFCCollections#56](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCollections#56)]  
  
## Requirements  
 **Header:** afxtempl.h  
  
## See Also  
 [CMap Class](../vs140/CMap-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)