---
title: "abstract (C# Reference)"
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
ms.assetid: b0797770-c1f3-4b4d-9441-b9122602a6bb
caps.latest.revision: 26
translation.priority.ht: 
  - de-de
  - ja-jp
---
# abstract (C# Reference)
The `abstract` modifier indicates that the thing being modified has a missing or incomplete implementation. The abstract modifier can be used with classes, methods, properties, indexers, and events. Use the `abstract` modifier in a class declaration to indicate that a class is intended only to be a base class of other classes. Members marked as abstract, or included in an abstract class, must be implemented by classes that derive from the abstract class.  
  
## Example  
 In this example, the class `Square` must provide an implementation of `Area` because it derives from `ShapesClass`:  
  
 [!CODE [csrefKeywordsModifiers#1](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsModifiers#1)]  
  
 Abstract classes have the following features:  
  
-   An abstract class cannot be instantiated.  
  
-   An abstract class may contain abstract methods and accessors.  
  
-   It is not possible to modify an abstract class with the [sealed](../vs140/sealed--C#-Reference-.md) modifier because the two modifers have opposite meanings. The `sealed` modifier prevents a class from being inherited and the `abstract` modifier requires a class to be inherited.  
  
-   A non-abstract class derived from an abstract class must include actual implementations of all inherited abstract methods and accessors.  
  
 Use the `abstract` modifier in a method or property declaration to indicate that the method or property does not contain implementation.  
  
 Abstract methods have the following features:  
  
-   An abstract method is implicitly a virtual method.  
  
-   Abstract method declarations are only permitted in abstract classes.  
  
-   Because an abstract method declaration provides no actual implementation, there is no method body; the method declaration simply ends with a semicolon and there are no curly braces ({ }) following the signature. For example:  
  
    ```  
    public abstract void MyMethod();  
    ```  
  
     The implementation is provided by an overriding method[override](../vs140/override--C#-Reference-.md), which is a member of a non-abstract class.  
  
-   It is an error to use the [static](../vs140/static--C#-Reference-.md) or [virtual](../vs140/virtual--C#-Reference-.md) modifiers in an abstract method declaration.  
  
 Abstract properties behave like abstract methods, except for the differences in declaration and invocation syntax.  
  
-   It is an error to use the `abstract` modifier on a static property.  
  
-   An abstract inherited property can be overridden in a derived class by including a property declaration that uses the [override](../vs140/override--C#-Reference-.md) modifier.  
  
 For more information about abstract classes, see [Abstract and Sealed Classes and Class Members (Visual C#)](../vs140/Abstract-and-Sealed-Classes-and-Class-Members--C#-Programming-Guide-.md).  
  
 An abstract class must provide implementation for all interface members.  
  
 An abstract class that implements an interface might map the interface methods onto abstract methods. For example:  
  
 [!CODE [csrefKeywordsModifiers#2](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsModifiers#2)]  
  
## Example  
 In this example, the class `DerivedClass` is derived from an abstract class `BaseClass`. The abstract class contains an abstract method, `AbstractMethod`, and two abstract properties, `X` and `Y`.  
  
 [!CODE [csrefKeywordsModifiers#3](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsModifiers#3)]  
  
 In the preceding example, if you attempt to instantiate the abstract class by using a statement like this:  
  
```  
BaseClass bc = new BaseClass();   // Error  
```  
  
 you will get an error saying that the compiler cannot create an instance of the abstract class 'BaseClass'.  
  
## C# Language Specification  
 [!INCLUDE[CSharplangspec](../vs140/includes/Csharplangspec_md.md)]  
  
## See Also  
 [C# Programmer's Reference](../vs140/C#-Reference.md)   
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [Modifiers](../vs140/Modifiers--C#-Reference-.md)   
 [virtual](../vs140/virtual--C#-Reference-.md)   
 [override](../vs140/override--C#-Reference-.md)   
 [C# Keywords](../Topic/C%23%20Keywords.md)