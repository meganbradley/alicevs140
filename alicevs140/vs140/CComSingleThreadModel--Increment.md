---
title: "CComSingleThreadModel::Increment"
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
ms.assetid: 537e123d-26fd-4895-9c77-ce2d7abadaa2
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComSingleThreadModel::Increment
This static function decrements the value of the variable pointed to by `p`.  
  
## Syntax  
  
```  
  
      static ULONG WINAPI Increment(  
   LPLONG p   
) throw();  
```  
  
#### Parameters  
 `p`  
 [in] Pointer to the variable to be incremented.  
  
## Return Value  
 The result of the increment.  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CComSingleThreadModel Class](../vs140/CComSingleThreadModel-Class.md)   
 [CComSingleThreadModel::Decrement](../vs140/CComSingleThreadModel--Decrement.md)