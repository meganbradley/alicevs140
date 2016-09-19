---
title: "_CIcos"
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
  - _CIcos
apilocation: 
  - msvcr90.dll
  - msvcrt.dll
  - msvcr120.dll
  - msvcr100.dll
  - msvcr80.dll
  - msvcr110_clr0400.dll
  - msvcr110.dll
apitype: DLLExport
ms.assetid: 6fc203fb-66f3-4ead-9784-f85833c26f1b
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _CIcos
Calculates the cosine of the top value in the stack.  
  
## Syntax  
  
```  
void __cdecl _CIcos();  
```  
  
## Remarks  
 This version of the `cos` function has a specialized calling convention that the compiler understands. It speeds up the execution because it prevents copies from being generated and helps with register allocation.  
  
 The resulting value is pushed onto the top of the stack.  
  
## Requirements  
 **Platform:** x86  
  
## See Also  
 [Alphabetical Function Reference](../vs140/CRT-Alphabetical-Function-Reference.md)   
 [cos, cosf, cosh, coshf](../vs140/cos--cosf--cosl--cosh--coshf--coshl.md)