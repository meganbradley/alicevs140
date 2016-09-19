---
title: "Namespaces (C# Programming Guide)"
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
ms.assetid: b1c4ab46-3fad-4ffa-9deb-dd50a2d8c65a
caps.latest.revision: 29
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Namespaces (C# Programming Guide)
Namespaces are heavily used in C# programming in two ways. First, the .NET Framework uses namespaces to organize its many classes, as follows:  
  
 [!CODE [csProgGuide#22](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuide#22)]  
  
 `System` is a namespace and `Console` is a class in that namespace. The `using` keyword can be used so that the complete name is not required, as in the following example:  
  
 [!CODE [csProgGuide#1](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuide#1)]  
  
 [!CODE [csProgGuide#25](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuide#25)]  
  
 For more information, see [using clause](../Topic/using%20Directive%20\(C%23%20Reference\).md).  
  
 Second, declaring your own namespaces can help you control the scope of class and method names in larger programming projects. Use the [namespace](../vs140/namespace--C#-Reference-.md) keyword to declare a namespace, as in the following example:  
  
 [!CODE [csProgGuideNamespaces#6](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideNamespaces#6)]  
  
## Namespaces Overview  
 Namespaces have the following properties:  
  
-   They organize large code projects.  
  
-   They are delimited by using the `.` operator.  
  
-   The `using directive` obviates the requirement to specify the name of the namespace for every class.  
  
-   The `global` namespace is the "root" namespace: `global::System` will always refer to the .NET Framework namespace `System`.  
  
## Related Sections  
 See the following topics for more information about namespaces:  
  
-   [Using Namespaces (C#)](../vs140/Using-Namespaces--C#-Programming-Guide-.md)  
  
-   [How to: Use the Global Namespace Qualifier](../Topic/How%20to:%20Use%20the%20Global%20Namespace%20Alias%20\(C%23%20Programming%20Guide\).md)  
  
-   [How to: Use the My Namespace (Visual C#)](../Topic/How%20to:%20Use%20the%20My%20Namespace%20\(C%23%20Programming%20Guide\).md)  
  
## C# Language Specification  
 [!INCLUDE[CSharplangspec](../vs140/includes/Csharplangspec_md.md)]  
  
## See Also  
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [Namespace Keywords](../vs140/Namespace-Keywords--C#-Reference-.md)   
 [using directive](../Topic/using%20Directive%20\(C%23%20Reference\).md)   
 [:: Operator](../vs140/---Operator--C#-Reference-.md)   
 [. Operator](../vs140/.-Operator--C#-Reference-.md)