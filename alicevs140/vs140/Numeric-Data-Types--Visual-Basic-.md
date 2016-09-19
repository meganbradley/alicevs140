---
title: "Numeric Data Types (Visual Basic)"
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
ms.assetid: a27bd4d0-7e14-43eb-9cc4-b42eaab323c9
caps.latest.revision: 27
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Numeric Data Types (Visual Basic)
[!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] supplies several *numeric data types* for handling numbers in various representations. *Integral* types represent only whole numbers (positive, negative, and zero), and *nonintegral* types represent numbers with both integer and fractional parts.  
  
 For a table showing a side-by-side comparison of the [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] data types, see [Data Type Summary (Visual Basic)](../Topic/Data%20Type%20Summary%20\(Visual%20Basic\).md).  
  
## Integral Numeric Types  
 *Integral data types* are those that represent only numbers without fractional parts.  
  
 The *signed* integral data types are [SByte Data Type (Visual Basic)](../Topic/SByte%20Data%20Type%20\(Visual%20Basic\).md) (8-bit), [Short Data Type (Visual Basic)](../Topic/Short%20Data%20Type%20\(Visual%20Basic\).md) (16-bit), [Integer Data Type (Visual Basic)](../vs140/Integer-Data-Type--Visual-Basic-.md) (32-bit), and [Long Data Type (Visual Basic)](../Topic/Long%20Data%20Type%20\(Visual%20Basic\).md) (64-bit). If a variable always stores integers rather than fractional numbers, declare it as one of these types.  
  
 The *unsigned* integral types are [Byte Data Type (Visual Basic)](../vs140/Byte-Data-Type--Visual-Basic-.md) (8-bit), [UShort Data Type (Visual Basic)](../Topic/UShort%20Data%20Type%20\(Visual%20Basic\).md) (16-bit), [UInteger Data Type](../vs140/UInteger-Data-Type.md) (32-bit), and [ULong Data Type (Visual Basic)](../vs140/ULong-Data-Type--Visual-Basic-.md) (64-bit). If a variable contains binary data, or data of unknown nature, declare it as one of these types.  
  
### Performance  
 Arithmetic operations are faster with integral types than with other data types. They are fastest with the `Integer` and `UInteger` types in [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)].  
  
### Large Integers  
 If you need to hold an integer larger than the `Integer` data type can hold, you can use the `Long` data type instead. `Long` variables can hold numbers from -9,223,372,036,854,775,808 through 9,223,372,036,854,775,807. Operations with `Long` are slightly slower than with `Integer`.  
  
 If you need even larger values, you can use the [Decimal Data Type (Visual Basic)](../vs140/Decimal-Data-Type--Visual-Basic-.md). You can hold numbers from -79,228,162,514,264,337,593,543,950,335 through 79,228,162,514,264,337,593,543,950,335 in a `Decimal` variable if you do not use any decimal places. However, operations with `Decimal` numbers are considerably slower than with any other numeric data type.  
  
### Small Integers  
 If you do not need the full range of the `Integer` data type, you can use the `Short` data type, which can hold integers from -32,768 through 32,767. For the smallest integer range, the `SByte` data type holds integers from -128 through 127. If you have a very large number of variables that hold small integers, the common language runtime can sometimes store your `Short` and `SByte` variables more efficiently and save memory consumption. However, operations with `Short` and `SByte` are somewhat slower than with `Integer`.  
  
### Unsigned Integers  
 If you know that your variable never needs to hold a negative number, you can use the *unsigned types*`Byte`, `UShort`, `UInteger`, and `ULong`. Each of these data types can hold a positive integer twice as large as its corresponding signed type (`SByte`, `Short`, `Integer`, and `Long`). In terms of performance, each unsigned type is exactly as efficient as its corresponding signed type. In particular, `UInteger` shares with `Integer` the distinction of being the most efficient of all the elementary numeric data types.  
  
## Nonintegral Numeric Types  
 *Nonintegral data types* are those that represent numbers with both integer and fractional parts.  
  
 The nonintegral numeric data types are `Decimal` (128-bit fixed point), [Single Data Type (Visual Basic)](../Topic/Single%20Data%20Type%20\(Visual%20Basic\).md) (32-bit floating point), and [Double Data Type (Visual Basic)](../Topic/Double%20Data%20Type%20\(Visual%20Basic\).md) (64-bit floating point). They are all signed types. If a variable can contain a fraction, declare it as one of these types.  
  
 `Decimal` is not a floating-point data type. `Decimal` numbers have a binary integer value and an integer scaling factor that specifies what portion of the value is a decimal fraction.  
  
 You can use `Decimal` variables for money values. The advantage is the precision of the values. The `Double` data type is faster and requires less memory, but it is subject to rounding errors. The `Decimal` data type retains complete accuracy to 28 decimal places.  
  
 Floating-point (`Single` and `Double`) numbers have larger ranges than `Decimal` numbers but can be subject to rounding errors. Floating-point types support fewer significant digits than `Decimal` but can represent values of greater magnitude.  
  
 Nonintegral number values can be expressed as mmmEeee, in which mmm is the *mantissa* (the significant digits) and eee is the *exponent* (a power of 10). The highest positive values of the nonintegral types are 7.9228162514264337593543950335E+28 for `Decimal`, 3.4028235E+38 for `Single`, and 1.79769313486231570E+308 for `Double`.  
  
### Performance  
 `Double` is the most efficient of the fractional data types, because the processors on current platforms perform floating-point operations in double precision. However, operations with `Double` are not as fast as with the integral types such as `Integer`.  
  
### Small Magnitudes  
 For numbers with the smallest possible magnitude (closest to 0), `Double` variables can hold numbers as small as -4.94065645841246544E-324 for negative values and 4.94065645841246544E-324 for positive values.  
  
### Small Fractional Numbers  
 If you do not need the full range of the `Double` data type, you can use the `Single` data type, which can hold floating-point numbers from -3.4028235E+38 through 3.4028235E+38. The smallest magnitudes for `Single` variables are -1.401298E-45 for negative values and 1.401298E-45 for positive values. If you have a very large number of variables that hold small floating-point numbers, the common language runtime can sometimes store your `Single` variables more efficiently and save memory consumption.  
  
## See Also  
 [Elementary Data Types](../vs140/Elementary-Data-Types--Visual-Basic-.md)   
 [Character Data Types](../vs140/Character-Data-Types--Visual-Basic-.md)   
 [Miscellaneous Data Types](../Topic/Miscellaneous%20Data%20Types%20\(Visual%20Basic\).md)   
 [Troubleshooting Data Types](../Topic/Troubleshooting%20Data%20Types%20\(Visual%20Basic\).md)   
 [How to: Call a Windows Function that Takes Unsigned Types](../vs140/How-to--Call-a-Windows-Function-that-Takes-Unsigned-Types--Visual-Basic-.md)