---
title: "CComMultiThreadModelNoCS::Increment"
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
ms.assetid: 867d1d49-7668-4081-aba1-67dfa85b0589
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComMultiThreadModelNoCS::Increment
This static function calls the Win32 function [InterlockedIncrement](http://msdn.microsoft.com/library/windows/desktop/ms683614), which increments the value of the variable pointed to by `p`.  
  
## Syntax  
  
```  
  
      static ULONG WINAPI Increment(  
   LPLONG p   
) throw( );  
```  
  
#### Parameters  
 `p`  
 [in] Pointer to the variable to be incremented.  
  
## Return Value  
 If the result of the increment is 0, then **Increment** returns 0. If the result of the increment is nonzero, the return value is also nonzero but may not equal the result of the increment.  
  
## Remarks  
 **InterlockedIncrement** prevents more than one thread from simultaneously using this variable.  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CComMultiThreadModelNoCS Class](../vs140/CComMultiThreadModelNoCS-Class.md)   
 [CComMultiThreadModelNoCS::Decrement](../vs140/CComMultiThreadModelNoCS--Decrement.md)