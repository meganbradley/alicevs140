---
title: "Static Constructors (C# Programming Guide)"
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
ms.assetid: 151ec95e-3c4d-4ed7-885d-95b7a3be2e7d
caps.latest.revision: 25
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Static Constructors (C# Programming Guide)
A static constructor is used to initialize any [static](../vs140/static--C#-Reference-.md) data, or to perform a particular action that needs to be performed once only. It is called automatically before the first instance is created or any static members are referenced.  
  
 [!CODE [csProgGuideObjects#14](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideObjects#14)]  
  
 Static constructors have the following properties:  
  
-   A static constructor does not take access modifiers or have parameters.  
  
-   A static constructor is called automatically to initialize the [class](../vs140/class--C#-Reference-.md) before the first instance is created or any static members are referenced.  
  
-   A static constructor cannot be called directly.  
  
-   The user has no control on when the static constructor is executed in the program.  
  
-   A typical use of static constructors is when the class is using a log file and the constructor is used to write entries to this file.  
  
-   Static constructors are also useful when creating wrapper classes for unmanaged code, when the constructor can call the `LoadLibrary` method.  
  
-   If a static constructor throws an exception, the runtime will not invoke it a second time, and the type will remain uninitialized for the lifetime of the application domain in which your program is running.  
  
## Example  
 In this example, class `Bus` has a static constructor. When the first instance of `Bus` is created (`bus1`), the static constructor is invoked to initialize the class. The sample output verifies that the static constructor runs only one time, even though two instances of `Bus` are created, and that it runs before the instance constructor runs.  
  
 [!CODE [csProgGuideObjects#15](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideObjects#15)]  
  
## See Also  
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [Objects, Classes, and Structs (Visual C#)](../Topic/Classes%20and%20Structs%20\(C%23%20Programming%20Guide\).md)   
 [Constructors](../vs140/Constructors--C#-Programming-Guide-.md)   
 [Static Classes and Static Class Members (C# Programming Guide)](../Topic/Static%20Classes%20and%20Static%20Class%20Members%20\(C%23%20Programming%20Guide\).md)   
 [Destructors (C# Programmer's Reference)](../Topic/Destructors%20\(C%23%20Programming%20Guide\).md)