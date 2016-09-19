---
title: "Checked and Unchecked (C# Reference)"
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
ms.assetid: a84bc877-2c7f-4396-8735-1ce97c42f35e
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Checked and Unchecked (C# Reference)
C# statements can execute in either checked or unchecked context. In a checked context, arithmetic overflow raises an exception. In an unchecked context, arithmetic overflow is ignored and the result is truncated.  
  
-   [checked](../vs140/checked--C#-Reference-.md) Specify checked context.  
  
-   [unchecked](../vs140/unchecked--C#-Reference-.md) Specify unchecked context.  
  
 If neither `checked` nor `unchecked` is specified, the default context depends on external factors such as compiler options.  
  
 The following operations are affected by the overflow checking:  
  
-   Expressions using the following predefined operators on integral types:  
  
     `++` `--` - (unary)   `+` -   `*` `/`  
  
-   Explicit numeric conversions between integral types.  
  
 The [/checked](../Topic/-checked%20\(C%23%20Compiler%20Options\).md) compiler option lets you specify checked or unchecked context for all integer arithmetic statements that are not explicitly in the scope of a `checked` or `unchecked` keyword.  
  
## See Also  
 [C# Reference](../vs140/C#-Reference.md)   
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [C# Keywords](../Topic/C%23%20Keywords.md)   
 [Statement Keywords](../vs140/Statement-Keywords--C#-Reference-.md)