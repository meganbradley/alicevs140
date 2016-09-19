---
title: "Loops: while...do Expression (F#)"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - FSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-fsharp
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: 69b80e73-83e2-4939-aa56-47e8d122f508
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Loops: while...do Expression (F#)
The `while...do` expression is used to perform iterative execution (looping) while a specified test condition is true.  
  
## Syntax  
  
```  
while test-expression do  
   body-expression  
```  
  
## Remarks  
 The `test-expression` is evaluated; if it is `true`, the `body-expression` is executed and the test expression is evaluated again. The `body-expression` must have type `unit`. If the test expression is `false`, the iteration ends.  
  
 The following example illustrates the use of the `while...do` expression.  
  
 [!CODE [FsLangRef2#5301](../CodeSnippet/VS_Snippets_Fsharp/fslangref2#5301)]  
  
 The output of the previous code is a stream of random numbers between 1 and 20, the last of which is 10.  
  
```  
13 19 8 18 16 2 10  
Found a 10!  
```  
  
> [!NOTE]
>  You can use `while...do` in sequence expressions and other computation expressions, in which case a customized version of the `while...do` expression is used. For more information, see [Sequences (F#)](../Topic/Sequences%20\(F%23\).md), [Asynchronous Workflows (F#)](../Topic/Asynchronous%20Workflows%20\(F%23\).md), and [Computation Expressions (F#)](../Topic/Computation%20Expressions%20\(F%23\).md).  
  
## See Also  
 [F# Language Reference](../Topic/F%23%20Language%20Reference.md)   
 [Loops: for...in Expression](../vs140/Loops--for...in-Expression--F#-.md)   
 [Loops: for...to Expression](../vs140/Loops--for...to-Expression--F#-.md)