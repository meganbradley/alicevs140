---
title: "How to: Write a Copy Constructor (C# Programming Guide)"
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
ms.assetid: fba899b5-fc41-428e-a745-3ebdbf37990a
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Write a Copy Constructor (C# Programming Guide)
C# doesn't provide a copy constructor for objects, but you can write one yourself.  
  
## Example  
 In the following example, the `Person`[class](../vs140/class--C#-Reference-.md) defines a copy constructor that takes, as its argument, an instance of `Person`. The values of the properties of the argument are assigned to the properties of the new instance of `Person`. The code contains an alternative copy constructor that sends the `Name` and `Age` properties of the instance that you want to copy to the instance constructor of the class.  
  
 [!CODE [csProgGuideObjects#16](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideObjects#16)]  
  
## See Also  
 <xref:System.ICloneable?qualifyHint=False>   
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [Objects, Classes, and Structs (Visual C#)](../Topic/Classes%20and%20Structs%20\(C%23%20Programming%20Guide\).md)   
 [Constructors](../vs140/Constructors--C#-Programming-Guide-.md)   
 [Destructors (C# Programmer's Reference)](../Topic/Destructors%20\(C%23%20Programming%20Guide\).md)