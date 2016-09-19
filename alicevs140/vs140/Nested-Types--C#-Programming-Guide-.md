---
title: "Nested Types (C# Programming Guide)"
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
ms.assetid: f2e1b315-e3d1-48ce-977f-7bae0960ba99
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Nested Types (C# Programming Guide)
A type defined within a [class](../vs140/class--C#-Reference-.md) or [struct](../vs140/struct--C#-Reference-.md) is called a nested type. For example:  
  
 [!CODE [csProgGuideObjects#68](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideObjects#68)]  
  
 Regardless of whether the outer type is a class or a struct, nested types default to [private](../vs140/private--C#-Reference-.md), but can be made [public](../vs140/public--C#-Reference-.md), protected internal, [protected](../vs140/protected--C#-Reference-.md), [internal](../vs140/internal--C#-Reference-.md), or [private](../vs140/private--C#-Reference-.md). In the previous example, `Nested` is inaccessible to external types, but can be made public like this:  
  
 [!CODE [csProgGuideObjects#69](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideObjects#69)]  
  
 The nested, or inner type can access the containing, or outer type. To access the containing type, pass it as a constructor to the nested type. For example:  
  
 [!CODE [csProgGuideObjects#70](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideObjects#70)]  
  
 A nested type has access to all of the members that are accessible to its containing type. It can access private and protected members of the containing type, including any inherited protected members.  
  
 In the previous declaration, the full name of class `Nested` is `Container.Nested`. This is the name used to create a new instance of the nested class, as follows:  
  
 [!CODE [csProgGuideObjects#71](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideObjects#71)]  
  
## See Also  
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [Classes and Structs (Visual C#)](../Topic/Classes%20and%20Structs%20\(C%23%20Programming%20Guide\).md)   
 [Access Modifiers (Visual C#)](../Topic/Access%20Modifiers%20\(C%23%20Programming%20Guide\).md)   
 [Constructors (C# Programming Guide)](../vs140/Constructors--C#-Programming-Guide-.md)