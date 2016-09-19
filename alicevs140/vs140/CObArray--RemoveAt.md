---
title: "CObArray::RemoveAt"
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
ms.assetid: 77597227-03e5-462b-b828-e2a9278f5345
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CObArray::RemoveAt
Removes one or more elements starting at a specified index in an array.  
  
## Syntax  
  
```  
  
      void RemoveAt(  
   INT_PTR nIndex,  
   INT_PTR nCount = 1   
);  
```  
  
#### Parameters  
 `nIndex`  
 An integer index that is greater than or equal to 0 and less than or equal to the value returned by `GetUpperBound`.  
  
 `nCount`  
 The number of elements to remove.  
  
## Remarks  
 In the process, it shifts down all the elements above the removed element(s). It decrements the upper bound of the array but does not free memory.  
  
 If you try to remove more elements than are contained in the array above the removal point, then the Debug version of the library asserts.  
  
 The `RemoveAt` function removes the `CObject` pointer from the array, but it does not delete the object itself.  
  
 The following table shows other member functions that are similar to `CObArray::RemoveAt`.  
  
|Class|Member Function|  
|-----------|---------------------|  
|[CByteArray](../vs140/CByteArray-Class.md)|**void RemoveAt( INT_PTR**  `nIndex` **, INT_PTR**  `nCount`  **= 1 );**|  
|[CDWordArray](../vs140/CDWordArray-Class.md)|**void RemoveAt( INT_PTR**  `nIndex` **, INT_PTR**  `nCount`  **= 1 );**|  
|[CPtrArray](../vs140/CPtrArray-Class.md)|**void RemoveAt( INT_PTR**  `nIndex` **, INT_PTR**  `nCount`  **= 1 );**|  
|[CStringArray](../vs140/CStringArray-Class.md)|**void RemoveAt( INT_PTR**  `nIndex` **, INT_PTR**  `nCount`  **= 1 );**|  
|[CUIntArray](../vs140/CUIntArray-Class.md)|**void RemoveAt( INT_PTR**  `nIndex` **, INT_PTR**  `nCount`  **= 1 );**|  
|[CWordArray](../vs140/CWordArray-Class.md)|**void RemoveAt( INT_PTR** `nIndex` **, INT_PTR**  *nCount*  **= 1 );**|  
  
## Example  
 See [CObList::CObList](../vs140/CObList--CObList.md) for a listing of the `CAge` class used in all collection examples.  
  
 [!CODE [NVC_MFCCollections#112](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCollections#112)]  
  
 The results from this program are as follows:  
  
 `RemoveAt example: A CObArray with 1 elements`  
  
 `[0] = a CAge at $4606 40`  
  
## Requirements  
 **Header:** afxcoll.h  
  
## See Also  
 [CObArray Class](../vs140/CObArray-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CObArray::SetAt](../vs140/CObArray--SetAt.md)   
 [CObArray::SetAtGrow](../vs140/CObArray--SetAtGrow.md)   
 [CObArray::InsertAt](../vs140/CObArray--InsertAt.md)