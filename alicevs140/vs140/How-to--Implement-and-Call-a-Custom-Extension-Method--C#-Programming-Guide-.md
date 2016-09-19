---
title: "How to: Implement and Call a Custom Extension Method (C# Programming Guide)"
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
ms.assetid: 7dab2a56-cf8e-4a47-a444-fe610a02772a
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Implement and Call a Custom Extension Method (C# Programming Guide)
This topic shows how to implement your own extension methods for any type in the [.NET Framework Class Library](http://go.microsoft.com/fwlink/?LinkID=217856), or any other .NET type that you want to extend. Client code can use your extension methods by adding a reference to the DLL that contains them, and adding a [using](../Topic/using%20Directive%20\(C%23%20Reference\).md) directive that specifies the namespace in which the extension methods are defined.  
  
### To define and call the extension method  
  
1.  Define a static [class](../Topic/Static%20Classes%20and%20Static%20Class%20Members%20\(C%23%20Programming%20Guide\).md) to contain the extension method.  
  
     The class must be visible to client code. For more information about accessibility rules, see [Access Modifiers (C# Programming Guide)](../Topic/Access%20Modifiers%20\(C%23%20Programming%20Guide\).md).  
  
2.  Implement the extension method as a static method with at least the same visibility as the containing class.  
  
3.  The first parameter of the method specifies the type that the method operates on; it must be preceded with the [this](../vs140/this--C#-Reference-.md) modifier.  
  
4.  In the calling code, add a `using` directive to specify the [namespace](../vs140/namespace--C#-Reference-.md) that contains the extension method class.  
  
5.  Call the methods as if they were instance methods on the type.  
  
     Note that the first parameter is not specified by calling code because it represents the type on which the operator is being applied, and the compiler already knows the type of your object. You only have to provide arguments for parameters 2 through `n`.  
  
## Example  
 The following example implements an extension method named `WordCount` in the `CustomExtensions.StringExtension` class. The method operates on the <xref:System.String?qualifyHint=False> class, which is specified as the first method parameter. The `CustomExtensions` namespace is imported into the application namespace, and the method is called inside the `Main` method.  
  
 [!CODE [csProgGuideExtensionMethods#1](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideExtensionMethods#1)]  
  
## Compiling the Code  
 To run this code, copy and paste it into a Visual C# console application project that has been created in [!INCLUDE[vs_current_short](../vs140/includes/vs_current_short_md.md)]. By default, this project targets version 3.5 of the [!INCLUDE[dnprdnshort](../vs140/includes/dnprdnshort_md.md)], and it has a reference to System.Core.dll and a `using` directive for System.Linq. If one or more of these requirements are missing from the project, you can add them manually. For more information, see [How To: Create a LINQ Project](../vs140/How-to--Create-a-LINQ-Project.md).  
  
## .NET Framework Security  
 Extension methods present no specific security vulnerabilities. They can never be used to impersonate existing methods on a type, because all name collisions are resolved in favor of the instance or static method defined by the type itself. Extension methods cannot access any private data in the extended class.  
  
## See Also  
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [Extension Methods (C# Programming Guide)](../Topic/Extension%20Methods%20\(C%23%20Programming%20Guide\).md)   
 [Language-Integrated Query (LINQ)](../vs140/LINQ--Language-Integrated-Query-.md)   
 [Static Classes and Static Class Members (C# Programming Guide)](../Topic/Static%20Classes%20and%20Static%20Class%20Members%20\(C%23%20Programming%20Guide\).md)   
 [protected (C# Reference)](../vs140/protected--C#-Reference-.md)   
 [internal (C# Reference)](../vs140/internal--C#-Reference-.md)   
 [public (C# Reference)](../vs140/public--C#-Reference-.md)   
 [this (C# Reference)](../vs140/this--C#-Reference-.md)   
 [namespace (C# Reference)](../vs140/namespace--C#-Reference-.md)