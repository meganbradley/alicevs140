---
title: "params (C# Reference)"
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
ms.assetid: 1690815e-b52b-4967-8380-5780aff08012
caps.latest.revision: 26
translation.priority.ht: 
  - de-de
  - ja-jp
---
# params (C# Reference)
By using the `params` keyword, you can specify a [method parameter](../vs140/Method-Parameters--C#-Reference-.md) that takes a variable number of arguments.  
  
 You can send a comma-separated list of arguments of the type specified in the parameter declaration or an array of arguments of the specified type. You also can send no arguments. If you send no arguments, the length of the `params` list is zero.  
  
 No additional parameters are permitted after the `params` keyword in a method declaration, and only one `params` keyword is permitted in a method declaration.  
  
## Example  
 The following example demonstrates various ways in which arguments can be sent to a `params` parameter.  
  
 [!CODE [csrefKeywordsMethodParams#5](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsMethodParams#5)]  
  
## C# Language Specification  
 [!INCLUDE[CSharplangspec](../vs140/includes/Csharplangspec_md.md)]  
  
## See Also  
 [C# Reference](../vs140/C#-Reference.md)   
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [C# Keywords](../Topic/C%23%20Keywords.md)   
 [Method Parameters](../vs140/Method-Parameters--C#-Reference-.md)