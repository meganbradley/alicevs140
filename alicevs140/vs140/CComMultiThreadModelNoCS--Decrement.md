---
title: "CComMultiThreadModelNoCS::Decrement"
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
ms.assetid: 3dae705d-42d3-442e-a6f0-dbc90e5fd51c
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComMultiThreadModelNoCS::Decrement
This static function calls the Win32 function [InterlockedDecrement](http://msdn.microsoft.com/library/windows/desktop/ms683580), which decrements the value of the variable pointed to by `p`.  
  
## Syntax  
  
```  
  
      static ULONG WINAPI Decrement(  
   LPLONG p   
) throw( );  
```  
  
#### Parameters  
 `p`  
 [in] Pointer to the variable to be decremented.  
  
## Return Value  
 If the result of the decrement is 0, then `Decrement` returns 0. If the result of the decrement is nonzero, the return value is also nonzero but may not equal the result of the decrement.  
  
## Remarks  
 **InterlockedDecrement** prevents more than one thread from simultaneously using this variable.  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CComMultiThreadModelNoCS Class](../vs140/CComMultiThreadModelNoCS-Class.md)   
 [CComMultiThreadModelNoCS::Increment](../vs140/CComMultiThreadModelNoCS--Increment.md)