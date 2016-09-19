---
title: "_ATLCATCH"
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
ms.assetid: f23a9048-4025-43f4-a245-e97b3562b267
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _ATLCATCH
Statement(s) to handle errors occurring in the associated `_ATLTRY`.  
  
## Syntax  
  
```  
  
_ATLCATCH(   
e  
 )  
  
```  
  
#### Parameters  
 *e*  
 The exception to catch.  
  
## Remarks  
 Used in conjunction with `_ATLTRY`. Resolves to C++ [catch(CAtlException e)](../vs140/try--throw--and-catch-Statements--C---.md) for handling a given type of C++ exceptions.  
  
## Requirements  
 **Header:** atldef.h  
  
## See Also  
 [Exception Handling Macros](../vs140/Exception-Handling-Macros.md)   
 [_ATLTRY](../vs140/_ATLTRY.md)   
 [_ATLCATCHALL](../vs140/_ATLCATCHALL.md)