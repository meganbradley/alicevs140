---
title: "Structure of a Visual Basic Program"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - VB
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-visual-basic
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ad0c6531-d762-4c77-a700-de16b07b6119
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Structure of a Visual Basic Program
A [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] program is built up from standard building blocks. A *solution* comprises one or more projects. A *project* in turn can contain one or more assemblies. Each *assembly* is compiled from one or more source files. A *source file* provides the definition and implementation of classes, structures, modules, and interfaces, which ultimately contain all your code.  
  
 For more information about these building blocks of a [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] program, see [Introduction to Solutions, Projects, and Items](../vs140/Solutions-and-Projects-in-Visual-Studio.md) and [Assemblies and the Global Assembly Cache (C# and Visual Basic)](../vs140/Assemblies-and-the-Global-Assembly-Cache--C#-and-Visual-Basic-.md).  
  
## File-Level Programming Elements  
 When you start a project or file and open the code editor, you see some code already in place and in the correct order. Any code that you write should follow the following sequence:  
  
1.  `Option` statements  
  
2.  `Imports` statements  
  
3.  `Namespace` statements and namespace-level elements  
  
 If you enter statements in a different order, compilation errors can result.  
  
 A program can also contain conditional compilation statements. You can intersperse these in the source file among the statements of the preceding sequence.  
  
### Option Statements  
 `Option` statements establish ground rules for subsequent code, helping prevent syntax and logic errors. The [Option Explicit Statement](../vs140/Option-Explicit-Statement--Visual-Basic-.md) ensures that all variables are declared and spelled correctly, which reduces debugging time. The [Option Strict Statement](../vs140/Option-Strict-Statement.md) helps to minimize logic errors and data loss that can occur when you work between variables of different data types. The [Option Compare Statement](../Topic/Option%20Compare%20Statement.md) specifies the way strings are compared to each other, based on either their `Binary` or `Text` values.  
  
### Imports Statements  
 You can include an [Imports Statement (.NET Namespace and Type)](../Topic/Imports%20Statement%20\(.NET%20Namespace%20and%20Type\).md) to import names defined outside your project. An `Imports` statement allows your code to refer to classes and other types defined within the imported namespace, without having to qualify them. You can use as many `Imports` statements as appropriate. For more information, see [References and the Imports Statement](../vs140/References-and-the-Imports-Statement--Visual-Basic-.md).  
  
### Namespace Statements  
 Namespaces help you organize and classify your programming elements for ease of grouping and accessing. You use the [Namespace Statement](../Topic/Namespace%20Statement.md) to classify the following statements within a particular namespace. For more information, see [Namespaces in Visual Basic](../Topic/Namespaces%20in%20Visual%20Basic.md).  
  
### Conditional Compilation Statements  
 Conditional compilation statements can appear almost anywhere in your source file. They cause parts of your code to be included or excluded at compile time depending on certain conditions. You can also use them for debugging your application, because conditional code runs in debugging mode only. For more information, see [Conditional Compilation](../vs140/Conditional-Compilation-in-Visual-Basic.md).  
  
## Namespace-Level Programming Elements  
 Classes, structures, and modules contain all the code in your source file. They are *namespace-level* elements, which can appear within a namespace or at the source file level. They hold the declarations of all other programming elements. Interfaces, which define element signatures but provide no implementation, also appear at module level. For more information on the module-level elements, see the following:  
  
-   [Class Statement](../Topic/Class%20Statement%20\(Visual%20Basic\).md)  
  
-   [Structure Statement](../Topic/Structure%20Statement.md)  
  
-   [Module Statement](../Topic/Module%20Statement.md)  
  
-   [Interface Statement (Visual Basic)](../vs140/Interface-Statement--Visual-Basic-.md)  
  
 Data elements at namespace level are enumerations and delegates.  
  
## Module-Level Programming Elements  
 Procedures, operators, properties, and events are the only programming elements that can hold executable code (statements that perform actions at run time). They are the *module-level* elements of your program. For more information on the procedure-level elements, see the following:  
  
-   [Function Statement (Visual Basic)](../Topic/Function%20Statement%20\(Visual%20Basic\).md)  
  
-   [Sub Statement](../Topic/Sub%20Statement%20\(Visual%20Basic\).md)  
  
-   [Declare Statement](../Topic/Declare%20Statement.md)  
  
-   [Operator Statement](../vs140/Operator-Statement.md)  
  
-   [Property Statement](../vs140/Property-Statement.md)  
  
-   [Event Statement](../vs140/Event-Statement.md)  
  
 Data elements at module level are variables, constants, enumerations, and delegates.  
  
## Procedure-Level Programming Elements  
 Most of the contents of *procedure-level* elements are executable statements, which constitute the run-time code of your program. All executable code must be in some procedure (`Function`, `Sub`, `Operator`, `Get`, `Set`, `AddHandler`, `RemoveHandler`, `RaiseEvent`). For more information, see [Statements in Visual Basic](../vs140/Statements-in-Visual-Basic.md).  
  
 Data elements at procedure level are limited to local variables and constants.  
  
## The Main Procedure  
 The `Main` procedure is the first code to run when your application has been loaded. `Main` serves as the starting point and overall control for your application. There are four varieties of `Main`:  
  
-   `Sub Main()`  
  
-   `Sub Main(ByVal cmdArgs() As String)`  
  
-   `Function Main() As Integer`  
  
-   `Function Main(ByVal cmdArgs() As String) As Integer`  
  
 The most common variety of this procedure is `Sub Main()`. For more information, see [Main Procedure in Visual Basic](../Topic/Main%20Procedure%20in%20Visual%20Basic.md).  
  
## See Also  
 [NIB: Visual Basic Version of Hello, World](assetId:///9d030b60-e148-4366-a462-69532f02294c)   
 [Main Procedure in Visual Basic](../Topic/Main%20Procedure%20in%20Visual%20Basic.md)   
 [Visual Basic Naming Conventions](../Topic/Visual%20Basic%20Naming%20Conventions.md)   
 [Visual Basic Limitations](../vs140/Visual-Basic-Limitations.md)