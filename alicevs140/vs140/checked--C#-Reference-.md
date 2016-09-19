---
title: "checked (C# Reference)"
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
ms.assetid: 718a1194-988d-48a3-b089-d6ee8bd1608d
caps.latest.revision: 26
translation.priority.ht: 
  - de-de
  - ja-jp
---
# checked (C# Reference)
The `checked` keyword is used to explicitly enable overflow checking for integral-type arithmetic operations and conversions.  
  
 By default, an expression that contains only constant values causes a compiler error if the expression produces a value that is outside the range of the destination type. If the expression contains one or more non-constant values, the compiler does not detect the overflow. Evaluating the expression assigned to `i2` in the following example does not cause a compiler error.  
  
 [!CODE [csrefKeywordsChecked#3](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsChecked#3)]  
  
 By default, these non-constant expressions are not checked for overflow at run time either, and they do not raise overflow exceptions. The previous example displays -2,147,483,639 as the sum of two positive integers.  
  
 Overflow checking can be enabled by compiler options, environment configuration, or use of the `checked` keyword. The following examples demonstrate how to use a `checked` expression or a `checked` block to detect the overflow that is produced by the previous sum at run time. Both examples raise an overflow exception.  
  
 [!CODE [csrefKeywordsChecked#4](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsChecked#4)]  
  
 The [unchecked](../vs140/unchecked--C#-Reference-.md) keyword can be used to prevent overflow checking.  
  
## Example  
 This sample shows how to use `checked` to enable overflow checking at run time.  
  
 [!CODE [csrefKeywordsChecked#1](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsChecked#1)]  
  
## C# Language Specification  
 [!INCLUDE[CSharplangspec](../vs140/includes/Csharplangspec_md.md)]  
  
## See Also  
 [C# Reference](../vs140/C#-Reference.md)   
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [C# Keywords](../Topic/C%23%20Keywords.md)   
 [Checked and Unchecked](../vs140/Checked-and-Unchecked--C#-Reference-.md)   
 [unchecked](../vs140/unchecked--C#-Reference-.md)