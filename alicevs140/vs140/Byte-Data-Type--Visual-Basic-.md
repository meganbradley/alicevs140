---
title: "Byte Data Type (Visual Basic)"
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
ms.assetid: eed44dff-eaee-4937-a89f-444e418e74f6
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Byte Data Type (Visual Basic)
Holds unsigned 8-bit (1-byte) integers that range in value from 0 through 255.  
  
## Remarks  
 Use the `Byte` data type to contain binary data.  
  
 The default value of `Byte` is 0.  
  
## Programming Tips  
  
-   **Negative Numbers.** Because `Byte` is an unsigned type, it cannot represent a negative number. If you use the unary minus (`-`) operator on an expression that evaluates to type `Byte`, Visual Basic converts the expression to `Short` first.  
  
-   **Format Conversions.** When Visual Basic reads or writes files, or when it calls DLLs, methods, and properties, it can automatically convert between data formats. Binary data stored in `Byte` variables and arrays is preserved during such format conversions. You should not use a `String` variable for binary data, because its contents can be corrupted during conversion between ANSI and Unicode formats.  
  
-   **Widening.** The `Byte` data type widens to `Short`, `UShort`, `Integer`, `UInteger`, `Long`, `ULong`, `Decimal`, `Single`, or `Double`. This means you can convert `Byte` to any of these types without encountering a <xref:System.OverflowException?qualifyHint=True> error.  
  
-   **Type Characters.** `Byte` has no literal type character or identifier type character.  
  
-   **Framework Type.** The corresponding type in the .NET Framework is the <xref:System.Byte?qualifyHint=True> structure.  
  
## Example  
 In the following example, `b` is a `Byte` variable. The statements demonstrate the range of the variable and the application of bit-shift operators to it.  
  
 [!CODE [VbVbalrDataTypes#16](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrDataTypes#16)]  
  
## See Also  
 <xref:System.Byte?qualifyHint=True>   
 [Data Types](../Topic/Data%20Type%20Summary%20\(Visual%20Basic\).md)   
 [Type Conversion Functions](../vs140/Type-Conversion-Functions--Visual-Basic-.md)   
 [Conversion Summary](../vs140/Conversion-Summary--Visual-Basic-.md)   
 [Efficient Use of Data Types](../Topic/Efficient%20Use%20of%20Data%20Types%20\(Visual%20Basic\).md)