---
title: "return (C# Reference)"
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
ms.assetid: 6da6e152-5b58-4448-8f3f-470dd0617ecd
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# return (C# Reference)
The `return` statement terminates execution of the method in which it appears and returns control to the calling method. It can also return an optional value. If the method is a `void` type, the `return` statement can be omitted.  
  
 If the return statement is inside a `try` block, the `finally` block, if one exists, will be executed before control returns to the calling method.  
  
## Example  
 In the following example, the method `A()` returns the variable `Area` as a [double](../vs140/double--C#-Reference-.md) value.  
  
 [!CODE [csrefKeywordsJump#6](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsJump#6)]  
  
## C# Language Specification  
 [!INCLUDE[CSharplangspec](../vs140/includes/Csharplangspec_md.md)]  
  
## See Also  
 [C# Reference](../vs140/C#-Reference.md)   
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [C# Keywords](../Topic/C%23%20Keywords.md)   
 [return Statement](../vs140/return-Statement--C---.md)   
 [Jump Statements](../vs140/Jump-Statements--C#-Reference-.md)