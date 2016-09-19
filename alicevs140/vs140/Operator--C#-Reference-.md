---
title: "operator (C# Reference)"
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
ms.assetid: 59218cce-e90e-42f6-a6bb-30300981b86a
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# operator (C# Reference)
Use the `operator` keyword to overload a built-in operator or to provide a user-defined conversion in a class or struct declaration.  
  
## Example  
 The following is a very simplified class for fractional numbers. It overloads the + and * operators to perform fractional addition and multiplication, and also provides a conversion operator that converts a Fraction type to a double type.  
  
 [!CODE [csrefKeywordsConversion#6](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsConversion#6)]  
  
## C# Language Specification  
 [!INCLUDE[CSharplangspec](../vs140/includes/Csharplangspec_md.md)]  
  
## See Also  
 [C# Reference](../vs140/C#-Reference.md)   
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [C# Keywords](../Topic/C%23%20Keywords.md)   
 [implicit](../Topic/implicit%20\(C%23%20Reference\).md)   
 [explicit](../Topic/explicit%20\(C%23%20Reference\).md)   
 [How to: Implement User-Defined Conversions Between Structs (C#)](../vs140/How-to--Implement-User-Defined-Conversions-Between-Structs--C#-Programming-Guide-.md)