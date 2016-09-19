---
title: "_ATL_MIXED"
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
ms.assetid: 11b59a83-7098-43e2-9f7b-408299930966
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _ATL_MIXED
_ATL_MIXED specifies that your ATL application is comprised of native and **/clr** compilands.  
  
## Syntax  
  
```  
_ATL_MIXED  
```  
  
## Remarks  
 When building an application that uses ATL, and where the compilands are not all native or all **/clr**, then you must add this macro to each compiland.  
  
 `#define _ATL_MIXED`  
  
 This will cause all startup code to run as native. You may need to ensure that all startup code is native. See [Initialization of Mixed Assemblies](../vs140/Initialization-of-Mixed-Assemblies.md) for more information.  
  
## See Also  
 [Compiler Options Macros](../vs140/Compiler-Options-Macros.md)   
 [Macros](../vs140/ATL-Macros.md)