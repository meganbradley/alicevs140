---
title: "partial (Type) (C# Reference)"
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
ms.assetid: 27320743-a22e-4c7b-b0b3-53afe3607334
caps.latest.revision: 26
translation.priority.ht: 
  - de-de
  - ja-jp
---
# partial (Type) (C# Reference)
Partial type definitions allow for the definition of a class, struct, or interface to be split into multiple files.  
  
 In File1.cs:  
  
 [!CODE [csrefKeywordsContextual#3](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsContextual#3)]  
  
 In File2.cs the declaration:  
  
 [!CODE [csrefKeywordsContextual#4](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsContextual#4)]  
  
## Remarks  
 Splitting a class, struct or interface type over several files can be useful when you are working with large projects, or with automatically generated code such as that provided by the [Windows Forms Designer](assetId:///3c3d61f8-f36c-4d41-b9c3-398376fabb15). A partial type may contain a [partial method](../vs140/partial--Method---C#-Reference-.md). For more information, see [Partial Classes and Methods](../vs140/Partial-Classes-and-Methods--C#-Programming-Guide-.md).  
  
## C# Language Specification  
 [!INCLUDE[CSharplangspec](../vs140/includes/Csharplangspec_md.md)]  
  
## See Also  
 [C# Reference](../vs140/C#-Reference.md)   
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [Modifiers](../vs140/Modifiers--C#-Reference-.md)   
 [Generics (C#)](../Topic/Introduction%20to%20Generics%20\(C%23%20Programming%20Guide\).md)