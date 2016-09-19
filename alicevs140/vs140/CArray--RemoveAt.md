---
title: "CArray::RemoveAt"
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
ms.assetid: 27c8d85a-b8b8-4aed-bb23-97e92b06f3e9
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CArray::RemoveAt
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
 An integer index that is greater than or equal to 0 and less than or equal to the value returned by [GetUpperBound](../vs140/CArray--GetUpperBound.md).  
  
 `nCount`  
 The number of elements to remove.  
  
## Remarks  
 In the process, it shifts down all the elements above the removed element(s). It decrements the upper bound of the array but does not free memory.  
  
 If you try to remove more elements than are contained in the array above the removal point, then the Debug version of the library asserts.  
  
## Example  
 [!CODE [NVC_MFCCollections#32](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCollections#32)]  
  
## Requirements  
 **Header:** afxtempl.h  
  
## See Also  
 [CArray Class](../vs140/CArray-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CArray::SetAt](../vs140/CArray--SetAt.md)   
 [CArray::SetAtGrow](../vs140/CArray--SetAtGrow.md)   
 [CArray::InsertAt](../vs140/CArray--InsertAt.md)