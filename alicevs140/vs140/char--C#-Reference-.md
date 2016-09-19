---
title: "char (C# Reference)"
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
ms.assetid: b51cf4fb-124c-4067-af48-afbac122b228
caps.latest.revision: 29
translation.priority.ht: 
  - de-de
  - ja-jp
---
# char (C# Reference)
The `char` keyword is used to declare an instance of the <xref:System.Char?qualifyHint=True> structure that the .NET Framework uses to represent a Unicode character. The value of a `Char` object is a 16-bit numeric (ordinal) value.  
  
 Unicode characters are used to represent most of the written languages throughout the world.  
  
|Type|Range|Size|.NET Framework type|  
|----------|-----------|----------|-------------------------|  
|`char`|U+0000 to U+FFFF|Unicode 16-bit character|<xref:System.Char?qualifyHint=True>|  
  
## Literals  
 Constants of the `char` type can be written as character literals, hexadecimal escape sequence, or Unicode representation. You can also cast the integral character codes. In the following example four `char` variables are initialized with the same character `X`:  
  
 [!CODE [csrefKeywordsTypes#19](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsTypes#19)]  
  
## Conversions  
 A `char` can be implicitly converted to [ushort](../Topic/ushort%20\(C%23%20Reference\).md), [int](../Topic/int%20\(C%23%20Reference\).md), [uint](../Topic/uint%20\(C%23%20Reference\).md), [long](../vs140/long--C#-Reference-.md), [ulong](../Topic/ulong%20\(C%23%20Reference\).md), [float](../vs140/float--C#-Reference-.md), [double](../vs140/double--C#-Reference-.md), or [decimal](../Topic/decimal%20\(C%23%20Reference\).md). However, there are no implicit conversions from other types to the `char` type.  
  
 The <xref:System.Char?qualifyHint=True> type provides several static methods for working with `char` values.  
  
## C# Language Specification  
 [!INCLUDE[CSharplangspec](../vs140/includes/Csharplangspec_md.md)]  
  
## See Also  
 <xref:System.Char?qualifyHint=False>   
 [C# Reference](../vs140/C#-Reference.md)   
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [C# Keywords](../Topic/C%23%20Keywords.md)   
 [Integral Types Table](../vs140/Integral-Types-Table--C#-Reference-.md)   
 [Built-in Types Table (Visual C#)](../Topic/Built-In%20Types%20Table%20\(C%23%20Reference\).md)   
 [Implicit Numeric Conversions Table](../vs140/Implicit-Numeric-Conversions-Table--C#-Reference-.md)   
 [Explicit Numeric Conversions Table (Visual C#)](../Topic/Explicit%20Numeric%20Conversions%20Table%20\(C%23%20Reference\).md)   
 [Nullable Types (C# Programming Guide)](../Topic/Nullable%20Types%20\(C%23%20Programming%20Guide\).md)   
 [String Basics (C# Programming Guide)](../Topic/Strings%20\(C%23%20Programming%20Guide\).md)