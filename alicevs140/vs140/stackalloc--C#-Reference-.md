---
title: "stackalloc (C# Reference)"
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
ms.assetid: adc04c28-3ed2-4326-807a-7545df92b852
caps.latest.revision: 29
translation.priority.ht: 
  - de-de
  - ja-jp
---
# stackalloc (C# Reference)
The `stackalloc` keyword is used in an unsafe code context to allocate a block of memory on the stack.  
  
```  
int* block = stackalloc int[100];  
```  
  
## Remarks  
 The keyword is valid only in local variable initializers. The following code causes compiler errors.  
  
```  
int* block;  
// The following assignment statement causes compiler errors. You  
// can use stackalloc only when declaring and initializing a local   
// variable.  
block = stackalloc int[100];  
```  
  
 Because pointer types are involved, `stackalloc` requires [unsafe](../vs140/unsafe--C#-Reference-.md) context. For more information, see [Unsafe Code and Pointers](../vs140/Unsafe-Code-and-Pointers--C#-Programming-Guide-.md).  
  
 `stackalloc` is like [_alloca](../vs140/_alloca.md) in the C run-time library.  
  
 The following example calculates and displays the first 20 numbers in the Fibonacci sequence. Each number is the sum of the previous two numbers. In the code, a block of memory of sufficient size to contain 20 elements of type `int` is allocated on the stack, not the heap. The address of the block is stored in the pointer `fib`. This memory is not subject to garbage collection and therefore does not have to be pinned (by using [fixed](../vs140/fixed-Statement--C#-Reference-.md)). The lifetime of the memory block is limited to the lifetime of the method that defines it. You cannot free the memory before the method returns.  
  
## Example  
 [!CODE [csrefKeywordsOperator#15](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsOperator#15)]  
  
## Security  
 Unsafe code is less secure than safe alternatives. However, the use of `stackalloc` automatically enables buffer overrun detection features in the common language runtime (CLR). If a buffer overrun is detected, the process is terminated as quickly as possible to minimize the chance that malicious code is executed.  
  
## C# Language Specification  
 [!INCLUDE[CSharplangspec](../vs140/includes/Csharplangspec_md.md)]  
  
## See Also  
 [C# Reference](../vs140/C#-Reference.md)   
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [C# Keywords](../Topic/C%23%20Keywords.md)   
 [Operator Keywords](../vs140/Operator-Keywords--C#-Reference-.md)   
 [Unsafe Code and Pointers (C#)](../vs140/Unsafe-Code-and-Pointers--C#-Programming-Guide-.md)