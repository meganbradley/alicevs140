---
title: "_CItan"
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
  - _CItan
apilocation: 
  - msvcr100.dll
  - msvcr110_clr0400.dll
  - msvcr80.dll
  - msvcrt.dll
  - msvcr110.dll
  - msvcr90.dll
  - msvcr120.dll
apitype: DLLExport
ms.assetid: d1ea3113-50a2-45a6-b6bc-680fcdcc0928
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _CItan
Calculates the tangent of the top value on the stack.  
  
## Syntax  
  
```  
void __cdecl _CItan();  
```  
  
## Remarks  
 This version of the `tan` function has a specialized calling convention that the compiler understands. The function speeds up the execution because it prevents copies from being generated and helps with register allocation.  
  
 The resulting value is pushed onto the top of the stack.  
  
## Requirements  
 **Platform:** x86  
  
## See Also  
 [Alphabetical Function Reference](../vs140/CRT-Alphabetical-Function-Reference.md)   
 [tan, tanf, tanh, tanhf](../vs140/tan--tanf--tanl--tanh--tanhf--tanhl.md)