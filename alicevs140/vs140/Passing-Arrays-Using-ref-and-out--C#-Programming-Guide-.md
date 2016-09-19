---
title: "Passing Arrays Using ref and out (C# Programming Guide)"
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
ms.assetid: 6a2b261e-a1cc-49a6-b4f0-6cacae385a1e
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Passing Arrays Using ref and out (C# Programming Guide)
Like all [out](../vs140/out--C#-Reference-.md) parameters, an `out` parameter of an array type must be assigned before it is used; that is, it must be assigned by the callee. For example:  
  
 [!CODE [csProgGuideArrays#39](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#39)]  
  
 Like all [ref](../vs140/ref--C#-Reference-.md) parameters, a `ref` parameter of an array type must be definitely assigned by the caller. Therefore, there is no need to be definitely assigned by the callee. A `ref` parameter of an array type may be altered as a result of the call. For example, the array can be assigned the [null](../vs140/null--C#-Reference-.md) value or can be initialized to a different array. For example:  
  
 [!CODE [csProgGuideArrays#40](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#40)]  
  
 The following two examples demonstrate the difference between `out` and `ref` when used in passing arrays to methods.  
  
## Example  
 In this example, the array `theArray` is declared in the caller (the `Main` method), and initialized in the `FillArray` method. Then, the array elements are returned to the caller and displayed.  
  
 [!CODE [csProgGuideArrays#37](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#37)]  
  
## Example  
 In this example, the array `theArray` is initialized in the caller (the `Main` method), and passed to the `FillArray` method by using the `ref` parameter. Some of the array elements are updated in the `FillArray` method. Then, the array elements are returned to the caller and displayed.  
  
 [!CODE [csProgGuideArrays#38](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideArrays#38)]  
  
## See Also  
 [C# Programming Guide](../vs140/ref--C#-Reference-.md)   
 [Arrays (Visual C#)](../vs140/out-parameter-modifier--C#-Reference-.md)   
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [Arrays (Visual C#)](../Topic/Arrays%20\(C%23%20Programming%20Guide\).md)   
 [Single-Dimensional Arrays](../vs140/Single-Dimensional-Arrays--C#-Programming-Guide-.md)   
 [Multidimensional Arrays](../vs140/Multidimensional-Arrays--C#-Programming-Guide-.md)   
 [Jagged Arrays](../Topic/Jagged%20Arrays%20\(C%23%20Programming%20Guide\).md)