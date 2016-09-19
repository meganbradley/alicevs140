---
title: "CObList::CObList"
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
ms.assetid: ba0bdf10-7749-416d-9eba-039bfc61299c
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CObList::CObList
Constructs an empty `CObject` pointer list.  
  
## Syntax  
  
```  
  
      CObList(  
   INT_PTR nBlockSize = 10   
);  
```  
  
#### Parameters  
 `nBlockSize`  
 The memory-allocation granularity for extending the list.  
  
## Remarks  
 As the list grows, memory is allocated in units of `nBlockSize` entries. If a memory allocation fails, a `CMemoryException` is thrown.  
  
 The following table shows other member functions that are similar to `CObList::CObList`.  
  
|Class|Member Function|  
|-----------|---------------------|  
|[CPtrList](../vs140/CPtrList-Class.md)|**CPtrList( INT_PTR**  `nBlockSize`  **= 10 );**|  
|[CStringList](../vs140/CStringList-Class.md)|**CStringList( INT_PTR**  `nBlockSize`  **= 10 );**|  
  
## Example  
 Below is a listing of the `CObject`-derived class `CAge` used in all the collection examples:  
  
 [!CODE [NVC_MFCCollections#91](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCollections#91)]  
  
 Below is an example of `CObList` constructor usage:  
  
 [!CODE [NVC_MFCCollections#92](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCollections#92)]  
  
## Requirements  
 **Header:** afxcoll.h  
  
## See Also  
 [CObList Class](../vs140/CObList-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)