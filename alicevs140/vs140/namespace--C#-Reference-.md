---
title: "namespace (C# Reference)"
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
ms.assetid: 0a788423-9110-42e0-97d9-bda41ca4870f
caps.latest.revision: 30
translation.priority.ht: 
  - de-de
  - ja-jp
---
# namespace (C# Reference)
The `namespace` keyword is used to declare a scope that contains a set of related objects. You can use a namespace to organize code elements and to create globally unique types.  
  
 [!CODE [csrefKeywordsNamespace#1](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsNamespace#1)]  
  
## Remarks  
 Within a namespace, you can declare one or more of the following types:  
  
-   another namespace  
  
-   [class](../vs140/class--C#-Reference-.md)  
  
-   [interface](../vs140/interface--C#-Reference-.md)  
  
-   [struct](../vs140/struct--C#-Reference-.md)  
  
-   [enum](../Topic/enum%20\(C%23%20Reference\).md)  
  
-   [delegate](../vs140/delegate--C#-Reference-.md)  
  
 Whether or not you explicitly declare a namespace in a C# source file, the compiler adds a default namespace. This unnamed namespace, sometimes referred to as the global namespace, is present in every file. Any identifier in the global namespace is available for use in a named namespace.  
  
 Namespaces implicitly have public access and this is not modifiable. For a discussion of the access modifiers you can assign to elements in a namespace, see [Access Modifiers](../vs140/Access-Modifiers--C#-Reference-.md).  
  
 It is possible to define a namespace in two or more declarations. For example, the following example defines two classes as part of the `MyCompany` namespace:  
  
 [!CODE [csrefKeywordsNamespace#2](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsNamespace#2)]  
  
## Example  
 The following example shows how to call a static method in a nested namespace.  
  
 [!CODE [csrefKeywordsNamespace#3](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsNamespace#3)]  
  
## For More Information  
 For more information about using namespaces, see the following topics:  
  
-   [Namespaces (C#)](../vs140/Namespaces--C#-Programming-Guide-.md)  
  
-   [Using Namespaces (C#)](../vs140/Using-Namespaces--C#-Programming-Guide-.md)  
  
-   [How to: Use the Global Namespace Qualifier (C#)](../Topic/How%20to:%20Use%20the%20Global%20Namespace%20Alias%20\(C%23%20Programming%20Guide\).md)  
  
## C# Language Specification  
 [!INCLUDE[CSharplangspec](../vs140/includes/Csharplangspec_md.md)]  
  
## See Also  
 [C# Reference](../vs140/C#-Reference.md)   
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [C# Keywords](../Topic/C%23%20Keywords.md)   
 [Namespace Keywords](../vs140/Namespace-Keywords--C#-Reference-.md)   
 [using](../vs140/using--C#-Reference-.md)