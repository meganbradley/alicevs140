---
title: "as (C# Reference)"
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
ms.assetid: a9be126b-cbf4-4990-a70d-d0e1983cad0e
caps.latest.revision: 26
translation.priority.ht: 
  - de-de
  - ja-jp
---
# as (C# Reference)
You can use the `as` operator to perform certain types of conversions between compatible reference types or [nullable types](../Topic/Nullable%20Types%20\(C%23%20Programming%20Guide\).md). The following code shows an example.  
  
 [!CODE [csrefKeywordsOperator#1](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsOperator#1)]  
  
## Remarks  
 The `as` operator is like a cast operation. However, if the conversion isn't possible, `as` returns `null` instead of raising an exception. Consider the following example:  
  
```  
expression as type  
```  
  
 The code is equivalent to the following expression except that the `expression` variable is evaluated only one time.  
  
```  
expression is type ? (type)expression : (type)null  
```  
  
 Note that the `as` operator performs only reference conversions, nullable conversions, and boxing conversions. The `as` operator can't perform other conversions, such as user-defined conversions, which should instead be performed by using cast expressions.  
  
## Example  
 [!CODE [csrefKeywordsOperator#2](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsOperator#2)]  
  
## C# Language Specification  
 [!INCLUDE[CSharplangspec](../vs140/includes/Csharplangspec_md.md)]  
  
## See Also  
 [C# Reference](../vs140/C#-Reference.md)   
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [C# Keywords](../Topic/C%23%20Keywords.md)   
 [is](../vs140/is--C#-Reference-.md)   
 [?: Operator](../vs140/---Operator--C#-Reference-.md)   
 [Operator Keywords](../vs140/Operator-Keywords--C#-Reference-.md)