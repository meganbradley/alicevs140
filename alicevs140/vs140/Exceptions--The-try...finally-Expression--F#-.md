---
title: "Exceptions: The try...finally Expression (F#)"
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
ms.assetid: 767c7719-fdae-450a-897c-babc928eaae9
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Exceptions: The try...finally Expression (F#)
The `try...finally` expression enables you to execute clean-up code even if a block of code throws an exception.  
  
## Syntax  
  
```  
try  
   expression1  
finally  
   expression2  
```  
  
## Remarks  
 The `try...finally` expression can be used to execute the code in `expression2` in the preceding syntax regardless of whether an exception is generated during the execution of `expression1`.  
  
 The type of `expression2` does not contribute to the value of the whole expression; the type returned when an exception does not occur is the last value in `expression1`. When an exception does occur, no value is returned and the flow of control transfers to the next matching exception handler up the call stack. If no exception handler is found, the program terminates. Before the code in a matching handler is executed or the program terminates, the code in the `finally` branch is executed.  
  
 The following code demonstrates the use of the `try...finally` expression.  
  
 [!CODE [FsLangRef2#5701](../CodeSnippet/VS_Snippets_Fsharp/fslangref2#5701)]  
  
 The output to the console is as follows.  
  
```  
Closing stream  
Exception handled.  
```  
  
 As you can see from the output, the stream was closed before the outer exception was handled, and the file `test.txt` contains the text `test1`, which indicates that the buffers were flushed and written to disk even though the exception transferred control to the outer exception handler.  
  
 Note that the `try...with` construct is a separate construct from the `try...finally` construct. Therefore, if your code requires both a `with` block and a `finally` block, you have to nest the two constructs, as in the following code example.  
  
 [!CODE [FsLangRef2#5702](../CodeSnippet/VS_Snippets_Fsharp/fslangref2#5702)]  
  
 In the context of computation expressions, including sequence expressions and asynchronous workflows, `try...finally` expressions can have a custom implementation. For more information, see [Computation Expressions (F#)](../Topic/Computation%20Expressions%20\(F%23\).md).  
  
## See Also  
 [Exception Handling](../vs140/Exception-Handling--F#-.md)   
 [Exceptions: the try .. with Expression](../vs140/Exceptions--The-try...with-Expression--F#-.md)