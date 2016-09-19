---
title: "public (C# Reference)"
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
ms.assetid: 0ae45d16-a551-4b74-9845-57208de1328e
caps.latest.revision: 23
translation.priority.ht: 
  - de-de
  - ja-jp
---
# public (C# Reference)
The `public` keyword is an access modifier for types and type members. Public access is the most permissive access level. There are no restrictions on accessing public members, as in this example:  
  
```  
class SampleClass  
{  
    public int x; // No access restrictions.  
}  
```  
  
 See [Access Modifiers (C# Programming Guide)](../Topic/Access%20Modifiers%20\(C%23%20Programming%20Guide\).md) and [Accessibility Levels](../vs140/Accessibility-Levels--C#-Reference-.md) for more information.  
  
## Example  
 In the following example, two classes are declared, `PointTest` and `MainClass`. The public members `x` and `y` of `PointTest` are accessed directly from `MainClass`.  
  
 [!CODE [csrefKeywordsModifiers#13](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsModifiers#13)]  
  
 If you change the `public` access level to [private](../vs140/private--C#-Reference-.md) or [protected](../vs140/protected--C#-Reference-.md), you will get the error message:  
  
 'PointTest.y' is inaccessible due to its protection level.  
  
## C# Language Specification  
 [!INCLUDE[CSharplangspec](../vs140/includes/Csharplangspec_md.md)]  
  
## See Also  
 [C# Programmer's Reference](../vs140/C#-Reference.md)   
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [Access Modifiers (C# Programming Guide)](../Topic/Access%20Modifiers%20\(C%23%20Programming%20Guide\).md)   
 [C# Keywords](../Topic/C%23%20Keywords.md)   
 [Access Modifiers](../vs140/Access-Modifiers--C#-Reference-.md)   
 [Accessibility Levels](../vs140/Accessibility-Levels--C#-Reference-.md)   
 [Modifiers](../vs140/Modifiers--C#-Reference-.md)   
 [private (C# Programmer's Reference)](../vs140/private--C#-Reference-.md)   
 [protected (C# Programmer's Reference)](../vs140/protected--C#-Reference-.md)   
 [internal (C# Programmer's Reference)](../vs140/internal--C#-Reference-.md)