---
title: "Interface Properties (C# Programming Guide)"
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
ms.assetid: 6503e9ed-33d7-44ec-b4c1-cc16c084b795
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Interface Properties (C# Programming Guide)
Properties can be declared on an [interface (C# Reference)](../vs140/interface--C#-Reference-.md). The following is an example of an interface indexer accessor:  
  
 [!CODE [csProgGuideProperties#14](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideProperties#14)]  
  
 The accessor of an interface property does not have a body. Thus, the purpose of the accessors is to indicate whether the property is read-write, read-only, or write-only.  
  
## Example  
 In this example, the interface `IEmployee` has a read-write property, `Name`, and a read-only property, `Counter`. The class `Employee` implements the `IEmployee` interface and uses these two properties. The program reads the name of a new employee and the current number of employees and displays the employee name and the computed employee number.  
  
 You could use the fully qualified name of the property, which references the interface in which the member is declared. For example:  
  
 [!CODE [csProgGuideProperties#16](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideProperties#16)]  
  
 This is called [Explicit Interface Implementation (C# Programmers Reference)](../vs140/Explicit-Interface-Implementation--C#-Programming-Guide-.md). For example, if the class `Employee` is implementing two interfaces `ICitizen` and `IEmployee` and both interfaces have the `Name` property, the explicit interface member implementation will be necessary. That is, the following property declaration:  
  
 [!CODE [csProgGuideProperties#16](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideProperties#16)]  
  
 implements the `Name` property on the `IEmployee` interface, while the following declaration:  
  
 [!CODE [csProgGuideProperties#17](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideProperties#17)]  
  
 implements the `Name` property on the `ICitizen` interface.  
  
 [!CODE [csProgGuideProperties#15](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideProperties#15)]  
  
  **`210 Hazem Abolrous`**    
## Sample Output  
 `Enter number of employees: 210`  
  
 `Enter the name of the new employee: Hazem Abolrous`  
  
 `The employee information:`  
  
 `Employee number: 211`  
  
 `Employee name: Hazem Abolrous`  
  
## See Also  
 [C# Programming](../vs140/C#-Programming-Guide.md)   
 [Properties (C# Programmer's Reference)](../vs140/Properties--C#-Programming-Guide-.md)   
 [Using Properties (C# Programmer's Reference)](../vs140/Using-Properties--C#-Programming-Guide-.md)   
 [Comparison Between Properties and Indexers](../vs140/Comparison-Between-Properties-and-Indexers--C#-Programming-Guide-.md)   
 [Indexers](../vs140/Indexers--C#-Programming-Guide-.md)   
 [Interfaces (C# Programming Guide)](../Topic/Interfaces%20\(C%23%20Programming%20Guide\).md)