---
title: "_CIlog10"
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
  - _CIlog10
apilocation: 
  - msvcr100.dll
  - msvcr120.dll
  - msvcr80.dll
  - msvcr90.dll
  - msvcr110_clr0400.dll
  - msvcrt.dll
  - msvcr110.dll
apitype: DLLExport
ms.assetid: 05d7fcaa-3cff-4cc5-8d44-015e7cacba24
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _CIlog10
Performs a `log10` operation on the top value in the stack.  
  
## Syntax  
  
```  
void __cdecl _CIlog10();  
```  
  
## Remarks  
 This version of the `log10` function has a specialized calling convention that the compiler understands. The function speeds up the execution because it prevents copies from being generated and helps with register allocation.  
  
 The resulting value is pushed onto the top of the stack.  
  
## Requirements  
 **Platform:** x86  
  
## See Also  
 [Alphabetical Function Reference](../vs140/CRT-Alphabetical-Function-Reference.md)   
 [log, logf, log10, log10f](../vs140/log--logf--log10--log10f.md)