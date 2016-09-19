---
title: "C Integer Constants"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
  - C
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: fcf6b83c-2038-49ec-91ca-3d5ca1f83037
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# C Integer Constants
An "integer constant" is a decimal (base 10), octal (base 8), or hexadecimal (base 16) number that represents an integral value. Use integer constants to represent integer values that cannot be changed.  
  
## Syntax  
 *integer-constant*:  
 *decimal-constant integer-suffix* opt  
  
 *octal-constant integer-suffix* opt  
  
 *hexadecimal-constant integer-suffix* opt  
  
 *decimal-constant*:  
 *nonzero-digit*  
  
 *decimal-constant digit*  
  
 *octal-constant*:  
 **0**  
  
 *octal-constant octal-digit*  
  
 *hexadecimal-constant*:  
 **0x**  *hexadecimal-digit*  
  
 **0X**  *hexadecimal-digit*  
  
 *hexadecimal-constant hexadecimal-digit*  
  
 *nonzero-digit*: one of  
 **1 2 3 4 5 6 7 8 9**  
  
 *octal-digit*: one of  
 **0 1 2 3 4 5 6 7**  
  
 *hexadecimal-digit*: one of  
 **0 1 2 3 4 5 6 7 8 9**  
  
 **a b c d e f**  
  
 **A B C D E F**  
  
 *integer-suffix*:  
 *unsigned-suffix long-suffix* opt  
  
 *long-suffix unsigned-suffix* opt  
  
 *unsigned-suffix*: one of  
 **u U**  
  
 *long-suffix*: one of  
 **l L**  
  
 *64-bit integer-suffix*:  
 **i64**  
  
 Integer constants are positive unless they are preceded by a minus sign (**–**). The minus sign is interpreted as the unary arithmetic negation operator. (See [Unary Arithmetic Operators](../vs140/Unary-Arithmetic-Operators.md) for information about this operator.)  
  
 If an integer constant begins with **0x** or **0X**, it is hexadecimal. If it begins with the digit **0**, it is octal. Otherwise, it is assumed to be decimal.  
  
 The following lines are equivalent:  
  
```  
0x1C   /* = Hexadecimal representation for decimal 28 */  
034    /* = Octal representation for decimal 28 */  
```  
  
 No white-space characters can separate the digits of an integer constant. These examples show valid decimal, octal, and hexadecimal constants.  
  
```  
/* Decimal Constants */  
10  
132  
32179  
  
/* Octal Constants */  
012  
0204  
076663  
  
/* Hexadecimal Constants */  
0xa or 0xA  
0x84  
0x7dB3 or 0X7DB3  
```  
  
## See Also  
 [C Constants](../vs140/C-Constants.md)