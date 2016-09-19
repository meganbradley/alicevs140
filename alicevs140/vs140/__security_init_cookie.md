---
title: "__security_init_cookie"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
  - C
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
apiname: 
  - __security_init_cookie
apilocation: 
  - msvcr110_clr0400.dll
  - msvcr80.dll
  - msvcr100.dll
  - msvcr90.dll
  - msvcr120.dll
  - msvcr110.dll
  - msvcrt.dll
apitype: DLLExport
ms.assetid: 32119905-0897-4a1c-84ca-bffd16c9b2af
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# __security_init_cookie
Initializes the global security cookie.  
  
## Syntax  
  
```  
void __security_init_cookie(void);  
```  
  
## Remarks  
 The global security cookie is used for buffer overrun protection in code compiled with [/GS (Buffer Security Check)](../Topic/-GS%20\(Buffer%20Security%20Check\).md) and in code that uses exception handling. On entry to an overrun-protected function, the cookie is put on the stack, and on exit, the value on the stack is compared with the global cookie. Any difference between them indicates that a buffer overrun has occurred and causes immediate termination of the program.  
  
 Normally, `__security_init_cookie` is called by the CRT when it is initialized. If you bypass CRT initialization—for example, if you use [/ENTRY](../vs140/-ENTRY--Entry-Point-Symbol-.md) to specify an entry-point—then you must call `__security_init_cookie` yourself. If `__security_init_cookie` is not called, the global security cookie is set to a default value and buffer overrun protection is compromised. Because an attacker can exploit this default cookie value to defeat the buffer overrun checks, we recommend that you always call `__security_init_cookie` when you define your own entry point.  
  
 The call to `__security_init_cookie` must be made before any overrun-protected function is entered; otherwise a spurious buffer overrun will be detected. For more information, see [C Run-Time Error R6035](../vs140/C-Runtime-Error-R6035.md).  
  
## Example  
 See the examples in [C Run-Time Error R6035](../vs140/C-Runtime-Error-R6035.md).  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`__security_init_cookie`|<process.h>|  
  
 `__security_init_cookie` is a Microsoft extension to the standard C Runtime Library. For compatibility information, see [Compatibility](../vs140/Compatibility.md).  
  
## .NET Framework Equivalent  
 Not applicable. This function should only be called from native code, not managed code.  
  
## See Also  
 [Compiler Security Checks In Depth](http://go.microsoft.com/fwlink/?linkid=7260)