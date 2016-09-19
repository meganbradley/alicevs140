---
title: "Single-Dimensional Arrays (C# Programming Guide)"
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
ms.assetid: 2cec1196-1de0-49d2-baf2-c607c33310e8
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Single-Dimensional Arrays (C# Programming Guide)
You can declare a single-dimensional array of five integers as shown in the following example:  
  
 [!CODE [csProgGuideArrays#4](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#4)]  
  
 This array contains the elements from `array[0]` to `array[4]`. The [new](../vs140/new--C#-Reference-.md) operator is used to create the array and initialize the array elements to their default values. In this example, all the array elements are initialized to zero.  
  
 An array that stores string elements can be declared in the same way. For example:  
  
 [!CODE [csProgGuideArrays#5](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#5)]  
  
## Array Initialization  
 It is possible to initialize an array upon declaration, in which case, the rank specifier is not needed because it is already supplied by the number of elements in the initialization list. For example:  
  
 [!CODE [csProgGuideArrays#6](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#6)]  
  
 A string array can be initialized in the same way. The following is a declaration of a string array where each array element is initialized by a name of a day:  
  
 [!CODE [csProgGuideArrays#7](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#7)]  
  
 When you initialize an array upon declaration, you can use the following shortcuts:  
  
 [!CODE [csProgGuideArrays#8](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#8)]  
  
 It is possible to declare an array variable without initialization, but you must use the `new` operator when you assign an array to this variable. For example:  
  
 [!CODE [csProgGuideArrays#9](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#9)]  
  
 C# 3.0 introduces implicitly typed arrays. For more information, see [Implicitly Typed Arrays (C# Programming Guide)](../vs140/Implicitly-Typed-Arrays--C#-Programming-Guide-.md).  
  
## Value Type and Reference Type Arrays  
 Consider the following array declaration:  
  
 [!CODE [csProgGuideArrays#10](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#10)]  
  
 The result of this statement depends on whether `SomeType` is a value type or a reference type. If it is a value type, the statement creates an array of 10 elements, each of which has the type `SomeType`. If `SomeType` is a reference type, the statement creates an array of 10 elements, each of which is initialized to a null reference.  
  
 For more information about value types and reference types, see [Types](../vs140/Types--C#-Reference-.md).  
  
## See Also  
 <xref:System.Array?qualifyHint=False>   
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [Arrays (C# Programming Guide)](../Topic/Arrays%20\(C%23%20Programming%20Guide\).md)   
 [Multidimensional Arrays](../vs140/Multidimensional-Arrays--C#-Programming-Guide-.md)   
 [Jagged Arrays](../Topic/Jagged%20Arrays%20\(C%23%20Programming%20Guide\).md)