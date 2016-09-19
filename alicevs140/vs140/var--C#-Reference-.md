---
title: "var (C# Reference)"
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
ms.assetid: 0777850a-2691-4e3e-927f-0c850f5efe15
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# var (C# Reference)
Beginning in Visual C# 3.0, variables that are declared at method scope can have an implicit type `var`. An implicitly typed local variable is strongly typed just as if you had declared the type yourself, but the compiler determines the type. The following two declarations of `i` are functionally equivalent:  
  
```  
var i = 10; // implicitly typed  
int i = 10; //explicitly typed  
```  
  
 For more information, see [Implicitly Typed Local Variables (C# Programming Guide)](../vs140/Implicitly-Typed-Local-Variables--C#-Programming-Guide-.md) and [Type Relationships in Query Operations (LINQ)](../vs140/Type-Relationships-in-LINQ-Query-Operations--C#-.md).  
  
## Example  
 The following example shows two query expressions. In the first expression, the use of `var` is permitted but is not required, because the type of the query result can be stated explicitly as an `IEnumerable<string>`. However, in the second expression, `var` must be used because the result is a collection of anonymous types, and the name of that type is not accessible except to the compiler itself. Note that in Example #2, the `foreach` iteration variable `item` must also be implicitly typed.  
  
 [!CODE [csrefKeywordsTypes#18](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsTypes#18)]  
  
## See Also  
 [C# Reference](../vs140/C#-Reference.md)   
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [Implicitly Typed Local Variables (C# Programming Guide)](../vs140/Implicitly-Typed-Local-Variables--C#-Programming-Guide-.md)