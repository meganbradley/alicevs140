---
title: "CComSafeArrayBound::GetUpperBound"
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
ms.assetid: 81d865a5-a0ce-449b-9e44-74c088188b9d
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComSafeArrayBound::GetUpperBound
Call this method to return the upper bound.  
  
## Syntax  
  
```  
  
LONG GetUpperBound( ) const throw( );  
  
```  
  
## Return Value  
 Returns the upper bound of the `CComSafeArrayBound` object.  
  
## Remarks  
 The upper bound depends on the number of elements and the lower bound value. For example, if the lower bound is 0 and the number of elements is 10, the upper bound will automatically be set to 9.  
  
## Requirements  
 **Header:** atlsafe.h  
  
## See Also  
 [CComSafeArrayBound Class](../vs140/CComSafeArrayBound-Class.md)   
 [CComSafeArrayBound::GetCount](../vs140/CComSafeArrayBound--GetCount.md)   
 [CComSafeArrayBound::GetLowerBound](../vs140/CComSafeArrayBound--GetLowerBound.md)