---
title: "CRBMultiMap::CRBMultiMap"
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
ms.assetid: 2102e839-1a86-4601-b092-e5e79427b1c3
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRBMultiMap::CRBMultiMap
The constructor.  
  
## Syntax  
  
```  
  
      explicit CRBMultiMap(  
   size_t nBlockSize = 10   
) throw( );  
```  
  
#### Parameters  
 `nBlockSize`  
 The block size.  
  
## Remarks  
 The `nBlockSize` parameter is a measure of the amount of memory allocated when a new element is required. Larger block sizes reduce calls to memory allocation routines, but use more resources. The default will allocate space for 10 elements at a time.  
  
 See the documentation for the base class [CRBTree](../vs140/CRBTree-Class.md) for information on the other methods available.  
  
## Example  
 [!CODE [NVC_ATL_Utilities#85](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#85)]  
  
## Requirements  
 **Header:** atlcoll.h  
  
## See Also  
 [CRBMultiMap Class](../vs140/CRBMultiMap-Class.md)   
 [CRBMultiMap::~CRBMultiMap](../vs140/CRBMultiMap--~CRBMultiMap.md)