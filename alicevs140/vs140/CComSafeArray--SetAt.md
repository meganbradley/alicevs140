---
title: "CComSafeArray::SetAt"
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
ms.assetid: 2f8d89ee-8442-4da2-bbde-e68643ff6720
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComSafeArray::SetAt
Sets the value of an element in a single-dimensional array.  
  
## Syntax  
  
```  
  
      HRESULT SetAt(  
   LONG lIndex,  
   const T& t,  
   BOOL bCopy = TRUE  
);  
```  
  
#### Parameters  
 `lIndex`  
 The index number of the array element to set.  
  
 *t*  
 The new value of the specified element.  
  
 `bCopy`  
 Indicates whether a copy of the data should be created. The default value is **TRUE**.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Remarks  
 The `bCopy` flag is taken into account when elements of type `BSTR` or **VARIANT** are added to an array. The default value of **TRUE** ensures that a new copy is made of the data when the element is added to the array.  
  
## Requirements  
 **Header:** atlsafe.h  
  
## See Also  
 [CComSafeArray Class](../vs140/CComSafeArray-Class.md)   
 [CComSafeArray::GetAt](../vs140/CComSafeArray--GetAt.md)   
 [CComSafeArray::MultiDimSetAt](../vs140/CComSafeArray--MultiDimSetAt.md)