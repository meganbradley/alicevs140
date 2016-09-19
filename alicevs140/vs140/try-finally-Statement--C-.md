---
title: "try-finally Statement (C)"
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
ms.assetid: 514400c1-c322-4bf3-9e48-3047240b8a82
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# try-finally Statement (C)
**Microsoft Specific**  
  
 The `try-finally` statement is a Microsoft extension to the C language that enables applications to guarantee execution of cleanup code when execution of a block of code is interrupted. Cleanup consists of such tasks as deallocating memory, closing files, and releasing file handles. The `try-finally` statement is especially useful for routines that have several places where a check is made for an error that could cause premature return from the routine.  
  
 *try-finally-statement*:  
 **__try**  *compound-statement*  
  
 **__finally**  *compound-statement*  
  
 The compound statement after the `__try` clause is the guarded section. The compound statement after the `__finally` clause is the termination handler. The handler specifies a set of actions that execute when the guarded section is exited, whether the guarded section is exited by an exception (abnormal termination) or by standard fall through (normal termination).  
  
 Control reaches a `__try` statement by simple sequential execution (fall through). When control enters the `__try` statement, its associated handler becomes active. Execution proceeds as follows:  
  
1.  The guarded section is executed.  
  
2.  The termination handler is invoked.  
  
3.  When the termination handler completes, execution continues after the `__finally` statement. Regardless of how the guarded section ends (for example, via a `goto` statement out of the guarded body or via a `return` statement), the termination handler is executed before the flow of control moves out of the guarded section.  
  
 The `__leave` keyword is valid within a `try-finally` statement block. The effect of `__leave` is to jump to the end of the `try-finally` block. The termination handler is immediately executed. Although a `goto` statement can be used to accomplish the same result, a `goto` statement causes stack unwinding. The `__leave` statement is more efficient because it does not involve stack unwinding.  
  
 Exiting a `try-finally` statement using a `return` statement or the `longjmp` run-time function is considered abnormal termination. It is illegal to jump into a `__try` statement, but legal to jump out of one. All `__finally` statements that are active between the point of departure and the destination must be run. This is called a "local unwind."  
  
 The termination handler is not called if a process is killed while executing a `try-finally` statement.  
  
> [!NOTE]
>  Structured exception handling works with C and C++ source files. However, it is not specifically designed for C++. You can ensure that your code is more portable by using C++ exception handling. Also, the C++ exception handling mechanism is much more flexible, in that it can handle exceptions of any type.  
  
> [!NOTE]
>  For C++ programs, C++ exception handling should be used instead of structured exception handling. For more information, see [Exception Handling](../vs140/Exception-Handling-in-Visual-C--.md) in the *C++ Language Reference*.  
  
 See the example for the [try-except statement](../vs140/try-except-Statement--C-.md) to see how the `try-finally` statement works.  
  
 **END Microsoft Specific**  
  
## See Also  
 [try-finally Statement](../vs140/try-finally-Statement.md)