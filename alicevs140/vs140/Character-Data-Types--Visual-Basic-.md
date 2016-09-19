---
title: "Character Data Types (Visual Basic)"
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
ms.assetid: 902479ef-1679-47fc-9911-0c1c5008226c
caps.latest.revision: 25
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Character Data Types (Visual Basic)
[!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] provides *character data types* to deal with printable and displayable characters. While they both deal with Unicode characters, `Char` holds a single character whereas `String` contains an indefinite number of characters.  
  
 For a table that displays a side-by-side comparison of the [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] data types, see [Data Type Summary (Visual Basic)](../Topic/Data%20Type%20Summary%20\(Visual%20Basic\).md).  
  
## Char Type  
 The `Char` data type is a single two-byte (16-bit) Unicode character. If a variable always stores exactly one character, declare it as `Char`. For example:  
  
 [!CODE [VbVbalrCharTypes#1](../CodeSnippet/VS_Snippets_VBCSharp/vbvbalrchartypes#1)]  
  
 Each possible value in a `Char` or `String` variable is a *code point*, or character code, in the Unicode character set. Unicode characters include the basic ASCII character set, various other alphabet letters, accents, currency symbols, fractions, diacritics, and mathematical and technical symbols.  
  
> [!NOTE]
>  The Unicode character set reserves the code points D800 through DFFF (55296 through 55551 decimal) for *surrogate pairs*, which require two 16-bit values to represent a single code point. A `Char` variable cannot hold a surrogate pair, and a `String` uses two positions to hold such a pair.  
  
 For more information, see [Char Data Type](../vs140/Char-Data-Type--Visual-Basic-.md).  
  
## String Type  
 The `String` data type is a sequence of zero or more two-byte (16-bit) Unicode characters. If a variable can contain an indefinite number of characters, declare it as `String`. For example:  
  
 [!CODE [VbVbalrCharTypes#2](../CodeSnippet/VS_Snippets_VBCSharp/vbvbalrchartypes#2)]  
  
 For more information, see [String Data Type](../Topic/String%20Data%20Type%20\(Visual%20Basic\).md).  
  
## See Also  
 [Elementary Data Types](../vs140/Elementary-Data-Types--Visual-Basic-.md)   
 [Composite Data Types](../vs140/Composite-Data-Types--Visual-Basic-.md)   
 [Generic Types in Visual Basic](../Topic/Generic%20Types%20in%20Visual%20Basic%20\(Visual%20Basic\).md)   
 [Value Types and Reference Types](../Topic/Value%20Types%20and%20Reference%20Types.md)   
 [Type Conversions in Visual Basic](../vs140/Type-Conversions-in-Visual-Basic.md)   
 [Troubleshooting Data Types](../Topic/Troubleshooting%20Data%20Types%20\(Visual%20Basic\).md)   
 [Type Characters](../vs140/Type-Characters--Visual-Basic-.md)