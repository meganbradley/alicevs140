---
title: "Generic Delegates (C# Programming Guide)"
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
ms.assetid: bdea509c-44c1-4309-aaa9-15c7aee009df
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Generic Delegates (C# Programming Guide)
A [delegate](../vs140/delegate--C#-Reference-.md) can define its own type parameters. Code that references the generic delegate can specify the type argument to create a closed constructed type, just like when instantiating a generic class or calling a generic method, as shown in the following example:  
  
 [!CODE [csProgGuideGenerics#36](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideGenerics#36)]  
  
 C# version 2.0 has a new feature called method group conversion, which applies to concrete as well as generic delegate types, and enables you to write the previous line with this simplified syntax:  
  
 [!CODE [csProgGuideGenerics#37](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideGenerics#37)]  
  
 Delegates defined within a generic class can use the generic class type parameters in the same way that class methods do.  
  
 [!CODE [csProgGuideGenerics#38](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideGenerics#38)]  
  
 Code that references the delegate must specify the type argument of the containing class, as follows:  
  
 [!CODE [csProgGuideGenerics#39](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideGenerics#39)]  
  
 Generic delegates are especially useful in defining events based on the typical design pattern because the sender argument can be strongly typed and no longer has to be cast to and from <xref:System.Object?qualifyHint=False>.  
  
 [!CODE [csProgGuideGenerics#40](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideGenerics#40)]  
  
## See Also  
 <xref:System.Collections.Generic?qualifyHint=False>   
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [Generics (C#)](../Topic/Introduction%20to%20Generics%20\(C%23%20Programming%20Guide\).md)   
 [Generic Methods (C#)](../Topic/Generic%20Methods%20\(C%23%20Programming%20Guide\).md)   
 [Generic Classes (C#)](../Topic/Generic%20Classes%20\(C%23%20Programming%20Guide\).md)   
 [Generic Interfaces (C#)](../vs140/Generic-Interfaces--C#-Programming-Guide-.md)   
 [Delegates (Visual C#)](../Topic/Delegates%20\(C%23%20Programming%20Guide\).md)   
 [Generics in the .NET Framework](assetId:///2994d786-c5c7-4666-ab23-4c83129fe39c)