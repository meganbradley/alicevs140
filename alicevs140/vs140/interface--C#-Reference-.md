---
title: "interface (C# Reference)"
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
ms.assetid: 7da38e81-4f99-4bc5-b07d-c986b687eeba
caps.latest.revision: 31
translation.priority.ht: 
  - de-de
  - ja-jp
---
# interface (C# Reference)
An interface contains only the signatures of [methods](../Topic/Methods%20\(C%23%20Programming%20Guide\).md), [properties](../vs140/Properties--C#-Programming-Guide-.md), [events](../Topic/Events%20\(C%23%20Programming%20Guide\).md) or [indexers](../vs140/Indexers--C#-Programming-Guide-.md). A class or struct that implements the interface must implement the members of the interface that are specified in the interface definition. In the following example, class `ImplementationClass` must implement a method named `SampleMethod` that has no parameters and returns `void`.  
  
 For more information and examples, see [Interfaces (C# Programming Guide)](../Topic/Interfaces%20\(C%23%20Programming%20Guide\).md).  
  
## Example  
 [!CODE [csrefKeywordsTypes#14](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsTypes#14)]  
  
 An interface can be a member of a namespace or a class and can contain signatures of the following members:  
  
-   [Methods](../Topic/Methods%20\(C%23%20Programming%20Guide\).md)  
  
-   [Properties](../vs140/Using-Properties--C#-Programming-Guide-.md)  
  
-   [Indexers](../Topic/Using%20Indexers%20\(C%23%20Programming%20Guide\).md)  
  
-   [Events](../Topic/event%20\(C%23%20Reference\).md)  
  
 An interface can inherit from one or more base interfaces.  
  
 When a base type list contains a base class and interfaces, the base class must come first in the list.  
  
 A class that implements an interface can explicitly implement members of that interface. An explicitly implemented member cannot be accessed through a class instance, but only through an instance of the interface.  
  
 For more details and code examples on explicit interface implementation, see [Explicit Interface Implementation (Visual C#)](../vs140/Explicit-Interface-Implementation--C#-Programming-Guide-.md).  
  
## Example  
 The following example demonstrates interface implementation. In this example, the interface contains the property declaration and the class contains the implementation. Any instance of a class that implements `IPoint` has integer properties `x` and `y`.  
  
 [!CODE [csrefKeywordsTypes#15](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsTypes#15)]  
  
## C# Language Specification  
 [!INCLUDE[CSharplangspec](../vs140/includes/Csharplangspec_md.md)]  
  
## See Also  
 [C# Reference](../vs140/C#-Reference.md)   
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [C# Keywords](../Topic/C%23%20Keywords.md)   
 [Reference Types](../vs140/Reference-Types--C#-Reference-.md)   
 [Interfaces](../Topic/Interfaces%20\(C%23%20Programming%20Guide\).md)   
 [Using Properties](../vs140/Using-Properties--C#-Programming-Guide-.md)   
 [Using Indexers](../Topic/Using%20Indexers%20\(C%23%20Programming%20Guide\).md)   
 [class](../vs140/class--C#-Reference-.md)   
 [struct](../vs140/struct--C#-Reference-.md)   
 [Interfaces (C# Programming Guide)](../Topic/Interfaces%20\(C%23%20Programming%20Guide\).md)