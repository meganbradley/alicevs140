---
title: "CMapStringToOb::InitHashTable"
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
ms.assetid: f4afc8dd-0730-41c0-8a8d-39a2f49c0539
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMapStringToOb::InitHashTable
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
  
 The following table shows other member functions that are similar to `CMapStringToOb::InitHashTable`.  
  
|Class|Member Function|  
|-----------|---------------------|  
|[CMapPtrToPtr](../vs140/CMapPtrToPtr-Class.md)|**void InitHashTable( UINT**  `hashSize` **, BOOL**  `bAllocNow`  **= TRUE );**|  
|[CMapPtrToWord](../vs140/CMapPtrToWord-Class.md)|**void InitHashTable( UINT**  `hashSize` **, BOOL**  `bAllocNow`  **= TRUE );**|  
|[CMapStringToString](../vs140/CMapStringToString-Class.md)|**void InitHashTable( UINT**  `hashSize` **, BOOL**  `bAllocNow`  **= TRUE );**|  
|[CMapStringToPtr](../vs140/CMapStringToPtr-Class.md)|**void InitHashTable( UINT**  `hashSize` **, BOOL**  `bAllocNow`  **= TRUE );**|  
|[CMapWordToOb](../vs140/CMapWordToOb-Class.md)|**void InitHashTable( UINT**  `hashSize` **, BOOL**  `bAllocNow`  **= TRUE );**|  
|[CMapWordToPtr](../vs140/CMapWordToPtr-Class.md)|**void InitHashTable( UINT**  `hashSize` **, BOOL**  `bAllocNow`  **= TRUE );**|  
  
## Requirements  
 **Header:** afxcoll.h  
  
## See Also  
 [CMapStringToOb Class](../vs140/CMapStringToOb-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)