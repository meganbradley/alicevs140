---
title: "CAtlMap::InitHashTable"
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
ms.assetid: 1faecd3e-160c-4027-8808-5862bfcb6b63
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlMap::InitHashTable
Call this method to initialize the hash table.  
  
## Syntax  
  
```  
  
      bool InitHashTable(  
   UINT nBins,  
   bool bAllocNow = true   
);  
```  
  
#### Parameters  
 `nBins`  
 The number of bins used by the hash table. See [CAtlMap::CAtlMap](../vs140/CAtlMap--CAtlMap.md) for an explanation.  
  
 `bAllocNow`  
 A flag indication when memory should be allocated.  
  
## Return Value  
 Returns **true** on successful initialization, **false** on failure.  
  
## Remarks  
 `InitHashTable` must be called before any elements are stored in the hash table.  If this method is not called explicitly, it will be called automatically the first time an element is added using the bin count specified by the **CAtlMap** constructor.  Otherwise, the map will be initialized using the new bin count specified by the `nBins` parameter.  
  
 If the `bAllocNow` parameter is false, the memory required by the hash table will not be allocated until it is first required. This can be useful if it is uncertain if the map will be used.  
  
## Example  
 See the example for [CAtlMap::CAtlMap](../vs140/CAtlMap--CAtlMap.md).  
  
## Requirements  
 **Header:** atlcoll.h  
  
## See Also  
 [CAtlMap Class](../vs140/CAtlMap-Class.md)