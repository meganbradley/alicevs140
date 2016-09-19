---
title: "CArray::SetAtGrow"
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
ms.assetid: eb62b6d5-7b7c-4c84-bad5-04ba0ea7f935
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CArray::SetAtGrow
Sets the array element at the specified index.  
  
## Syntax  
  
```  
  
      void SetAtGrow(  
   INT_PTR nIndex,  
   ARG_TYPE newElement   
);  
```  
  
#### Parameters  
 `nIndex`  
 An integer index that is greater than or equal to 0.  
  
 `ARG_TYPE`  
 Template parameter specifying the type of elements in the array.  
  
 `newElement`  
 The element to be added to this array. A **NULL** value is allowed.  
  
## Remarks  
 The array grows automatically if necessary (that is, the upper bound is adjusted to accommodate the new element).  
  
## Example  
 [!CODE [NVC_MFCCollections#33](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCollections#33)]  
  
## Requirements  
 **Header:** afxtempl.h  
  
## See Also  
 [CArray Class](../vs140/CArray-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CArray::GetAt](../vs140/CArray--GetAt.md)   
 [CArray::SetAt](../vs140/CArray--SetAt.md)   
 [CArray::ElementAt](../vs140/CArray--ElementAt.md)   
 [CArray::operator](../vs140/CArray--operator.md)