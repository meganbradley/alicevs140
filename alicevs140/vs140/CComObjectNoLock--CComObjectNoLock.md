---
title: "CComObjectNoLock::CComObjectNoLock"
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
ms.assetid: 94f3a4df-35f4-4bc0-bff3-350ddd76677b
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComObjectNoLock::CComObjectNoLock
The constructor. Unlike [CComObject](../vs140/CComObject-Class.md), does not increment the module lock count.  
  
## Syntax  
  
```  
  
      CComObjectNoLock(  
   void* = NULL   
);  
```  
  
#### Parameters  
 **void\***  
 [in] This unnamed parameter is not used. It exists for symmetry with other **CCom***XXX*`Object`*XXX* constructors.  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [CComObjectNoLock Class](../vs140/CComObjectNoLock-Class.md)