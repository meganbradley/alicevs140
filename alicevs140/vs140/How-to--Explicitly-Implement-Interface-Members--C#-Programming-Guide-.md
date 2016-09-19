---
title: "How to: Explicitly Implement Interface Members (C# Programming Guide)"
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
ms.assetid: 514cde76-f981-474e-8b40-9493619f899c
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Explicitly Implement Interface Members (C# Programming Guide)
This example declares an [interface](../vs140/interface--C#-Reference-.md), `IDimensions`, and a class, `Box`, which explicitly implements the interface members `getLength` and `getWidth`. The members are accessed through the interface instance `dimensions`.  
  
## Example  
 [!CODE [csProgGuideInheritance#8](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideInheritance#8)]  
  
## Robust Programming  
  
-   Notice that the following lines, in the `Main` method, are commented out because they would produce compilation errors. An interface member that is explicitly implemented cannot be accessed from a [class](../vs140/class--C#-Reference-.md) instance:  
  
     [!CODE [csProgGuideInheritance#45](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideInheritance#45)]  
  
-   Notice also that the following lines, in the `Main` method, successfully print out the dimensions of the box because the methods are being called from an instance of the interface:  
  
     [!CODE [csProgGuideInheritance#46](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideInheritance#46)]  
  
## See Also  
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [Objects, Classes and Structs (C# Programming Guide)](../Topic/Classes%20and%20Structs%20\(C%23%20Programming%20Guide\).md)   
 [Interfaces (Visual C#)](../Topic/Interfaces%20\(C%23%20Programming%20Guide\).md)   
 [How to: Explicitly Implement Interface Members with Inheritance (C#)](../vs140/How-to--Explicitly-Implement-Members-of-Two-Interfaces--C#-Programming-Guide-.md)