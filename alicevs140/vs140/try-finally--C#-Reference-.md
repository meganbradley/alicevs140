---
title: "try-finally (C# Reference)"
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
ms.assetid: c27623fb-7261-4464-862c-7a369d3c8f0a
caps.latest.revision: 27
translation.priority.ht: 
  - de-de
  - ja-jp
---
# try-finally (C# Reference)
By using a `finally` block, you can clean up any resources that are allocated in a [try](../Topic/try-catch%20\(C%23%20Reference\).md) block, and you can run code even if an exception occurs in the `try` block. Typically, the statements of a `finally` block run when control leaves a `try` statement. The transfer of control can occur as a result of normal execution, of execution of a `break`, `continue`, `goto`, or `return` statement, or of propagation of an exception out of the `try` statement.  
  
 Within a handled exception, the associated `finally` block is guaranteed to be run. However, if the exception is unhandled, execution of the `finally` block is dependent on how the exception unwind operation is triggered. That, in turn, is dependent on how your computer is set up. For more information, see [Unhandled Exception Processing in the CLR](http://go.microsoft.com/fwlink/?LinkId=128371).  
  
 Usually, when an unhandled exception ends an application, whether or not the `finally` block is run is not important. However, if you have statements in a `finally` block that must be run even in that situation, one solution is to add a `catch` block to the `try`-`finally` statement. Alternatively, you can catch the exception that might be thrown in the `try` block of a `try`-`finally` statement higher up the call stack. That is, you can catch the exception in the method that calls the method that contains the `try`-`finally` statement, or in the method that calls that method, or in any method in the call stack. If the exception is not caught, execution of the `finally` block depends on whether the operating system chooses to trigger an exception unwind operation.  
  
## Example  
 In the following example, an invalid conversion statement causes a `System.InvalidCastException` exception. The exception is unhandled.  
  
 [!CODE [csrefKeywordsExceptions#4](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsExceptions#4)]  
  
 In the following example, an exception from the `TryCast` method is caught in a method farther up the call stack.  
  
 [!CODE [csrefKeywordsExceptions#6](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsExceptions#6)]  
  
 For more information about `finally`, see [try-catch-finally](../vs140/try-catch-finally--C#-Reference-.md).  
  
 C# also contains the [using statement](../Topic/using%20Statement%20\(C%23%20Reference\).md), which provides similar functionality for <xref:System.IDisposable?qualifyHint=False> objects in a convenient syntax.  
  
## C# Language Specification  
 [!INCLUDE[CSharplangspec](../vs140/includes/Csharplangspec_md.md)]  
  
## See Also  
 [C# Reference](../vs140/C#-Reference.md)   
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [C# Keywords](../Topic/C%23%20Keywords.md)   
 [try, throw, and catch Statements (C++)](../vs140/try--throw--and-catch-Statements--C---.md)   
 [Exception Handling Statements](../vs140/Exception-Handling-Statements--C#-Reference-.md)   
 [throw](../Topic/throw%20\(C%23%20Reference\).md)   
 [try-catch](../Topic/try-catch%20\(C%23%20Reference\).md)   
 [Throwing Exceptions](assetId:///72bdd157-caa9-4478-9ee3-cb4500b84528)