---
title: "_CIlog"
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
  - _CIlog
apilocation: 
  - msvcr90.dll
  - msvcr120.dll
  - msvcr80.dll
  - msvcr110.dll
  - msvcr110_clr0400.dll
  - msvcr100.dll
  - msvcrt.dll
apitype: DLLExport
ms.assetid: 23503854-ddaa-4fe0-a4a3-7fbb3a43bdec
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _CIlog
Calculates the natural logarithm of the top value in the stack.  
  
## Syntax  
  
```  
void __cdecl _CIlog();  
```  
  
## Remarks  
 This version of the `log` function has a specialized calling convention that the compiler understands. It speeds up the execution because it prevents copies from being generated and helps with register allocation.  
  
 The resulting value is pushed onto the top of the stack.  
  
## Requirements  
 **Platform:** x86  
  
## See Also  
 [Alphabetical Function Reference](../vs140/CRT-Alphabetical-Function-Reference.md)   
 [log, logf, log10, log10f](../vs140/log--logf--log10--log10f.md)