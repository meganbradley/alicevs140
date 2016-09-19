---
title: "override (C# Reference)"
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
ms.assetid: dd1907a8-acf8-46d3-80b9-c2ca4febada8
caps.latest.revision: 28
translation.priority.ht: 
  - de-de
  - ja-jp
---
# override (C# Reference)
The `override` modifier is required to extend or modify the abstract or virtual implementation of an inherited method, property, indexer, or event.  
  
## Example  
 In this example, the `Square` class must provide an overridden implementation of `Area` because `Area` is inherited from the abstract `ShapesClass`:  
  
 [!CODE [csrefKeywordsModifiers#1](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsModifiers#1)]  
  
 An `override` method provides a new implementation of a member that is inherited from a base class. The method that is overridden by an `override` declaration is known as the overridden base method. The overridden base method must have the same signature as the `override` method. For information about inheritance, see [Inheritance](../Topic/Inheritance%20\(C%23%20Programming%20Guide\).md).  
  
 You cannot override a non-virtual or static method. The overridden base method must be `virtual`, `abstract`, or `override`.  
  
 An `override` declaration cannot change the accessibility of the `virtual` method. Both the `override` method and the `virtual` method must have the same [access level modifier](../vs140/Access-Modifiers--C#-Reference-.md).  
  
 You cannot use the `new`, `static`, or `virtual` modifiers to modify an `override` method.  
  
 An overriding property declaration must specify exactly the same access modifier, type, and name as the inherited property, and the overridden property must be `virtual`, `abstract`, or `override`.  
  
 For more information about how to use the `override` keyword, see [Versioning with the Override and New Keywords](../vs140/Versioning-with-the-Override-and-New-Keywords--C#-Programming-Guide-.md) and [Knowing when to use Override and New Keywords](../vs140/Knowing-When-to-Use-Override-and-New-Keywords--C#-Programming-Guide-.md).  
  
## Example  
 This example defines a base class named `Employee`, and a derived class named `SalesEmployee`. The `SalesEmployee` class includes an extra property, `salesbonus`, and overrides the method `CalculatePay` in order to take it into account.  
  
 [!CODE [csrefKeywordsModifiers#9](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsModifiers#9)]  
  
## C# Language Specification  
 [!INCLUDE[CSharplangspec](../vs140/includes/Csharplangspec_md.md)]  
  
## See Also  
 [C# Reference](../vs140/C#-Reference.md)   
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [Inheritance (Visual C#)](../Topic/Inheritance%20\(C%23%20Programming%20Guide\).md)   
 [C# Keywords](../Topic/C%23%20Keywords.md)   
 [Modifiers](../vs140/Modifiers--C#-Reference-.md)   
 [abstract](../vs140/abstract--C#-Reference-.md)   
 [virtual](../vs140/virtual--C#-Reference-.md)   
 [new (C# Programmer's Reference)](../vs140/new--C#-Reference-.md)   
 [Polymorphism (Visual C#)](../Topic/Polymorphism%20\(C%23%20Programming%20Guide\).md)