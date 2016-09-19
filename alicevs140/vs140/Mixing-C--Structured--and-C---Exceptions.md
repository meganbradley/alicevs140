---
title: "Mixing C (Structured) and C++ Exceptions"
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
ms.topic: language-reference
ms.assetid: a149154e-36dd-4d1a-980b-efde2a563a56
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Mixing C (Structured) and C++ Exceptions
If you want to write more portable code, using structured exception handling in a C++ program is not recommended. However, you may sometimes want to compile with **/EHa** and mix structured exceptions and C++ source code, and need some facility for handling both kinds of exceptions. Because a structured exception handler has no concept of objects or typed exceptions, it cannot handle exceptions thrown by C++ code; however, C++ **catch** handlers can handle structured exceptions. As such, C++ exception handling syntax (**try**, `throw`, **catch**) is not accepted by the C compiler, but structured exception handling syntax (`__try`, `__except`, `__finally`) is supported by the C++ compiler.  
  
 See [_set_se_translator](../vs140/_set_se_translator.md) for information on handling structured exceptions as C++ exceptions.  
  
 If you mix structured and C++ exceptions, note the following:  
  
1.  C++ exceptions and structured exceptions cannot be mixed within the same function.  
  
2.  Termination handlers (`__finally` blocks) are always executed, even during unwinding after an exception is thrown.  
  
3.  C++ exception handling can catch and preserve unwind semantics in all modules compiled with the [/EH](../vs140/-EH--Exception-Handling-Model-.md) compiler option (this option enables unwind semantics).  
  
4.  There may be some situations in which destructor functions are not called for all objects. For example, if a structured exception occurs while attempting to make a function call through an uninitialized function pointer, and that function takes as parameters objects that were constructed before the call, those objects will not have their destructors called during stack unwind.  
  
## What do you want to know more about?  
  
-   [Using setjmp or longjmp in C++ programs](../vs140/Using-setjmp-longjmp.md)  
  
-   [Differences between SEH and C++ EH](../vs140/Exception-Handling-Differences.md)  
  
## See Also  
 [C++ Exception Handling](../vs140/C---Exception-Handling.md)