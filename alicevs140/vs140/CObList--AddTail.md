---
title: "CObList::AddTail"
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
ms.assetid: 2653bf9e-0957-4870-bc4d-2279237acba1
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CObList::AddTail
Adds a new element or list of elements to the tail of this list.  
  
## Syntax  
  
```  
  
      POSITION AddTail(  
   CObject* newElement   
);  
void AddTail(  
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
  
## Remarks  
 The list can be empty before the operation.  
  
 The following table shows other member functions that are similar to `CObList::AddTail`.  
  
|Class|Member Function|  
|-----------|---------------------|  
|[CPtrList](../vs140/CPtrList-Class.md)|**POSITION AddTail( void\***  `newElement`  **);**<br /><br /> **void AddTail( CPtrList\***  `pNewList`  **);**|  
|[CStringList](../vs140/CStringList-Class.md)|**POSITION AddTail( const CString&**  `newElement`  **);**<br /><br /> **POSITION AddTail( LPCTSTR**  `newElement`  **);**<br /><br /> **void AddTail( CStringList\***  `pNewList`  **);**|  
  
## Example  
 See [CObList::CObList](../vs140/CObList--CObList.md) for a listing of the `CAge` class.  
  
 [!CODE [NVC_MFCCollections#90](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCollections#90)]  
  
 The results from this program are as follows:  
  
 `AddTail example: A CObList with 2 elements`  
  
 `a CAge at $444A 21`  
  
 `a CAge at $4526 40`  
  
## Requirements  
 **Header:** afxcoll.h  
  
## See Also  
 [CObList Class](../vs140/CObList-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CObList::GetTail](../vs140/CObList--GetTail.md)   
 [CObList::RemoveTail](../vs140/CObList--RemoveTail.md)