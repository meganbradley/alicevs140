---
title: "= Operator (C# Reference)"
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
ms.assetid: d802a6d5-32f0-42b8-b180-12f5a081bfc1
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# = Operator (C# Reference)
The assignment operator (`=`) stores the value of its right-hand operand in the storage location, property, or indexer denoted by its left-hand operand and returns the value as its result. The operands must be of the same type (or the right-hand operand must be implicitly convertible to the type of the left-hand operand).  
  
## Remarks  
 The assignment operator cannot be overloaded. However, you can define implicit conversion operators for a type, which enable you to use the assignment operator with those types. For more information, see [Using Conversion Operators (C# Programming Guide)](../vs140/Using-Conversion-Operators--C#-Programming-Guide-.md).  
  
## Example  
 [!CODE [csRefOperators#49](../CodeSnippet/VS_Snippets_VBCSharp/csrefOperators#49)]  
  
## See Also  
 [C# Programmer's Reference](../vs140/C#-Reference.md)   
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [C# Operators](../Topic/C%23%20Operators.md)