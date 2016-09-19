---
title: "CMap::InitHashTable"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: e769aa09-58f2-4f3f-b00f-383ef0b8451d
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMap::InitHashTable
Initializes the hash table.  
  
## Syntax  
  
```  
  
      void InitHashTable(  
   UINT hashSize,  
   BOOL bAllocNow = TRUE   
);  
```  
  
#### Parameters  
 `hashSize`  
 Number of entries in the hash table.  
  
 `bAllocNow`  
 If **TRUE**, allocates the hash table upon initialization; otherwise the table is allocated when needed.  
  
## Remarks  
 For best performance, the hash table size should be a prime number. To minimize collisions, the size should be roughly 20 percent larger than the largest anticipated data set.  
  
## Example  
 See the example for [CMap::Lookup](../vs140/CMap--Lookup.md).  
  
## Requirements  
 **Header:** afxtempl.h  
  
## See Also  
 [CMap Class](../vs140/CMap-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMap::GetHashTableSize](../vs140/CMap--GetHashTableSize.md)