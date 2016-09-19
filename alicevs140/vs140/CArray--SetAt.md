---
title: "CArray::SetAt"
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
ms.assetid: 1b5a4f09-ea42-4ba0-b88d-75d7339b463e
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CArray::SetAt
Sets the array element at the specified index.  
  
## Syntax  
  
```  
  
      void SetAt(  
   INT_PTR nIndex,  
   ARG_TYPE newElement   
);  
```  
  
#### Parameters  
 `nIndex`  
 An integer index that is greater than or equal to 0 and less than or equal to the value returned by [GetUpperBound](../vs140/CArray--GetUpperBound.md).  
  
 `ARG_TYPE`  
 Template parameter specifying the type of arguments used for referencing array elements.  
  
 `newElement`  
 The new element value to be stored at the specified position.  
  
## Remarks  
 `SetAt` will not cause the array to grow. Use [SetAtGrow](../vs140/CArray--SetAtGrow.md) if you want the array to grow automatically.  
  
 You must ensure that your index value represents a valid position in the array. If it is out of bounds, then the Debug version of the library asserts.  
  
## Example  
 See the example for [GetAt](../vs140/CArray--GetAt.md).  
  
## Requirements  
 **Header:** afxtempl.h  
  
## See Also  
 [CArray Class](../vs140/CArray-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CArray::GetAt](../vs140/CArray--GetAt.md)   
 [CArray::SetAtGrow](../vs140/CArray--SetAtGrow.md)   
 [CArray::ElementAt](../vs140/CArray--ElementAt.md)   
 [CArray::operator](../vs140/CArray--operator.md)