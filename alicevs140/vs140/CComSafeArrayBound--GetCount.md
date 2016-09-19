---
title: "CComSafeArrayBound::GetCount"
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
ms.assetid: 7c33d699-225d-4570-8368-ce11754c4d6b
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComSafeArrayBound::GetCount
Call this method to return the number of elements.  
  
## Syntax  
  
```  
  
ULONG GetCount( ) const throw( );  
  
```  
  
## Return Value  
 Returns the number of elements.  
  
## Remarks  
 If the associated `CComSafeArray` object represents a multidimensional array, this method will only return the total number of elements in the rightmost dimension. Use [CComSafeArray::GetCount](../vs140/CComSafeArray--GetCount.md) to obtain the total number of elements.  
  
## Requirements  
 **Header:** atlsafe.h  
  
## See Also  
 [CComSafeArrayBound Class](../vs140/CComSafeArrayBound-Class.md)   
 [CComSafeArray::GetCount](../vs140/CComSafeArray--GetCount.md)