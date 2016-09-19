---
title: "Instance Constructors (C# Programming Guide)"
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
ms.assetid: 24663779-c1e5-4af4-a942-ca554e4c542d
caps.latest.revision: 28
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Instance Constructors (C# Programming Guide)
Instance constructors are used to create and initialize any instance member variables when you use the [new](../vs140/new--C#-Reference-.md) expression to create an object of a [class](../vs140/class--C#-Reference-.md). To initialize a [static](../vs140/static--C#-Reference-.md) class, or static variables in a non-static class, you must define a static constructor. For more information, see [Static Constructors (C# Programming Guide)](../vs140/Static-Constructors--C#-Programming-Guide-.md).  
  
 The following example shows an instance constructor:  
  
 [!CODE [csProgGuideObjects#5](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideObjects#5)]  
  
> [!NOTE]
>  For clarity, this class contains public fields. The use of public fields is not a recommended programming practice because it allows any method anywhere in a program unrestricted and unverified access to an object's inner workings. Data members should generally be private, and should be accessed only through class methods and properties.  
  
 This instance constructor is called whenever an object based on the `CoOrds` class is created. A constructor like this one, which takes no arguments, is called a *default constructor*. However, it is often useful to provide additional constructors. For example, we can add a constructor to the `CoOrds` class that allows us to specify the initial values for the data members:  
  
 [!CODE [csProgGuideObjects#76](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideObjects#76)]  
  
 This allows `CoOrd` objects to be created with default or specific initial values, like this:  
  
 [!CODE [csProgGuideObjects#77](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideObjects#77)]  
  
 If a class does not have a constructor, a default constructor is automatically generated and default values are used to initialize the object fields. For example, an [int](../Topic/int%20\(C%23%20Reference\).md) is initialized to 0. For more information on default values, see [Default Values Table](../vs140/Default-Values-Table--C#-Reference-.md). Therefore, because the `CoOrds` class default constructor initializes all data members to zero, it can be removed altogether without changing how the class works. A complete example using multiple constructors is provided in Example 1 later in this topic, and an example of an automatically generated constructor is provided in Example 2.  
  
 Instance constructors can also be used to call the instance constructors of base classes. The class constructor can invoke the constructor of the base class through the initializer, as follows:  
  
 [!CODE [csProgGuideObjects#78](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideObjects#78)]  
  
 In this example, the `Circle` class passes values representing radius and height to the constructor provided by `Shape` from which `Circle` is derived. A complete example using `Shape` and `Circle` appears in this topic as Example 3.  
  
## Example 1  
 The following example demonstrates a class with two class constructors, one without arguments and one with two arguments.  
  
 [!CODE [csProgGuideObjects#4](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideObjects#4)]  
  
## Example 2  
 In this example, the class `Person` does not have any constructors, in which case, a default constructor is automatically provided and the fields are initialized to their default values.  
  
 [!CODE [csProgGuideObjects#8](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideObjects#8)]  
  
 Notice that the default value of `age` is `0` and the default value of `name` is `null`. For more information on default values, see [Default Values Table](../vs140/Default-Values-Table--C#-Reference-.md).  
  
## Example 3  
 The following example demonstrates using the base class initializer. The `Circle` class is derived from the general class `Shape`, and the `Cylinder` class is derived from the `Circle` class. The constructor on each derived class is using its base class initializer.  
  
 [!CODE [csProgGuideObjects#9](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideObjects#9)]  
  
 For more examples on invoking the base class constructors, see [virtual](../vs140/virtual--C#-Reference-.md), [override](../vs140/override--C#-Reference-.md), and [base](../vs140/base--C#-Reference-.md).  
  
## See Also  
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [Objects, Classes, and Structs (Visual C#)](../Topic/Classes%20and%20Structs%20\(C%23%20Programming%20Guide\).md)   
 [Constructors](../vs140/Constructors--C#-Programming-Guide-.md)   
 [Destructors (C# Programmer's Reference)](../Topic/Destructors%20\(C%23%20Programming%20Guide\).md)   
 [static (C# Reference)](../vs140/static--C#-Reference-.md)