---
title: "CComObjectRootEx::OuterRelease"
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
ms.assetid: 8d441b85-2ec1-4734-aa30-638eca6751a4
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComObjectRootEx::OuterRelease
Decrements the reference count of the outer unknown of an aggregation.  
  
## Syntax  
  
```  
  
ULONG OuterRelease( );  
```  
  
## Return Value  
 In non-debug builds, always returns 0. In debug builds, returns a value that may be useful for diagnostics or testing.  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [CComObjectRootEx Class](../vs140/CComObjectRootEx-Class.md)   
 [CComObjectRootEx::OuterAddRef](../vs140/CComObjectRootEx--OuterAddRef.md)   
 [CComObjectRootEx::OuterQueryInterface](../vs140/CComObjectRootEx--OuterQueryInterface.md)