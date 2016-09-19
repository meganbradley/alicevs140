---
title: "Exceptions: The try...with Expression (F#)"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - FSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-fsharp
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: 38eeb1f2-3bd7-4b9f-a859-91662181ca41
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Exceptions: The try...with Expression (F#)
This topic describes the `try...with` expression, the expression that is used for exception handling in the F# language.  
  
## Syntax  
  
```  
try  
 expression1  
with  
  | pattern1 -> expression2  
  | pattern2 -> expression3  
  ...  
```  
  
## Remarks  
 The `try...with` expression is used to handle exceptions in F#. It is similar to the `try...catch` statement in C#. In the preceding syntax, the code in `expression1` might generate an exception. The `try...with` expression returns a value. If no exception is thrown, the whole expression returns the value of `expression1`. If an exception is thrown, each `pattern` is compared in turn with the exception, and for the first matching pattern, the corresponding `expression`, known as the *exception handler*, for that branch is executed, and the overall expression returns the value of the expression in that exception handler. If no pattern matches, the exception propagates up the call stack until a matching handler is found. The types of the values returned from each expression in the exception handlers must match the type returned from the expression in the `try` block.  
  
 Frequently, the fact that an error occurred also means that there is no valid value that can be returned from the expressions in each exception handler. A frequent pattern is to have the type of the expression be an option type. The following code example illustrates this pattern.  
  
 [!CODE [FsLangRef2#5601](../CodeSnippet/VS_Snippets_Fsharp/fslangref2#5601)]  
  
 Exceptions can be .NET exceptions, or they can be F# exceptions. You can define F# exceptions by using the `exception` keyword.  
  
 You can use a variety of patterns to filter on the exception type and other conditions; the options are summarized in the following table.  
  
|Pattern|Description|  
|-------------|-----------------|  
|:? `exception-type`|Matches the specified .NET exception type.|  
|:? `exception-type` as `identifier`|Matches the specified .NET exception type, but gives the exception a named value.|  
|`exception-name`(`arguments`)|Matches an F# exception type and binds the arguments.|  
|`identifier`|Matches any exception and binds the name to the exception object. Equivalent to `:? System.Exception as` *identifier*|  
|`identifier` when `condition`|Matches any exception if the condition is true.|  
  
## Examples  
 The following code examples illustrate the use of the various exception handler patterns.  
  
 [!CODE [FsLangRef2#5602](../CodeSnippet/VS_Snippets_Fsharp/fslangref2#5602)]  
  
> [!NOTE]
>  The `try...with` construct is a separate expression from the `try...finally` expression. Therefore, if your code requires both a `with` block and a `finally` block, you will have to nest the two expressions.  
  
> [!NOTE]
>  You can use `try...with` in asynchronous workflows and other computation expressions, in which case a customized version of the `try...with` expression is used. For more information, see [Asynchronous Workflows (F#)](../Topic/Asynchronous%20Workflows%20\(F%23\).md), and [Computation Expressions (F#)](../Topic/Computation%20Expressions%20\(F%23\).md).  
  
## See Also  
 [Exception Handling (F#)](../vs140/Exception-Handling--F#-.md)   
 [Exception Types](../Topic/Exception%20Types%20\(F%23\).md)   
 [Exceptions: The try .. finally Expression](../vs140/Exceptions--The-try...finally-Expression--F#-.md)