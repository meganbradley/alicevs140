---
title: "_ATLCATCHALL"
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
ms.assetid: 4d739656-a00c-46b8-be0c-b56545a09335
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _ATLCATCHALL
Statement(s) to handle errors occurring in the associated `_ATLTRY`.  
  
## Syntax  
  
```  
  
_ATLCATCHALL  
  
```  
  
## Remarks  
 Used in conjunction with `_ATLTRY`. Resolves to C++ [catch(...)](../vs140/try--throw--and-catch-Statements--C---.md) for handling all types of C++ exceptions.  
  
## Requirements  
 **Header:** atldef.h  
  
## See Also  
 [Exception Handling Macros](../vs140/Exception-Handling-Macros.md)   
 [_ATLTRY](../vs140/_ATLTRY.md)   
 [_ATLCATCH](../vs140/_ATLCATCH.md)