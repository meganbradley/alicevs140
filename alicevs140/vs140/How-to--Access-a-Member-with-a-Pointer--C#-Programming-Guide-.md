---
title: "How to: Access a Member with a Pointer (C# Programming Guide)"
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
ms.assetid: 1e998498-8c85-4a78-8ce2-4d8c20f08342
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Access a Member with a Pointer (C# Programming Guide)
To access a member of a struct that is declared in an unsafe context, you can use the member access operator as shown in the following example in which `p` is a pointer to a [struct](../vs140/struct--C#-Reference-.md) that contains a member `x`.  
  
```  
CoOrds* p = &home;  
p -> x = 25; //member access operator ->  
```  
  
## Example  
 In this example, a [struct](../vs140/struct--C#-Reference-.md), `CoOrds`, that contains the two coordinates `x` and `y` is declared and instantiated. By using the member access operator `->` and a pointer to the instance `home`, `x` and `y` are assigned values.  
  
> [!NOTE]
>  Notice that the expression `p->x` is equivalent to the expression `(*p).x`, and you can obtain the same result by using either of the two expressions.  
  
 [!CODE [csProgGuidePointers#9](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuidePointers#9)]  
  
 [!CODE [csProgGuidePointers#10](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuidePointers#10)]  
  
## See Also  
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [Pointer Expressions](../vs140/Pointer-Expressions--C#-Programming-Guide-.md)   
 [Pointer types](../vs140/Pointer-types--C#-Programming-Guide-.md)   
 [Types](../vs140/Types--C#-Reference-.md)   
 [unsafe](../vs140/unsafe--C#-Reference-.md)   
 [fixed Statement](../vs140/fixed-Statement--C#-Reference-.md)   
 [stackalloc](../vs140/stackalloc--C#-Reference-.md)