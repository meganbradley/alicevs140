---
title: "CObList::FindIndex"
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
ms.assetid: 87549ed5-6d5e-457c-8d8b-4299205f7b81
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CObList::FindIndex
Uses the value of `nIndex` as an index into the list.  
  
## Syntax  
  
```  
  
      POSITION FindIndex(  
   INT_PTR nIndex   
) const;  
```  
  
#### Parameters  
 `nIndex`  
 The zero-based index of the list element to be found.  
  
## Return Value  
 A **POSITION** value that can be used for iteration or object pointer retrieval; **NULL** if `nIndex` is too large. (The framework generates an assertion if `nIndex` is negative.)  
  
## Remarks  
 It starts a sequential scan from the head of the list, stopping on the *n*th element.  
  
 The following table shows other member functions that are similar to `CObList::FindIndex`.  
  
|Class|Member Function|  
|-----------|---------------------|  
|[CPtrList](../vs140/CPtrList-Class.md)|**POSITION FindIndex( INT_PTR**  `nIndex`  **) const;**|  
|[CStringList](../vs140/CStringList-Class.md)|**POSITION FindIndex( INT_PTR**  `nIndex`  **) const;**|  
  
## Example  
 See [CObList::CObList](../vs140/CObList--CObList.md) for a listing of the `CAge` class.  
  
 [!CODE [NVC_MFCCollections#94](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCollections#94)]  
  
## Requirements  
 **Header:** afxcoll.h  
  
## See Also  
 [CObList Class](../vs140/CObList-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CObList::Find](../vs140/CObList--Find.md)   
 [CObList::GetNext](../vs140/CObList--GetNext.md)   
 [CObList::GetPrev](../vs140/CObList--GetPrev.md)