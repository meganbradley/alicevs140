---
title: "How to: Define Abstract Properties (C# Programming Guide)"
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
ms.assetid: 672a90eb-47b9-4ae0-9914-af53852fddcb
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Define Abstract Properties (C# Programming Guide)
The following example shows how to define [abstract](../vs140/abstract--C#-Reference-.md) properties. An abstract property declaration does not provide an implementation of the property accessors -- it declares that the class supports properties, but leaves the accessor implementation to derived classes. The following example demonstrates how to implement the abstract properties inherited from a base class.  
  
 This sample consists of three files, each of which is compiled individually and its resulting assembly is referenced by the next compilation:  
  
-   abstractshape.cs: the `Shape` class that contains an abstract `Area` property.  
  
-   shapes.cs: The subclasses of the `Shape` class.  
  
-   shapetest.cs: A test program to display the areas of some `Shape`-derived objects.  
  
 To compile the example, use the following command:  
  
 `csc abstractshape.cs shapes.cs shapetest.cs`  
  
 This will create the executable file shapetest.exe.  
  
## Example  
 This file declares the `Shape` class that contains the `Area` property of the type `double`.  
  
 [!CODE [csProgGuideInheritance#1](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideInheritance#1)]  
  
-   Modifiers on the property are placed on the property declaration itself. For example:  
  
    ```  
    public abstract double Area  
    ```  
  
-   When declaring an abstract property (such as `Area` in this example), you simply indicate what property accessors are available, but do not implement them. In this example, only a [get](../vs140/get--C#-Reference-.md) accessor is available, so the property is read-only.  
  
## Example  
 The following code shows three subclasses of `Shape` and how they override the `Area` property to provide their own implementation.  
  
 [!CODE [csProgGuideInheritance#2](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideInheritance#2)]  
  
## Example  
 The following code shows a test program that creates a number of `Shape`-derived objects and prints out their areas.  
  
 [!CODE [csProgGuideInheritance#3](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideInheritance#3)]  
  
## See Also  
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [Objects, Classes and Structs (C# Programming Guide)](../Topic/Classes%20and%20Structs%20\(C%23%20Programming%20Guide\).md)   
 [Abstract and Sealed Classes and Class Members](../vs140/Abstract-and-Sealed-Classes-and-Class-Members--C#-Programming-Guide-.md)   
 [Properties (C# Programming Guide)](../vs140/Properties--C#-Programming-Guide-.md)   
 [How to: Create and Use C# DLLs (C# Programming Guide)](../vs140/How-to--Create-and-Use-Assemblies-Using-the-Command-Line--C#-and-Visual-Basic-.md)