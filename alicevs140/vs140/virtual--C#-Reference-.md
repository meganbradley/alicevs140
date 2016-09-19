---
title: "virtual (C# Reference)"
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
ms.assetid: 5da9abae-bc1e-434f-8bea-3601b8dcb3b2
caps.latest.revision: 28
translation.priority.ht: 
  - de-de
  - ja-jp
---
# virtual (C# Reference)
The `virtual` keyword is used to modify a method, property, indexer, or event declaration and allow for it to be overridden in a derived class. For example, this method can be overridden by any class that inherits it:  
  
```  
public virtual double Area()   
{  
    return x * y;  
}  
```  
  
 The implementation of a virtual member can be changed by an [overriding member](../vs140/override--C#-Reference-.md) in a derived class. For more information about how to use the `virtual` keyword, see [Versioning with the Override and New Keywords (C#)](../vs140/Versioning-with-the-Override-and-New-Keywords--C#-Programming-Guide-.md) and [Knowing when to use Override and New Keywords](../vs140/Knowing-When-to-Use-Override-and-New-Keywords--C#-Programming-Guide-.md).  
  
## Remarks  
 When a virtual method is invoked, the run-time type of the object is checked for an overriding member. The overriding member in the most derived class is called, which might be the original member, if no derived class has overridden the member.  
  
 By default, methods are non-virtual. You cannot override a non-virtual method.  
  
 You cannot use the `virtual` modifier with the `static`, `abstract, private`, or `override` modifiers. The following example shows a virtual property:  
  
 [!CODE [csrefKeywordsModifiers#26](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsModifiers#26)]  
  
 Virtual properties behave like abstract methods, except for the differences in declaration and invocation syntax.  
  
-   It is an error to use the `virtual` modifier on a static property.  
  
-   A virtual inherited property can be overridden in a derived class by including a property declaration that uses the `override` modifier.  
  
## Example  
 In this example, the `Shape` class contains the two coordinates `x`, `y`, and the `Area()` virtual method. Different shape classes such as `Circle`, `Cylinder`, and `Sphere` inherit the `Shape` class, and the surface area is calculated for each figure. Each derived class has it own override implementation of `Area()`.  
  
 Notice that the inherited classes `Circle`, `Sphere`, and `Cylinder` all use constructors that initialize the base class, as shown in the following declaration.  
  
```  
public Cylinder(double r, double h): base(r, h) {}  
```  
  
 The following program calculates and displays the appropriate area for each figure by invoking the appropriate implementation of the `Area()` method, according to the object that is associated with the method.  
  
 [!CODE [csrefKeywordsModifiers#23](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsModifiers#23)]  
  
## C# Language Specification  
 [!INCLUDE[CSharplangspec](../vs140/includes/Csharplangspec_md.md)]  
  
## See Also  
 [C# Reference](../vs140/C#-Reference.md)   
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [Modifiers](../vs140/Modifiers--C#-Reference-.md)   
 [C# Keywords](../Topic/C%23%20Keywords.md)   
 [Polymorphism (Visual C#)](../Topic/Polymorphism%20\(C%23%20Programming%20Guide\).md)   
 [abstract](../vs140/abstract--C#-Reference-.md)   
 [override (C# Programmer's Reference)](../vs140/override--C#-Reference-.md)   
 [new (C# Programmer's Reference)](../vs140/new--C#-Reference-.md)