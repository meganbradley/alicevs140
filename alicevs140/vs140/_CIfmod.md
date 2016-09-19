---
title: "_CIfmod"
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
  - _CIfmod
apilocation: 
  - msvcrt.dll
  - msvcr110_clr0400.dll
  - msvcr100.dll
  - msvcr80.dll
  - msvcr90.dll
  - msvcr120.dll
  - msvcr110.dll
apitype: DLLExport
ms.assetid: 7c050653-7ec6-4810-b3a7-7a0057ea65ed
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _CIfmod
Calculates the floating-point remainder of the top two values on the stack.  
  
## Syntax  
  
```  
void __cdecl _CIfmod();  
```  
  
## Remarks  
 This version of the `fmod` function has a specialized calling convention that the compiler understands. It speeds up the execution because it prevents copies from being generated and helps with register allocation.  
  
 The resulting value is pushed onto the top of the stack.  
  
## Requirements  
 **Platform:** x86  
  
## See Also  
 [Alphabetical Function Reference](../vs140/CRT-Alphabetical-Function-Reference.md)   
 [fmod, fmodf](../vs140/fmod--fmodf.md)