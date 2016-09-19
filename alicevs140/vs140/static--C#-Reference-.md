---
title: "static (C# Reference)"
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
ms.assetid: 5509e215-2183-4da3-bab4-6b7e607a4fdf
caps.latest.revision: 28
translation.priority.ht: 
  - de-de
  - ja-jp
---
# static (C# Reference)
Use the `static` modifier to declare a static member, which belongs to the type itself rather than to a specific object. The `static` modifier can be used with classes, fields, methods, properties, operators, events, and constructors, but it cannot be used with indexers, destructors, or types other than classes. For more information, see [Static Classes and Static Class Members](../Topic/Static%20Classes%20and%20Static%20Class%20Members%20\(C%23%20Programming%20Guide\).md).  
  
## Example  
 The following class is declared as `static` and contains only `static` methods:  
  
 [!CODE [csrefKeywordsModifiers#18](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsModifiers#18)]  
  
 A constant or type declaration is implicitly a static member.  
  
 A static member cannot be referenced through an instance. Instead, it is referenced through the type name. For example, consider the following class:  
  
 [!CODE [csrefKeywordsModifiers#19](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsModifiers#19)]  
  
 To refer to the static member `x`, use the fully qualified name, `MyBaseC.MyStruct.x`, unless the member is accessible from the same scope:  
  
```c#  
Console.WriteLine(MyBaseC.MyStruct.x);  
```  
  
 While an instance of a class contains a separate copy of all instance fields of the class, there is only one copy of each static field.  
  
 It is not possible to use [this](../vs140/this--C#-Reference-.md) to reference static methods or property accessors.  
  
 If the `static` keyword is applied to a class, all the members of the class must be static.  
  
 Classes and static classes may have static constructors. Static constructors are called at some point between when the program starts and the class is instantiated.  
  
> [!NOTE]
>  The `static` keyword has more limited uses than in C++. To compare with the C++ keyword, see [Static](../vs140/Static--C---.md).  
  
 To demonstrate static members, consider a class that represents a company employee. Assume that the class contains a method to count employees and a field to store the number of employees. Both the method and the field do not belong to any instance employee. Instead they belong to the company class. Therefore, they should be declared as static members of the class.  
  
## Example  
 This example reads the name and ID of a new employee, increments the employee counter by one, and displays the information for the new employee and the new number of employees. For simplicity, this program reads the current number of employees from the keyboard. In a real application, this information should be read from a file.  
  
 [!CODE [csrefKeywordsModifiers#20](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsModifiers#20)]  
  
## Example  
 This example shows that although you can initialize a static field by using another static field not yet declared, the results will be undefined until you explicitly assign a value to the static field.  
  
 [!CODE [csrefKeywordsModifiers#21](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsModifiers#21)]  
  
## C# Language Specification  
 [!INCLUDE[CSharplangspec](../vs140/includes/Csharplangspec_md.md)]  
  
## See Also  
 [C# Reference](../vs140/C#-Reference.md)   
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [C# Keywords](../Topic/C%23%20Keywords.md)   
 [Modifiers](../vs140/Modifiers--C#-Reference-.md)   
 [Static Classes and Static Class Members](../Topic/Static%20Classes%20and%20Static%20Class%20Members%20\(C%23%20Programming%20Guide\).md)