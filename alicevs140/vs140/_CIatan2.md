---
title: "_CIatan2"
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
  - _CIatan2
apilocation: 
  - msvcr80.dll
  - msvcrt.dll
  - msvcr120.dll
  - msvcr110_clr0400.dll
  - msvcr110.dll
  - msvcr100.dll
  - msvcr90.dll
apitype: DLLExport
ms.assetid: 31f8cc78-b79f-4576-b73b-8add18e08680
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _CIatan2
Calculates the arctangent of *x* / *y* where *x* and *y* are values on the top of the stack.  
  
## Syntax  
  
```  
void __cdecl _CIatan2();  
```  
  
## Remarks  
 This version of the `atan2` function has a specialized calling convention that the compiler understands. It speeds up the execution because it prevents copies from being generated and helps with register allocation.  
  
 The resulting value is pushed onto the top of the stack.  
  
## Requirements  
 **Platform:** x86  
  
## See Also  
 [Alphabetical Function Reference](../vs140/CRT-Alphabetical-Function-Reference.md)   
 [atan, atanf, atan2, atan2f](../vs140/atan--atanf--atanl--atan2--atan2f--atan2l.md)