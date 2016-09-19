---
title: "Using Exceptions (C# Programming Guide)"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - CSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 71472c62-320a-470a-97d2-67995180389d
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Using Exceptions (C# Programming Guide)
In C#, errors in the program at run time are propagated through the program by using a mechanism called exceptions. Exceptions are thrown by code that encounters an error and caught by code that can correct the error. Exceptions can be thrown by the .NET Framework common language runtime (CLR) or by code in a program. Once an exception is thrown, it propagates up the call stack until a `catch` statement for the exception is found. Uncaught exceptions are handled by a generic exception handler provided by the system that displays a dialog box.  
  
 Exceptions are represented by classes derived from <xref:System.Exception?qualifyHint=False>. This class identifies the type of exception and contains properties that have details about the exception. Throwing an exception involves creating an instance of an exception-derived class, optionally configuring properties of the exception, and then throwing the object by using the `throw` keyword. For example:  
  
 [!CODE [csProgGuideExceptions#1](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideExceptions#1)]  
  
 After an exception is thrown, the runtime checks the current statement to see whether it is within a `try` block. If it is, any `catch` blocks associated with the `try` block are checked to see whether they can catch the exception. `Catch` blocks typically specify exception types; if the type of the `catch` block is the same type as the exception, or a base class of the exception, the `catch` block can handle the method. For example:  
  
 [!CODE [csProgGuideExceptions#2](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideExceptions#2)]  
  
 If the statement that throws an exception is not within a `try` block or if the `try` block that encloses it has no matching `catch` block, the runtime checks the calling method for a `try` statement and `catch` blocks. The runtime continues up the calling stack, searching for a compatible `catch` block. After the `catch` block is found and executed, control is passed to the next statement after that `catch` block.  
  
 A `try` statement can contain more than one `catch` block. The first `catch` statement that can handle the exception is executed; any following `catch` statements, even if they are compatible, are ignored. Therefore, catch blocks should always be ordered from most specific (or most-derived) to least specific. For example:  
  
 [!CODE [csProgGuideExceptions#3](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideExceptions#3)]  
  
 Before the `catch` block is executed, the runtime checks for `finally` blocks. `Finally` blocks enable the programmer to clean up any ambiguous state that could be left over from an aborted `try` block, or to release any external resources (such as graphics handles, database connections or file streams) without waiting for the garbage collector in the runtime to finalize the objects. For example:  
  
 [!CODE [csProgGuideExceptions#4](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideExceptions#4)]  
  
 If `WriteByte()` threw an exception, the code in the second `try` block that tries to reopen the file would fail if `file.Close()` is not called, and the file would remain locked. Because `finally` blocks are executed even if an exception is thrown, the `finally` block in the previous example allows for the file to be closed correctly and helps avoid an error.  
  
 If no compatible `catch` block is found on the call stack after an exception is thrown, one of three things occurs:  
  
-   If the exception is within a destructor, the destructor is aborted and the base destructor, if any, is called.  
  
-   If the call stack contains a static constructor, or a static field initializer, a <xref:System.TypeInitializationException?qualifyHint=False> is thrown, with the original exception assigned to the <xref:System.Exception.InnerException?qualifyHint=False> property of the new exception.  
  
-   If the start of the thread is reached, the thread is terminated.  
  
## See Also  
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [Exceptions and Exception Handling (Visual C#)](../Topic/Exceptions%20and%20Exception%20Handling%20\(C%23%20Programming%20Guide\).md)