---
title: "CComSafeArrayBound::operator ="
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
ms.assetid: 1218486b-ea83-4c8a-80de-94f819386ded
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComSafeArrayBound::operator =
Sets the `CComSafeArrayBound` to a new value.  
  
## Syntax  
  
```  
  
      CComSafeArrayBound & operator =(  
   const CComSafeArrayBound & bound   
) throw( );  
CComSafeArrayBound & operator =(  
   ULONG ulCount   
) throw( );  
```  
  
#### Parameters  
 `bound`  
 A `CComSafeArrayBound` object.  
  
 `ulCount`  
 The number of elements.  
  
## Return Value  
 Returns a pointer to the `CComSafeArrayBound` object.  
  
## Remarks  
 The `CComSafeArrayBound` object can be assigned using an existing `CComSafeArrayBound`, or by supplying the number of elements, in which case the lower bound is set to 0 by default.  
  
## Requirements  
 **Header:** atlsafe.h  
  
## See Also  
 [CComSafeArrayBound Class](../vs140/CComSafeArrayBound-Class.md)