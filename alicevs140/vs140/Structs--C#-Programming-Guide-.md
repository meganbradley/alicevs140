---
title: "Structs (C# Programming Guide)"
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
ms.assetid: b7cf4ff2-0eb7-4e5c-93d5-b2196b4f5d89
caps.latest.revision: 33
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Structs (C# Programming Guide)
Structs are defined by using the [struct](../vs140/struct--C#-Reference-.md) keyword, for example:  
  
 [!CODE [csProgGuideObjects#39](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideObjects#39)]  
  
 Structs share most of the same syntax as classes, although structs are more limited than classes:  
  
-   Within a struct declaration, fields cannot be initialized unless they are declared as const or static.  
  
-   A struct cannot declare a default constructor (a constructor without parameters) or a destructor.  
  
-   Structs are copied on assignment. When a struct is assigned to a new variable, all the data is copied, and any modification to the new copy does not change the data for the original copy. This is important to remember when working with collections of value types such as Dictionary<string, myStruct>.  
  
-   Structs are value types and classes are reference types.  
  
-   Unlike classes, structs can be instantiated without using a `new` operator.  
  
-   Structs can declare constructors that have parameters.  
  
-   A struct cannot inherit from another struct or class, and it cannot be the base of a class. All structs inherit directly from `System.ValueType`, which inherits from `System.Object`.  
  
-   A struct can implement interfaces.  
  
-   A struct can be used as a nullable type and can be assigned a null value.  
  
## Related Sections  
 For more information:  
  
-   [Using structs](../vs140/Using-Structs--C#-Programming-Guide-.md)  
  
-   [Constructors (C# Programming Guide)](../vs140/Constructors--C#-Programming-Guide-.md)  
  
-   [Nullable Types (C# Programming Guide)](../Topic/Nullable%20Types%20\(C%23%20Programming%20Guide\).md)  
  
-   [How to: Know the Difference Between Passing a Struct and Passing a Class Reference to a Method](../vs140/How-to--Know-the-Difference-Between-Passing-a-Struct-and-Passing-a-Class-Reference-to-a-Method--C#-Programming-Guide-.md)  
  
-   [How to: Implement User-Defined Conversions Between Structs](../vs140/How-to--Implement-User-Defined-Conversions-Between-Structs--C#-Programming-Guide-.md)  
  
-   [More About Variables](http://go.microsoft.com/fwlink/?LinkId=221230) in [Beginning Visual C# 2010](http://go.microsoft.com/fwlink/?LinkId=221214)  
  
## See Also  
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [Objects, Classes and Structs (C# Programming Guide)](../Topic/Classes%20and%20Structs%20\(C%23%20Programming%20Guide\).md)   
 [Classes (C#)](../vs140/Classes--C#-Programming-Guide-.md)