---
title: "_CIsqrt"
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
ms.topic: article
apiname: 
  - _CIsqrt
apilocation: 
  - msvcr90.dll
  - msvcr80.dll
  - msvcr110_clr0400.dll
  - msvcr120.dll
  - msvcrt.dll
  - msvcr110.dll
  - msvcr100.dll
apitype: DLLExport
ms.assetid: 663548ea-398c-48ee-8397-a787c6ebb937
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _CIsqrt
Calculates the square root of the top value in the stack.  
  
## Syntax  
  
```  
void __cdecl _CIsqrt();  
```  
  
## Remarks  
 This version of the `sqrt` function has a specialized calling convention that the compiler understands. It speeds up the execution because it prevents copies from being generated and helps with register allocation.  
  
 The resulting value is pushed onto the top of the stack.  
  
## Requirements  
 **Platform:** x86  
  
## See Also  
 [Alphabetical Function Reference](../vs140/CRT-Alphabetical-Function-Reference.md)   
 [sqrt, sqrtf](../vs140/sqrt--sqrtf--sqrtl.md)