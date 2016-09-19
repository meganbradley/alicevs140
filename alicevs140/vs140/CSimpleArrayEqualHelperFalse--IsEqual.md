---
title: "CSimpleArrayEqualHelperFalse::IsEqual"
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
ms.assetid: fb289ea3-2309-45fe-b1ba-40c2d688dcfd
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSimpleArrayEqualHelperFalse::IsEqual
Returns false.  
  
## Syntax  
  
```  
  
      static bool IsEqual(  
   const T& ,  
   const T&   
);  
```  
  
## Return Value  
 Returns false.  
  
## Remarks  
 This method always returns false, and will call `ATLASSERT` with an argument of false if referenced. The purpose of `CSimpleArrayEqualHelperFalse::IsEqual` is to force methods using comparisons to fail in a well-defined manner when equality tests have not been adequately defined.  
  
## Requirements  
 **Header:** atlsimpcoll.h  
  
## See Also  
 [CSimpleArrayEqualHelperFalse Class](../vs140/CSimpleArrayEqualHelperFalse-Class.md)