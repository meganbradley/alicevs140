---
title: "partial (Method) (C# Reference)"
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
ms.assetid: 43f40242-17e0-4452-8573-090503ad3137
caps.latest.revision: 28
translation.priority.ht: 
  - de-de
  - ja-jp
---
# partial (Method) (C# Reference)
A partial method has its signature defined in one part of a partial type, and its implementation defined in another part of the type. Partial methods enable class designers to provide method hooks, similar to event handlers, that developers may decide to implement or not. If the developer does not supply an implementation, the compiler removes the signature at compile time. The following conditions apply to partial methods:  
  
-   Signatures in both parts of the partial type must match.  
  
-   The method must return void.  
  
-   No access modifiers are allowed. Partial methods are implicitly private.  
  
 The following example shows a partial method defined in two parts of a partial class:  
  
 [!CODE [csrefKeywordsContextual#9](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsContextual#9)]  
  
 For more information, see [Partial Classes and Methods (C# Programming Guide)](../vs140/Partial-Classes-and-Methods--C#-Programming-Guide-.md).  
  
## See Also  
 [C# Reference](../vs140/C#-Reference.md)   
 [partial (Type) (C# Reference)](../vs140/partial--Type---C#-Reference-.md)