---
title: "CObArray::Add"
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
ms.assetid: e17b99be-c6c2-4eb5-b7b7-f7c73cd014c4
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CObArray::Add
Adds a new element to the end of an array, growing the array by 1.  
  
## Syntax  
  
```  
  
      INT_PTR Add(  
   CObject* newElement   
);  
```  
  
#### Parameters  
 `newElement`  
 The `CObject` pointer to be added to this array.  
  
## Return Value  
 The index of the added element.  
  
## Remarks  
 If [SetSize](../vs140/CObArray--SetSize.md) has been used with an `nGrowBy` value greater than 1, then extra memory may be allocated. However, the upper bound will increase by only 1.  
  
 The following table shows other member functions that are similar to `CObArray::Add`.  
  
|Class|Member Function|  
|-----------|---------------------|  
|[CByteArray](../vs140/CByteArray-Class.md)|**INT_PTR Add( BYTE**  `newElement` **);**<br /><br /> **throw( CMemoryException\* );**|  
|[CDWordArray](../vs140/CDWordArray-Class.md)|**INT_PTR Add( DWORD**  `newElement`  **);**<br /><br /> **throw( CMemoryException\* );**|  
|[CPtrArray](../vs140/CPtrArray-Class.md)|**INT_PTR Add( void\***  `newElement`  **);**<br /><br /> **throw( CMemoryException\* );**|  
|[CStringArray](../vs140/CStringArray-Class.md)|**INT_PTR Add( LPCTSTR**  `newElement`  **); throw( CMemoryException\* );**<br /><br /> **INT_PTR Add(const CString&**  `newElement` **);**|  
|[CUIntArray](../vs140/CUIntArray-Class.md)|**INT_PTR Add( UINT**  `newElement`  **);**<br /><br /> **throw( CMemoryException\* );**|  
|[CWordArray](../vs140/CWordArray-Class.md)|**INT_PTR Add( WORD**  `newElement`  **);**<br /><br /> **throw( CMemoryException\* );**|  
  
## Example  
 See [CObList::CObList](../vs140/CObList--CObList.md) for a listing of the `CAge` class used in all collection examples.  
  
 [!CODE [NVC_MFCCollections#75](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCollections#75)]  
  
 The results from this program are as follows:  
  
 `Add example: A CObArray with 2 elements`  
  
 `[0] = a CAge at $442A 21`  
  
 `[1] = a CAge at $4468 40`  
  
## Requirements  
 **Header:** afxcoll.h  
  
## See Also  
 [CObArray Class](../vs140/CObArray-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CObArray::SetAt](../vs140/CObArray--SetAt.md)   
 [CObArray::SetAtGrow](../vs140/CObArray--SetAtGrow.md)   
 [CObArray::InsertAt](../vs140/CObArray--InsertAt.md)   
 [CObArray::operator](../vs140/CObArray--operator.md)