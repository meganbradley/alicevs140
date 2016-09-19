---
title: "float (C# Reference)"
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
ms.assetid: 1e77db7b-dedb-48b7-8dd1-b055e96a9258
caps.latest.revision: 26
translation.priority.ht: 
  - de-de
  - ja-jp
---
# float (C# Reference)
The `float` keyword signifies a simple type that stores 32-bit floating-point values. The following table shows the precision and approximate range for the `float` type.  
  
|Type|Approximate range|Precision|.NET Framework type|  
|----------|-----------------------|---------------|-------------------------|  
|`float`|-3.4 × 10<sup>38</sup>to +3.4 × 10<sup>38</sup>|7 digits|<xref:System.Single?qualifyHint=True>|  
  
## Literals  
 By default, a real numeric literal on the right side of the assignment operator is treated as [double](../vs140/double--C#-Reference-.md). Therefore, to initialize a float variable, use the suffix `f` or `F`, as in the following example:  
  
```  
  
float x = 3.5F;  
```  
  
 If you do not use the suffix in the previous declaration, you will get a compilation error because you are trying to store a [double](../vs140/double--C#-Reference-.md) value into a `float` variable.  
  
## Conversions  
 You can mix numeric integral types and floating-point types in an expression. In this case, the integral types are converted to floating-point types. The evaluation of the expression is performed according to the following rules:  
  
-   If one of the floating-point types is [double](../vs140/double--C#-Reference-.md), the expression evaluates to [double](../vs140/double--C#-Reference-.md) or [bool](../Topic/bool%20\(C%23%20Reference\).md) in relational or Boolean expressions.  
  
-   If there is no [double](../vs140/double--C#-Reference-.md) type in the expression, the expression evaluates to `float` or [bool](../Topic/bool%20\(C%23%20Reference\).md) in relational or Boolean expressions.  
  
 A floating-point expression can contain the following sets of values:  
  
-   Positive and negative zero  
  
-   Positive and negative infinity  
  
-   Not-a-Number value (NaN)  
  
-   The finite set of nonzero values  
  
 For more information about these values, see IEEE Standard for Binary Floating-Point Arithmetic, available on the [IEEE](http://go.microsoft.com/fwlink/?LinkId=26269) Web site.  
  
## Example  
 In the following example, an [int](../Topic/int%20\(C%23%20Reference\).md), a [short](../Topic/short%20\(C%23%20Reference\).md), and a `float` are included in a mathematical expression giving a `float` result. (Remember that `float` is an alias for the <xref:System.Single?qualifyHint=True> type.) Notice that there is no [double](../vs140/double--C#-Reference-.md) in the expression.  
  
 [!CODE [csrefKeywordsTypes#13](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsTypes#13)]  
  
## C# Language Specification  
 [!INCLUDE[CSharplangspec](../vs140/includes/Csharplangspec_md.md)]  
  
## See Also  
 <xref:System.Single?qualifyHint=False>   
 [C# Reference](../vs140/C#-Reference.md)   
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [Casting and Type Conversions (C# Programming Guide)](../Topic/Casting%20and%20Type%20Conversions%20\(C%23%20Programming%20Guide\).md)   
 [C# Keywords](../Topic/C%23%20Keywords.md)   
 [Integral Types Table](../vs140/Integral-Types-Table--C#-Reference-.md)   
 [Built-in Types Table (Visual C#)](../Topic/Built-In%20Types%20Table%20\(C%23%20Reference\).md)   
 [Implicit Numeric Conversions Table](../vs140/Implicit-Numeric-Conversions-Table--C#-Reference-.md)   
 [Explicit Numeric Conversions Table (Visual C#)](../Topic/Explicit%20Numeric%20Conversions%20Table%20\(C%23%20Reference\).md)