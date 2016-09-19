---
title: "false Operator (C# Reference)"
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
ms.assetid: 81a888fd-011e-4589-b242-6c261fea505e
caps.latest.revision: 23
translation.priority.ht: 
  - de-de
  - ja-jp
---
# false Operator (C# Reference)
Returns the [bool](../Topic/bool%20\(C%23%20Reference\).md) value `true` to indicate that an operand is `false` and returns `false` otherwise.  
  
 Prior to C# 2.0, the `true` and `false` operators were used to create user-defined nullable value types that were compatible with types such as `SqlBool`. However, the language now provides built-in support for nullable value types, and whenever possible you should use those instead of overloading the `true` and `false` operators. For more information, see [Nullable Types (C# Programming Guide)](../Topic/Nullable%20Types%20\(C%23%20Programming%20Guide\).md).  
  
 With nullable Booleans, the expression `a != b` is not necessarily equal to `!(a == b)` because one or both of the values might be null. You have to overload both the `true` and `false` operators separately to correctly handle the null values in the expression. The following example shows how to overload and use the `true` and `false` operators.  
  
 [!CODE [csrefKeywordsOperator#16](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsOperator#16)]  
  
 A type that overloads the `true` and `false` operators can be used for the controlling expression in [if](../vs140/if-else--C#-Reference-.md), [do](../vs140/do--C#-Reference-.md), [while](../vs140/while--C#-Reference-.md), and [for](../vs140/for--C#-Reference-.md) statements and in [conditional expressions](../vs140/---Operator--C#-Reference-.md).  
  
 If a type defines operator `false`, it must also define operator [true](../vs140/true--C#-Reference-.md).  
  
 A type cannot directly overload the conditional logical operators [&&](../vs140/---Operator--C#-Reference-.md) and [&#124;&#124;](../vs140/---Operator--C#-Reference-.md), but an equivalent effect can be achieved by overloading the regular logical operators and operators `true` and `false`.  
  
## C# Language Specification  
 [!INCLUDE[CSharplangspec](../vs140/includes/Csharplangspec_md.md)]  
  
## See Also  
 [C# Reference](../vs140/C#-Reference.md)   
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [C# Keywords](../Topic/C%23%20Keywords.md)   
 [C# Operators](../Topic/C%23%20Operators.md)   
 [true](../vs140/true--C#-Reference-.md)