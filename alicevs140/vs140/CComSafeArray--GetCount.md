---
title: "CComSafeArray::GetCount"
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
ms.assetid: 2bbd4653-e240-4769-aff4-5216fb8b55d3
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComSafeArray::GetCount
Returns the number of elements in the array.  
  
## Syntax  
  
```  
  
      ULONG GetCount(  
   UINT uDim = 0   
) const;  
```  
  
#### Parameters  
 `uDim`  
 The array dimension.  
  
## Return Value  
 Returns the number of elements in the array.  
  
## Remarks  
 When used with a multidimensional array, this method will return the number of elements in a specific dimension only.  
  
## Requirements  
 **Header:** atlsafe.h  
  
## See Also  
 [CComSafeArray Class](../vs140/CComSafeArray-Class.md)   
 [CComSafeArray::GetLowerBound](../vs140/CComSafeArray--GetLowerBound.md)   
 [CComSafeArray::GetUpperBound](../vs140/CComSafeArray--GetUpperBound.md)   
 [CComSafeArray::GetDimensions](../vs140/CComSafeArray--GetDimensions.md)