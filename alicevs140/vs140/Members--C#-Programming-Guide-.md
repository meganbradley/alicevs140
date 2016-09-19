---
title: "Members (C# Programming Guide)"
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
ms.assetid: 4a30a4ab-d690-4936-9124-92ce9448665a
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Members (C# Programming Guide)
Classes and structs have members that represent their data and behavior. A class's members include all the members declared in the class, along with all members (except constructors and destructors) declared in all classes in its inheritance hierarchy. Private members in base classes are inherited but are not accessible from derived classes.  
  
 The following table lists the kinds of members a class or struct may contain:  
  
|Member|Description|  
|------------|-----------------|  
|[Fields (C# Programming Guide)](../vs140/Fields--C#-Programming-Guide-.md)|Fields are variables declared at class scope. A field may be a built-in numeric type or an instance of another class. For example, a calendar class may have a field that contains the current date.|  
|[Constants (C# Programming Guide)](../Topic/Constants%20\(C%23%20Programming%20Guide\).md)|Constants are fields or properties whose value is set at compile time and cannot be changed.|  
|[Properties (C# Programming Guide)](../vs140/Properties--C#-Programming-Guide-.md)|Properties are methods on a class that are accessed as if they were fields on that class. A property can provide protection for a class field to keep it from being changed without the knowledge of the object.|  
|[Methods (C# Programming Guide)](../Topic/Methods%20\(C%23%20Programming%20Guide\).md)|Methods define the actions that a class can perform. Methods can take parameters that provide input data, and can return output data through parameters. Methods can also return a value directly, without using a parameter.|  
|[Events (C# Programming Guide)](../Topic/Events%20\(C%23%20Programming%20Guide\).md)|Events provide notifications about occurrences, such as button clicks or the successful completion of a method, to other objects. Events are defined and triggered by using delegates.|  
|[Operators (C# Programming Guide)](../Topic/Operators%20\(C%23%20Programming%20Guide\).md)|Overloaded operators are considered class members. When you overload an operator, you define it as a public static method in a class. The predefined operators (`+`, `*`, `<`, and so on) are not considered members. For more information, see [Overloadable Operators (Visual C#)](../Topic/Overloadable%20Operators%20\(C%23%20Programming%20Guide\).md).|  
|[Indexers (C# Programming Guide)](../vs140/Indexers--C#-Programming-Guide-.md)|Indexers enable an object to be indexed in a manner similar to arrays.|  
|[Constructors (C# Programming Guide)](../vs140/Constructors--C#-Programming-Guide-.md)|Constructors are methods that are called when the object is first created. They are often used to initialize the data of an object.|  
|[Destructors (C# Programming Guide)](../Topic/Destructors%20\(C%23%20Programming%20Guide\).md)|Destructors are used very rarely in C#. They are methods that are called by the runtime execution engine when the object is about to be removed from memory. They are generally used to make sure that any resources which must be released are handled appropriately.|  
|[Nested Types (C# Programming Guide)](../vs140/Nested-Types--C#-Programming-Guide-.md)|Nested types are types declared within another type. Nested types are often used to describe objects that are used only by the types that contain them.|  
  
## See Also  
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [Classes (C#)](../vs140/Classes--C#-Programming-Guide-.md)   
 [Methods (C# Programming Guide)](../Topic/Methods%20\(C%23%20Programming%20Guide\).md)   
 [Constructors](../vs140/Constructors--C#-Programming-Guide-.md)   
 [Destructors (C# Programmer's Reference)](../Topic/Destructors%20\(C%23%20Programming%20Guide\).md)   
 [Properties (C# Programmer's Reference)](../vs140/Properties--C#-Programming-Guide-.md)   
 [Fields (C# Programming Guide)](../vs140/Fields--C#-Programming-Guide-.md)   
 [Indexers](../vs140/Indexers--C#-Programming-Guide-.md)   
 [Events (C#)](../Topic/Events%20\(C%23%20Programming%20Guide\).md)   
 [Nested Types (C# Programming Guide)](../vs140/Nested-Types--C#-Programming-Guide-.md)   
 [Operators (C# Programming Guide)](../Topic/Operators%20\(C%23%20Programming%20Guide\).md)   
 [Overloadable Operators (C# Programming Guide)](../Topic/Overloadable%20Operators%20\(C%23%20Programming%20Guide\).md)