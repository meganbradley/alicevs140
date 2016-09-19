---
title: "CObList::AddHead"
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
ms.assetid: f2636a7a-cf5a-4657-a090-f4aa3b390d6f
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CObList::AddHead
Adds a new element or list of elements to the head of this list.  
  
## Syntax  
  
```  
  
      POSITION AddHead(  
   CObject* newElement   
);  
void AddHead(  
   CObList* pNewList   
);  
```  
  
#### Parameters  
 `newElement`  
 The `CObject` pointer to be added to this list.  
  
 `pNewList`  
 A pointer to another `CObList` list. The elements in `pNewList` will be added to this list.  
  
## Return Value  
 The first version returns the **POSITION** value of the newly inserted element.  
  
 The following table shows other member functions that are similar to `CObList::AddHead`.  
  
|Class|Member Function|  
|-----------|---------------------|  
|[CPtrList](../vs140/CPtrList-Class.md)|**POSITION AddHead( void\***  `newElement`  **);**<br /><br /> **void AddHead( CPtrList\***  `pNewList`  **);**|  
|[CStringList](../vs140/CStringList-Class.md)|**POSITION AddHead(const CString&**  `newElement`  **);**<br /><br /> **POSITION AddHead(LPCTSTR**  `newElement`  **);**<br /><br /> **void AddHead(CStringList\***  `pNewList`  **);**|  
  
## Remarks  
 The list can be empty before the operation.  
  
## Example  
 See [CObList::CObList](../vs140/CObList--CObList.md) for a listing of the `CAge` class.  
  
 [!CODE [NVC_MFCCollections#89](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCollections#89)]  
  
 The results from this program are as follows:  
  
 `AddHead example: A CObList with 2 elements`  
  
 `a CAge at $44A8 40`  
  
 `a CAge at $442A 21`  
  
## Requirements  
 **Header:** afxcoll.h  
  
## See Also  
 [CObList Class](../vs140/CObList-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CObList::GetHead](../vs140/CObList--GetHead.md)   
 [CObList::RemoveHead](../vs140/CObList--RemoveHead.md)