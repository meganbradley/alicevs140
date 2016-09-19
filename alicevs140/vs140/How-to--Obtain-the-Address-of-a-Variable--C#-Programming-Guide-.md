---
title: "How to: Obtain the Address of a Variable (C# Programming Guide)"
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
ms.assetid: 44fe2cd9-a64f-4ef5-be2a-09ce807c0182
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Obtain the Address of a Variable (C# Programming Guide)
To obtain the address of a unary expression, which evaluates to a fixed variable, use the address-of operator:  
  
```  
int number;  
int* p = &number; //address-of operator &  
```  
  
 The address-of operator can only be applied to a variable. If the variable is a moveable variable, you can use the [fixed statement](../vs140/fixed-Statement--C#-Reference-.md) to temporarily fix the variable before obtaining its address.  
  
 It is your responsibility to ensure that the variable is initialized. The compiler will not issue an error message if the variable is not initialized.  
  
 You cannot get the address of a constant or a value.  
  
## Example  
 In this example, a pointer to `int`, `p`, is declared and assigned the address of an integer variable, `number`. The variable `number` is initialized as a result of the assignment to *p. If you make this assignment statement a comment, the initialization of the variable `number` will be removed, but no compile-time error is issued. Notice the use of the [Member Access](../vs140/How-to--Access-a-Member-with-a-Pointer--C#-Programming-Guide-.md) operator `->` to obtain and display the address stored in the pointer.  
  
 [!CODE [csProgGuidePointers#7](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuidePointers#7)]  
  
 [!CODE [csProgGuidePointers#8](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuidePointers#8)]  
  
## See Also  
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [Pointer Expressions](../vs140/Pointer-Expressions--C#-Programming-Guide-.md)   
 [Pointer types](../vs140/Pointer-types--C#-Programming-Guide-.md)   
 [Types](../vs140/Types--C#-Reference-.md)   
 [unsafe](../vs140/unsafe--C#-Reference-.md)   
 [fixed Statement](../vs140/fixed-Statement--C#-Reference-.md)   
 [stackalloc](../vs140/stackalloc--C#-Reference-.md)