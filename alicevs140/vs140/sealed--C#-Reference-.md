---
title: "sealed (C# Reference)"
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
ms.assetid: 8e4ed5d3-10be-47db-9488-0da2008e6f3f
caps.latest.revision: 32
translation.priority.ht: 
  - de-de
  - ja-jp
---
# sealed (C# Reference)
When applied to a class, the `sealed` modifier prevents other classes from inheriting from it. In the following example, class `B` inherits from class `A`, but no class can inherit from class `B`.  
  
```  
class A {}      
sealed class B : A {}  
```  
  
 You can also use the `sealed` modifier on a method or property that overrides a virtual method or property in a base class. This enables you to allow classes to derive from your class and prevent them from overriding specific virtual methods or properties.  
  
## Example  
 In the following example, `Z` inherits from `Y` but `Z` cannot override the virtual function `F` that is declared in `X` and sealed in `Y`.  
  
 [!CODE [csrefKeywordsModifiers#16](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsModifiers#16)]  
  
 When you define new methods or properties in a class, you can prevent deriving classes from overriding them by not declaring them as [virtual](../vs140/virtual--C#-Reference-.md).  
  
 It is an error to use the [abstract](../vs140/abstract--C#-Reference-.md) modifier with a sealed class, because an abstract class must be inherited by a class that provides an implementation of the abstract methods or properties.  
  
 When applied to a method or property, the `sealed` modifier must always be used with [override](../vs140/override--C#-Reference-.md).  
  
 Because structs are implicitly sealed, they cannot be inherited.  
  
 For more information, see [Inheritance (Visual C#)](../Topic/Inheritance%20\(C%23%20Programming%20Guide\).md).  
  
 For more examples, see [Abstract and Sealed Classes and Class Members (C# Programming Guide)](../vs140/Abstract-and-Sealed-Classes-and-Class-Members--C#-Programming-Guide-.md).  
  
## Example  
 [!CODE [csrefKeywordsModifiers#17](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsModifiers#17)]  
  
 In the previous example, you might try to inherit from the sealed class by using the following statement:  
  
 `class MyDerivedC: SealedClass {}   // Error`  
  
 The result is an error message:  
  
 `'MyDerivedC' cannot inherit from sealed class 'SealedClass'.`  
  
## C# Language Specification  
 [!INCLUDE[CSharplangspec](../vs140/includes/Csharplangspec_md.md)]  
  
## Remarks  
 To determine whether to seal a class, method, or property, you should generally consider the following two points:  
  
-   The potential benefits that deriving classes might gain through the ability to customize your class.  
  
-   The potential that deriving classes could modify your classes in such a way that they would no longer work correctly or as expected.  
  
## See Also  
 [C# Reference](../vs140/C#-Reference.md)   
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [C# Keywords](../Topic/C%23%20Keywords.md)   
 [Static Classes and Static Class Members](../Topic/Static%20Classes%20and%20Static%20Class%20Members%20\(C%23%20Programming%20Guide\).md)   
 [Abstract and Sealed Classes and Class Members (Visual C#)](../vs140/Abstract-and-Sealed-Classes-and-Class-Members--C#-Programming-Guide-.md)   
 [Access Modifiers (Visual C#)](../Topic/Access%20Modifiers%20\(C%23%20Programming%20Guide\).md)   
 [Modifiers](../vs140/Modifiers--C#-Reference-.md)   
 [override (C# Reference)](../vs140/override--C#-Reference-.md)   
 [virtual (C# Reference)](../vs140/virtual--C#-Reference-.md)