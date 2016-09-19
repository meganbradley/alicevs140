---
title: "Char Data Type (Visual Basic)"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - VB
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-visual-basic
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: cd7547a9-7855-4e8e-b216-35d74a362657
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Char Data Type (Visual Basic)
Holds unsigned 16-bit (2-byte) code points ranging in value from 0 through 65535. Each *code point*, or character code, represents a single Unicode character.  
  
## Remarks  
 Use the `Char` data type when you need to hold only a single character and do not need the overhead of `String`. In some cases you can use `Char()`, an array of `Char` elements, to hold multiple characters.  
  
 The default value of `Char` is the character with a code point of 0.  
  
## Unicode Characters  
 The first 128 code points (0–127) of Unicode correspond to the letters and symbols on a standard U.S. keyboard. These first 128 code points are the same as those the ASCII character set defines. The second 128 code points (128–255) represent special characters, such as Latin-based alphabet letters, accents, currency symbols, and fractions. Unicode uses the remaining code points (256-65535) for a wide variety of symbols, including worldwide textual characters, diacritics, and mathematical and technical symbols.  
  
 You can use methods like <xref:System.Char.IsDigit?qualifyHint=False> and <xref:System.Char.IsPunctuation?qualifyHint=False> on a `Char` variable to determine its Unicode classification.  
  
## Type Conversions  
 Visual Basic does not convert directly between `Char` and the numeric types. You can use the <xref:Microsoft.VisualBasic.Strings.Asc?qualifyHint=False> or <xref:Microsoft.VisualBasic.Strings.AscW?qualifyHint=False> function to convert a `Char` value to an `Integer` that represents its code point. You can use the <xref:Microsoft.VisualBasic.Strings.Chr?qualifyHint=False> or <xref:Microsoft.VisualBasic.Strings.ChrW?qualifyHint=False> function to convert an `Integer` value to a `Char` that has that code point.  
  
 If the type checking switch ([Option Strict Statement](../vs140/Option-Strict-Statement.md)) is on, you must append the literal type character to a single-character string literal to identify it as the `Char` data type. The following example illustrates this.  
  
```  
Option Strict On  
Dim charVar As Char  
' The following statement attempts to convert a String literal to Char.  
' Because Option Strict is On, it generates a compiler error.  
charVar = "Z"  
' The following statement succeeds because it specifies a Char literal.  
charVar = "Z"C  
```  
  
## Programming Tips  
  
-   **Negative Numbers.** `Char` is an unsigned type and cannot represent a negative value. In any case, you should not use `Char` to hold numeric values.  
  
-   **Interop Considerations.** If you interface with components not written for the .NET Framework, for example Automation or COM objects, remember that character types have a different data width (8 bits) in other environments. If you pass an 8-bit argument to such a component, declare it as `Byte` instead of `Char` in your new Visual Basic code.  
  
-   **Widening.** The `Char` data type widens to `String`. This means you can convert `Char` to `String` and will not encounter a <xref:System.OverflowException?qualifyHint=True> error.  
  
-   **Type Characters.** Appending the literal type character `C` to a single-character string literal forces it to the `Char` data type. `Char` has no identifier type character.  
  
-   **Framework Type.** The corresponding type in the .NET Framework is the <xref:System.Char?qualifyHint=True> structure.  
  
## See Also  
 <xref:System.Char?qualifyHint=True>   
 <xref:Microsoft.VisualBasic.Strings.Asc?qualifyHint=False>   
 <xref:Microsoft.VisualBasic.Strings.AscW?qualifyHint=False>   
 <xref:Microsoft.VisualBasic.Strings.Chr?qualifyHint=False>   
 <xref:Microsoft.VisualBasic.Strings.ChrW?qualifyHint=False>   
 [Data Types](../Topic/Data%20Type%20Summary%20\(Visual%20Basic\).md)   
 [String Data Type (Visual Basic)](../Topic/String%20Data%20Type%20\(Visual%20Basic\).md)   
 [Type Conversion Functions](../vs140/Type-Conversion-Functions--Visual-Basic-.md)   
 [Conversion Summary](../vs140/Conversion-Summary--Visual-Basic-.md)   
 [How to: Call a Windows Function that Takes Unsigned Types](../vs140/How-to--Call-a-Windows-Function-that-Takes-Unsigned-Types--Visual-Basic-.md)   
 [Efficient Use of Data Types](../Topic/Efficient%20Use%20of%20Data%20Types%20\(Visual%20Basic\).md)