---
title: "Using setjmp-longjmp"
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
H1: Using setjmp/longjmp
ms.assetid: 96be8816-f6f4-4567-9a9c-0c3c720e37c5
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Using setjmp-longjmp
When [setjmp](../vs140/setjmp.md) and [longjmp](../vs140/longjmp.md) are used together, they provide a way to execute a non-local `goto`. They are typically used to pass execution control to error-handling or recovery code in a previously called routine without using the standard calling or return conventions.  
  
> [!CAUTION]
>  However, because `setjmp` and `longjmp` do not support C++ object semantics, and because they might degrade performance by preventing optimization on local variables, we recommend that you do not use them in C++ programs. We recommend that you use `try`/`catch` constructs instead.  
  
 If you decide to use `setjmp`/`longjmp` in a C++ program, also include SETJMP.H or SETJMPEX.H to assure correct interaction between the functions and C++ exception handling. If you use [/EH](../vs140/-EH--Exception-Handling-Model-.md) to compile, destructors for local objects are called during the stack unwind. If you use **/EHs** to compile, and one of your functions calls a function that uses [nothrow](../vs140/nothrow--C---.md) and the function that uses `nothrow` calls `longjmp`, then the destructor unwind might not occur, depending on the optimizer.  
  
 In portable code, when a non-local `goto` that calls `longjmp` is executed, correct destruction of frame-based objects might be unreliable.  
  
## See Also  
 [Mixing C (Structured) and C++ Exceptions](../vs140/Mixing-C--Structured--and-C---Exceptions.md)