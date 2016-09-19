---
title: "CComSafeArray::MultiDimSetAt"
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
ms.assetid: 92d7b0af-147b-42d4-a37c-d60c5a8d162e
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComSafeArray::MultiDimSetAt
Sets the value of an element in a multidimensional array.  
  
## Syntax  
  
```  
  
      HRESULT MultiDimSetAt(  
   const LONG * alIndex,  
   const T& t   
);  
```  
  
#### Parameters  
 `alIndex`  
 Pointer to a vector of indexes for each dimension in the array. The rightmost (least significant) dimension is `alIndex`[0].  
  
 *T*  
 Specifies the value of the new element.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Remarks  
 This is a multidimensional version of [CComSafeArray::SetAt](../vs140/CComSafeArray--SetAt.md).  
  
## Requirements  
 **Header:** atlsafe.h  
  
## See Also  
 [CComSafeArray Class](../vs140/CComSafeArray-Class.md)   
 [CComSafeArray::SetAt](../vs140/CComSafeArray--SetAt.md)   
 [CComSafeArray::GetAt](../vs140/CComSafeArray--GetAt.md)   
 [CComSafeArray::MultiDimGetAt](../vs140/CComSafeArray--MultiDimGetAt.md)