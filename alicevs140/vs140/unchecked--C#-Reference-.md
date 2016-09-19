---
title: "unchecked (C# Reference)"
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
ms.assetid: 0c021f7c-923f-4b3d-a58f-55336f5ac27e
caps.latest.revision: 25
translation.priority.ht: 
  - de-de
  - ja-jp
---
# unchecked (C# Reference)
The `unchecked` keyword is used to suppress overflow-checking for integral-type arithmetic operations and conversions.  
  
 In an unchecked context, if an expression produces a value that is outside the range of the destination type, the overflow is not flagged. For example, because the calculation in the following example is performed in an `unchecked` block or expression, the fact that the result is too large for an integer is ignored, and `int1` is assigned the value -2,147,483,639.  
  
 [!CODE [csrefKeywordsChecked#5](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsChecked#5)]  
  
 If the `unchecked` environment is removed, a compilation error occurs. The overflow can be detected at compile time because all the terms of the expression are constants.  
  
 Expressions that contain non-constant terms are unchecked by default at compile time and run time. See [checked (C# Reference)](../vs140/checked--C#-Reference-.md) for information about enabling a checked environment.  
  
 Because checking for overflow takes time, the use of unchecked code in situations where there is no danger of overflow might improve performance. However, if overflow is a possibility, a checked environment should be used.  
  
## Example  
 This sample shows how to use the `unchecked` keyword.  
  
 [!CODE [csrefKeywordsChecked#2](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsChecked#2)]  
  
## C# Language Specification  
 [!INCLUDE[CSharplangspec](../vs140/includes/Csharplangspec_md.md)]  
  
## See Also  
 [C# Reference](../vs140/C#-Reference.md)   
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [C# Keywords](../Topic/C%23%20Keywords.md)   
 [Checked and Unchecked](../vs140/Checked-and-Unchecked--C#-Reference-.md)   
 [checked](../vs140/checked--C#-Reference-.md)