---
title: "CSimpleMapEqualHelperFalse::IsEqualValue"
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
ms.assetid: ba001ada-f091-4072-8699-8882ef730374
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSimpleMapEqualHelperFalse::IsEqualValue
Returns false.  
  
## Syntax  
  
```  
  
      static bool IsEqualValue(  
   const TVal& ,  
   const TVal&   
);  
```  
  
## Return Value  
 Returns false.  
  
## Remarks  
 This method always returns false, and will call `ATLASSERT` with an argument of false if it is ever referenced. The purpose of `CSimpleMapEqualHelperFalse::IsEqualValue` is to force methods using comparisons to fail in a well-defined manner when equality tests have not been adequately defined.  
  
## Requirements  
 **Header:** atlsimpcoll.h  
  
## See Also  
 [CSimpleMapEqualHelperFalse Class](../vs140/CSimpleMapEqualHelperFalse-Class.md)   
 [CSimpleMapEqualHelperFalse::IsEqualKey](../vs140/CSimpleMapEqualHelperFalse--IsEqualKey.md)