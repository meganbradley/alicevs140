---
title: "Arithmetic Operations on Pointers (C# Programming Guide)"
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
ms.assetid: d4f0b623-827e-45ce-8649-cfcebc8692aa
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Arithmetic Operations on Pointers (C# Programming Guide)
This topic discusses using the arithmetic operators `+` and **-** to manipulate pointers.  
  
> [!NOTE]
>  You cannot perform any arithmetic operations on void pointers.  
  
## Adding and Subtracting Numeric Values to or From Pointers  
 You can add a value `n` of type [int](../Topic/int%20\(C%23%20Reference\).md), [uint](../Topic/uint%20\(C%23%20Reference\).md), [long](../vs140/long--C#-Reference-.md), or [ulong](../Topic/ulong%20\(C%23%20Reference\).md) to a pointer, `p`,of any type except `void*`. The result `p+n` is the pointer resulting from adding `n * sizeof(p) to the address of p`. Similarly, `p-n` is the pointer resulting from subtracting `n * sizeof(p)` from the address of `p`.  
  
## Subtracting Pointers  
 You can also subtract pointers of the same type. The result is always of the type `long`. For example, if `p1` and `p2` are pointers of the type `pointer-type*`, then the expression `p1-p2` results in:  
  
 `((long)p1 - (long)p2)/sizeof(pointer_type)`  
  
 No exceptions are generated when the arithmetic operation overflows the domain of the pointer, and the result depends on the implementation.  
  
## Example  
 [!CODE [csProgGuidePointers#14](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuidePointers#14)]  
  
 [!CODE [csProgGuidePointers#15](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuidePointers#15)]  
  
## C# Language Specification  
 [!INCLUDE[CSharplangspec](../vs140/includes/Csharplangspec_md.md)]  
  
## See Also  
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [Unsafe Code and Pointers (C# Programming Guide)](../vs140/Unsafe-Code-and-Pointers--C#-Programming-Guide-.md)   
 [Pointer Expressions](../vs140/Pointer-Expressions--C#-Programming-Guide-.md)   
 [C# Operators](../Topic/C%23%20Operators.md)   
 [Manipulating Pointers](../vs140/Manipulating-Pointers--C#-Programming-Guide-.md)   
 [Pointer types](../vs140/Pointer-types--C#-Programming-Guide-.md)   
 [Types](../vs140/Types--C#-Reference-.md)   
 [unsafe](../vs140/unsafe--C#-Reference-.md)   
 [fixed Statement](../vs140/fixed-Statement--C#-Reference-.md)   
 [stackalloc](../vs140/stackalloc--C#-Reference-.md)