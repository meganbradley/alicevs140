---
title: "Type Characters (Visual Basic)"
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
ms.assetid: 6353cb9b-6ee4-4af6-a5a8-88ce39f90cc5
caps.latest.revision: 24
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Type Characters (Visual Basic)
In addition to specifying a data type in a declaration statement, you can force the data type of some programming elements with a *type character*. The type character must immediately follow the element, with no intervening characters of any kind.  
  
 The type character is not part of the name of the element. An element defined with a type character can be referenced without the type character.  
  
## Identifier Type Characters  
 [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] supplies a set of *identifier type characters*, which you can use in a declaration to specify the data type of a variable or constant. The following table shows the available identifier type characters with examples of usage.  
  
|Identifier type character|Data type|Example|  
|-------------------------------|---------------|-------------|  
|`%`|`Integer`|`Dim L%`|  
|`&`|`Long`|`Dim M&`|  
|`@`|`Decimal`|`Const W@ = 37.5`|  
|`!`|`Single`|`Dim Q!`|  
|`#`|`Double`|`Dim X#`|  
|`$`|`String`|`Dim V$ = "Secret"`|  
  
 No identifier type characters exist for the `Boolean`, `Byte`, `Char`, `Date`, `Object`, `SByte`, `Short`, `UInteger`, `ULong`, or `UShort` data types, or for any composite data types such as arrays or structures.  
  
 In some cases, you can append the `$` character to a [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] function, for example `Left$` instead of `Left`, to obtain a returned value of type `String`.  
  
 In all cases, the identifier type character must immediately follow the identifier name.  
  
## Literal Type Characters  
 A *literal* is a textual representation of a particular value of a data type.  
  
### Default Literal Types  
 The form of a literal as it appears in your code ordinarily determines its data type. The following table shows these default types.  
  
|Textual form of literal|Default data type|Example|  
|-----------------------------|-----------------------|-------------|  
|Numeric, no fractional part|`Integer`|`2147483647`|  
|Numeric, no fractional part, too large for `Integer`|`Long`|`2147483648`|  
|Numeric, fractional part|`Double`|`1.2`|  
|Enclosed in double quotation marks|`String`|`"A"`|  
|Enclosed within number signs|`Date`|`#5/17/1993 9:32 AM#`|  
  
### Forced Literal Types  
 [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] supplies a set of *literal type characters*, which you can use to force a literal to assume a data type other than the one its form indicates. You do this by appending the character to the end of the literal. The following table shows the available literal type characters with examples of usage.  
  
|Literal type character|Data type|Example|  
|----------------------------|---------------|-------------|  
|`S`|`Short`|`I = 347S`|  
|`I`|`Integer`|`J = 347I`|  
|`L`|`Long`|`K = 347L`|  
|`D`|`Decimal`|`X = 347D`|  
|`F`|`Single`|`Y = 347F`|  
|`R`|`Double`|`Z = 347R`|  
|`US`|`UShort`|`L = 347US`|  
|`UI`|`UInteger`|`M = 347UI`|  
|`UL`|`ULong`|`N = 347UL`|  
|`C`|`Char`|`Q = "."C`|  
  
 No literal type characters exist for the `Boolean`, `Byte`, `Date`, `Object`, `SByte`, or `String` data types, or for any composite data types such as arrays or structures.  
  
 Literals can also use the identifier type characters (`%`, `&`, `@`, `!`, `#`, `$`), as can variables, constants, and expressions. However, the literal type characters (`S`, `I`, `L`, `D`, `F`, `R`, `C`) can be used only with literals.  
  
 In all cases, the literal type character must immediately follow the literal value.  
  
## Hexadecimal and Octal Literals  
 The compiler normally construes an integer literal to be in the decimal (base 10) number system. You can force an integer literal to be hexadecimal (base 16) with the `&H` prefix, and you can force it to be octal (base 8) with the `&O` prefix. The digits that follow the prefix must be appropriate for the number system. The following table illustrates this.  
  
|Number base|Prefix|Valid digit values|Example|  
|-----------------|------------|------------------------|-------------|  
|Hexadecimal (base 16)|`&H`|0-9 and A-F|`&HFFFF`|  
|Octal (base 8)|`&O`|0-7|`&O77`|  
  
 You can follow a prefixed literal with a literal type character. The following example shows this.  
  
```  
Dim counter As Short = &H8000S  
Dim flags As UShort = &H8000US  
```  
  
 In the previous example, `counter` has the decimal value of -32768, and `flags` has the decimal value of +32768.  
  
## See Also  
 [Data Types in Visual Basic](../vs140/Data-Types-in-Visual-Basic.md)   
 [Elementary Data Types](../vs140/Elementary-Data-Types--Visual-Basic-.md)   
 [Value Types and Reference Types](../Topic/Value%20Types%20and%20Reference%20Types.md)   
 [Type Conversions in Visual Basic](../vs140/Type-Conversions-in-Visual-Basic.md)   
 [Troubleshooting Data Types](../Topic/Troubleshooting%20Data%20Types%20\(Visual%20Basic\).md)   
 [Variable Declaration in Visual Basic](../Topic/Variable%20Declaration%20in%20Visual%20Basic.md)   
 [Data Type Summary (Visual Basic)](../Topic/Data%20Type%20Summary%20\(Visual%20Basic\).md)