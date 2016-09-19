---
title: "Pointer Conversions (C# Programming Guide)"
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
ms.assetid: f0e87502-477a-4ede-a31f-7a3e262e46fb
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Pointer Conversions (C# Programming Guide)
The following table shows the predefined implicit pointer conversions. Implicit conversions might occur in many situations, including method invoking and assignment statements.  
  
## Implicit pointer conversions  
  
|From|To|  
|----------|--------|  
|Any pointer type|void*|  
|null|Any pointer type|  
  
 Explicit pointer conversion is used to perform conversions, for which there is no implicit conversion, by using a cast expression. The following table shows these conversions.  
  
## Explicit pointer conversions  
  
|From|To|  
|----------|--------|  
|Any pointer type|Any other pointer type|  
|sbyte, byte, short, ushort, int, uint, long, or ulong|Any pointer type|  
|Any pointer type|sbyte, byte, short, ushort, int, uint, long, or ulong|  
  
## Example  
 In the following example, a pointer to `int` is converted to a pointer to `byte`. Notice that the pointer points to the lowest addressed byte of the variable. When you successively increment the result, up to the size of `int` (4 bytes), you can display the remaining bytes of the variable.  
  
 [!CODE [csProgGuidePointers#3](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuidePointers#3)]  
  
 [!CODE [csProgGuidePointers#4](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuidePointers#4)]  
  
## See Also  
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [Pointer Expressions](../vs140/Pointer-Expressions--C#-Programming-Guide-.md)   
 [Pointer types](../vs140/Pointer-types--C#-Programming-Guide-.md)   
 [Types](../vs140/Types--C#-Reference-.md)   
 [unsafe](../vs140/unsafe--C#-Reference-.md)   
 [fixed Statement](../vs140/fixed-Statement--C#-Reference-.md)   
 [stackalloc](../vs140/stackalloc--C#-Reference-.md)