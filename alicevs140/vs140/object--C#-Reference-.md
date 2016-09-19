---
title: "object (C# Reference)"
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
ms.assetid: 93f60c0b-e17a-40a9-9362-cca5fb77b0e7
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# object (C# Reference)
The `object` type is an alias for <xref:System.Object?qualifyHint=False> in the .NET Framework. In the unified type system of C#, all types, predefined and user-defined, reference types and value types, inherit directly or indirectly from <xref:System.Object?qualifyHint=False>. You can assign values of any type to variables of type `object`. When a variable of a value type is converted to object, it is said to be *boxed*. When a variable of type object is converted to a value type, it is said to be *unboxed*. For more information, see [Boxing and Unboxing](../Topic/Boxing%20and%20Unboxing%20\(C%23%20Programming%20Guide\).md).  
  
## Example  
 The following sample shows how variables of type `object` can accept values of any data type and how variables of type `object` can use methods on <xref:System.Object?qualifyHint=False> from the .NET Framework.  
  
 [!CODE [csrefKeywordsTypes#16](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsTypes#16)]  
  
## C# Language Specification  
 [!INCLUDE[CSharplangspec](../vs140/includes/Csharplangspec_md.md)]  
  
## See Also  
 [C# Reference](../vs140/C#-Reference.md)   
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [C# Keywords](../Topic/C%23%20Keywords.md)   
 [Reference Types](../vs140/Reference-Types--C#-Reference-.md)   
 [Value Types](../Topic/Value%20Types%20\(C%23%20Reference\).md)