---
title: "double (C# Reference)"
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
ms.assetid: 0980e11b-6004-4102-abcf-cfc280fc6991
caps.latest.revision: 28
translation.priority.ht: 
  - de-de
  - ja-jp
---
# double (C# Reference)
The `double` keyword signifies a simple type that stores 64-bit floating-point values. The following table shows the precision and approximate range for the `double` type.  
  
|Type|Approximate range|Precision|.NET Framework type|  
|----------|-----------------------|---------------|-------------------------|  
|`double`|±5.0 × 10<sup>−324</sup> to ±1.7 × 10<sup>308</sup>|15-16 digits|<xref:System.Double?qualifyHint=True>|  
  
## Literals  
 By default, a real numeric literal on the right side of the assignment operator is treated as `double`. However, if you want an integer number to be treated as `double`, use the suffix d or D, for example:  
  
```  
  
double x = 3D;  
```  
  
## Conversions  
 You can mix numeric integral types and floating-point types in an expression. In this case, the integral types are converted to floating-point types. The evaluation of the expression is performed according to the following rules:  
  
-   If one of the floating-point types is `double`, the expression evaluates to `double`, or [bool](../Topic/bool%20\(C%23%20Reference\).md) in relational or Boolean expressions.  
  
-   If there is no `double` type in the expression, it evaluates to [float](../vs140/float--C#-Reference-.md), or [bool](../Topic/bool%20\(C%23%20Reference\).md) in relational or Boolean expressions.  
  
 A floating-point expression can contain the following sets of values:  
  
-   Positive and negative zero.  
  
-   Positive and negative infinity.  
  
-   Not-a-Number value (NaN).  
  
-   The finite set of nonzero values.  
  
 For more information about these values, see IEEE Standard for Binary Floating-Point Arithmetic, available on the [IEEE](http://go.microsoft.com/fwlink/?LinkId=26269) Web site.  
  
## Example  
 In the following example, an [int](../Topic/int%20\(C%23%20Reference\).md), a [short](../Topic/short%20\(C%23%20Reference\).md), a [float](../vs140/float--C#-Reference-.md), and a `double` are added together giving a `double` result.  
  
 [!CODE [csrefKeywordsTypes#9](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsTypes#9)]  
  
## C# Language Specification  
 [!INCLUDE[CSharplangspec](../vs140/includes/Csharplangspec_md.md)]  
  
## See Also  
 [C# Reference](../vs140/C#-Reference.md)   
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [C# Keywords](../Topic/C%23%20Keywords.md)   
 [Default Values Table](../vs140/Default-Values-Table--C#-Reference-.md)   
 [Built-in Types Table (Visual C#)](../Topic/Built-In%20Types%20Table%20\(C%23%20Reference\).md)   
 [Floating-Point Types Table](../vs140/Floating-Point-Types-Table--C#-Reference-.md)   
 [Implicit Numeric Conversions Table](../vs140/Implicit-Numeric-Conversions-Table--C#-Reference-.md)   
 [Explicit Numeric Conversions Table (Visual C#)](../Topic/Explicit%20Numeric%20Conversions%20Table%20\(C%23%20Reference\).md)