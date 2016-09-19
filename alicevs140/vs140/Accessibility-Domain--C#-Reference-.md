---
title: "Accessibility Domain (C# Reference)"
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
ms.assetid: 8af779c1-275b-44be-a864-9edfbca71bcc
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Accessibility Domain (C# Reference)
The accessibility domain of a member specifies in which program sections a member can be referenced. If the member is nested within another type, its accessibility domain is determined by both the [accessibility level](../vs140/Accessibility-Levels--C#-Reference-.md) of the member and the accessibility domain of the immediately containing type.  
  
 The accessibility domain of a top-level type is at least the program text of the project that it is declared in. That is, the domain includes all of the source files of this project. The accessibility domain of a nested type is at least the program text of the type in which it is declared. That is, the domain is the type body, which includes all nested types. The accessibility domain of a nested type never exceeds that of the containing type. These concepts are demonstrated in the following example.  
  
## Example  
 This example contains a top-level type, `T1`, and two nested classes, `M1` and `M2`. The classes contain fields that have different declared accessibilities. In the `Main` method, a comment follows each statement to indicate the accessibility domain of each member. Notice that the statements that try to reference the inaccessible members are commented out. If you want to see the compiler errors caused by referencing an inaccessible member, remove the comments one at a time.  
  
 [!CODE [csrefKeywordsModifiers#4](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsModifiers#4)]  
  
## C# Language Specification  
 [!INCLUDE[CSharplangspec](../vs140/includes/Csharplangspec_md.md)]  
  
## See Also  
 [C# Programmer's Reference](../vs140/C#-Reference.md)   
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [C# Keywords](../Topic/C%23%20Keywords.md)   
 [Access Modifiers](../vs140/Access-Modifiers--C#-Reference-.md)   
 [Accessibility Levels](../vs140/Accessibility-Levels--C#-Reference-.md)   
 [Restrictions on Using Accessibility Levels](../vs140/Restrictions-on-Using-Accessibility-Levels--C#-Reference-.md)   
 [Access Modifiers (Visual C#)](../Topic/Access%20Modifiers%20\(C%23%20Programming%20Guide\).md)   
 [public (C# Programmer's Reference)](../vs140/public--C#-Reference-.md)   
 [private (C# Programmer's Reference)](../vs140/private--C#-Reference-.md)   
 [protected (C# Programmer's Reference)](../vs140/protected--C#-Reference-.md)   
 [internal (C# Programmer's Reference)](../vs140/internal--C#-Reference-.md)