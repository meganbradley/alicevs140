---
title: "CComAutoThreadModule::Lock"
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
ms.assetid: 7dd467c6-314f-43de-95f4-f2f99aeea4bf
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComAutoThreadModule::Lock
As of ATL 7.0, `CComAutoThreadModule` is obsolete: see [ATL Module Classes](../vs140/ATL-Module-Classes.md) for more details.  
  
## Syntax  
  
```  
  
LONG Lock( );  
  
```  
  
## Return Value  
 A value that may be useful for diagnostics or testing.  
  
## Remarks  
 Performs an atomic increment on the lock count for the module and for the current thread. `CComAutoThreadModule` uses the module lock count to determine whether any clients are accessing the module. The lock count on the current thread is used for statistical purposes.  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CComAutoThreadModule Class](../vs140/CComAutoThreadModule-Class.md)   
 [CComAutoThreadModule::Unlock](../vs140/CComAutoThreadModule--Unlock.md)