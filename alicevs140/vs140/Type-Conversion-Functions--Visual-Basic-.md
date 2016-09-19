---
title: "Type Conversion Functions (Visual Basic)"
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
ms.assetid: d9d8d165-f967-44ff-a6cd-598e4740a99e
caps.latest.revision: 24
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Type Conversion Functions (Visual Basic)
These functions are compiled inline, meaning the conversion code is part of the code that evaluates the expression. Sometimes there is no call to a procedure to accomplish the conversion, which improves performance. Each function coerces an expression to a specific data type.  
  
## Syntax  
  
```  
CBool(expression)  
CByte(expression)  
CChar(expression)  
CDate(expression)  
CDbl(expression)  
CDec(expression)  
CInt(expression)  
CLng(expression)  
CObj(expression)  
CSByte(expression)  
CShort(expression)  
CSng(expression)  
CStr(expression)  
CUInt(expression)  
CULng(expression)  
CUShort(expression)  
```  
  
## Part  
 `expression`  
 Required. Any expression of the source data type.  
  
## Return Value Data Type  
 The function name determines the data type of the value it returns, as shown in the following table.  
  
|Function name|Return data type|Range for `expression` argument|  
|-------------------|----------------------|-------------------------------------|  
|`CBool`|[Boolean Data Type (Visual Basic)](../vs140/Boolean-Data-Type--Visual-Basic-.md)|Any valid `Char` or `String` or numeric expression.|  
|`CByte`|[Byte Data Type (Visual Basic)](../vs140/Byte-Data-Type--Visual-Basic-.md)|0 through 255 (unsigned); fractional parts are rounded.<sup>1</sup>|  
|`CChar`|[Char Data Type (Visual Basic)](../vs140/Char-Data-Type--Visual-Basic-.md)|Any valid `Char` or `String` expression; only first character of a `String` is converted; value can be 0 through 65535 (unsigned).|  
|`CDate`|[Date Data Type (Visual Basic)](../Topic/Date%20Data%20Type%20\(Visual%20Basic\).md)|Any valid representation of a date and time.|  
|`CDbl`|[Double Data Type (Visual Basic)](../Topic/Double%20Data%20Type%20\(Visual%20Basic\).md)|-1.79769313486231570E+308 through -4.94065645841246544E-324 for negative values; 4.94065645841246544E-324 through 1.79769313486231570E+308 for positive values.|  
|`CDec`|[Decimal Data Type (Visual Basic)](../vs140/Decimal-Data-Type--Visual-Basic-.md)|+/-79,228,162,514,264,337,593,543,950,335 for zero-scaled numbers, that is, numbers with no decimal places. For numbers with 28 decimal places, the range is +/-7.9228162514264337593543950335. The smallest possible non-zero number is 0.0000000000000000000000000001 (+/-1E-28).|  
|`CInt`|[Integer Data Type (Visual Basic)](../vs140/Integer-Data-Type--Visual-Basic-.md)|-2,147,483,648 through 2,147,483,647; fractional parts are rounded.<sup>1</sup>|  
|`CLng`|[Long Data Type (Visual Basic)](../Topic/Long%20Data%20Type%20\(Visual%20Basic\).md)|-9,223,372,036,854,775,808 through 9,223,372,036,854,775,807; fractional parts are rounded.<sup>1</sup>|  
|`CObj`|[Object Data Type](../Topic/Object%20Data%20Type.md)|Any valid expression.|  
|`CSByte`|[SByte Data Type (Visual Basic)](../Topic/SByte%20Data%20Type%20\(Visual%20Basic\).md)|-128 through 127; fractional parts are rounded.<sup>1</sup>|  
|`CShort`|[Short Data Type (Visual Basic)](../Topic/Short%20Data%20Type%20\(Visual%20Basic\).md)|-32,768 through 32,767; fractional parts are rounded.<sup>1</sup>|  
|`CSng`|[Single Data Type (Visual Basic)](../Topic/Single%20Data%20Type%20\(Visual%20Basic\).md)|-3.402823E+38 through -1.401298E-45 for negative values; 1.401298E-45 through 3.402823E+38 for positive values.|  
|`CStr`|[String Data Type (Visual Basic)](../Topic/String%20Data%20Type%20\(Visual%20Basic\).md)|Returns for `CStr` depend on the `expression` argument. See [Return Values for the CStr Function](../Topic/Return%20Values%20for%20the%20CStr%20Function%20\(Visual%20Basic\).md).|  
|`CUInt`|[UInteger Data Type](../vs140/UInteger-Data-Type.md)|0 through 4,294,967,295 (unsigned); fractional parts are rounded.<sup>1</sup>|  
|`CULng`|[ULong Data Type (Visual Basic)](../vs140/ULong-Data-Type--Visual-Basic-.md)|0 through 18,446,744,073,709,551,615 (unsigned); fractional parts are rounded.<sup>1</sup>|  
|`CUShort`|[UShort Data Type (Visual Basic)](../Topic/UShort%20Data%20Type%20\(Visual%20Basic\).md)|0 through 65,535 (unsigned); fractional parts are rounded.<sup>1</sup>|  
  
 <sup>1</sup> Fractional parts can be subject to a special type of rounding called *banker's rounding*. See "Remarks" for more information.  
  
## Remarks  
 As a rule, you should use the Visual Basic type conversion functions in preference to the .NET Framework methods such as `ToString()`, either on the <xref:System.Convert?qualifyHint=False> class or on an individual type structure or class. The Visual Basic functions are designed for optimal interaction with Visual Basic code, and they also make your source code shorter and easier to read. In addition, the .NET Framework conversion methods do not always produce the same results as the Visual Basic functions, for example when converting `Boolean` to `Integer`. For more information, see [Troubleshooting Data Types](../Topic/Troubleshooting%20Data%20Types%20\(Visual%20Basic\).md).  
  
## Behavior  
  
-   **Coercion.** In general, you can use the data type conversion functions to coerce the result of an operation to a particular data type rather than the default data type. For example, use `CDec` to force decimal arithmetic in cases where single-precision, double-precision, or integer arithmetic would normally take place.  
  
-   **Failed Conversions.** If the `expression` passed to the function is outside the range of the data type to which it is to be converted, an <xref:System.OverflowException?qualifyHint=False> occurs.  
  
-   **Fractional Parts.** When you convert a nonintegral value to an integral type, the integer conversion functions (`CByte`, `CInt`, `CLng`, `CSByte`, `CShort`, `CUInt`, `CULng`, and `CUShort`) remove the fractional part and round the value to the closest integer.  
  
     If the fractional part is exactly 0.5, the integer conversion functions round it to the nearest even integer. For example, 0.5 rounds to 0, and 1.5 and 2.5 both round to 2. This is sometimes called *banker's rounding*, and its purpose is to compensate for a bias that could accumulate when adding many such numbers together.  
  
     `CInt` and `CLng` differ from the <xref:Microsoft.VisualBasic.Conversion.Int?qualifyHint=False> and <xref:Microsoft.VisualBasic.Conversion.Fix?qualifyHint=False> functions, which truncate, rather than round, the fractional part of a number. Also, `Fix` and `Int` always return a value of the same data type as you pass in.  
  
-   **Date/Time Conversions.** Use the <xref:Microsoft.VisualBasic.Information.IsDate?qualifyHint=False> function to determine if a value can be converted to a date and time. `CDate` recognizes date literals and time literals but not numeric values. To convert a Visual Basic 6.0 `Date` value to a `Date` value in Visual Basic 2005 or later versions, you can use the <xref:System.DateTime.FromOADate?qualifyHint=True> method.  
  
-   **Neutral Date/Time Values.** The [Date Data Type (Visual Basic)](../Topic/Date%20Data%20Type%20\(Visual%20Basic\).md) always contains both date and time information. For purposes of type conversion, Visual Basic considers 1/1/0001 (January 1 of the year 1) to be a *neutral value* for the date, and 00:00:00 (midnight) to be a neutral value for the time. If you convert a `Date` value to a string, `CStr` does not include neutral values in the resulting string. For example, if you convert `#January 1, 0001 9:30:00#` to a string, the result is "9:30:00 AM"; the date information is suppressed. However, the date information is still present in the original `Date` value and can be recovered with functions such as <xref:Microsoft.VisualBasic.DateAndTime.DatePart?qualifyHint=False> function.  
  
-   **Culture Sensitivity.** The type conversion functions involving strings perform conversions based on the current culture settings for the application. For example, `CDate` recognizes date formats according to the locale setting of your system. You must provide the day, month, and year in the correct order for your locale, or the date might not be interpreted correctly. A long date format is not recognized if it contains a day-of-the-week string, such as "Wednesday".  
  
     If you need to convert to or from a string representation of a value in a format other than the one specified by your locale, you cannot use the Visual Basic type conversion functions. To do this, use the `ToString(IFormatProvider)` and `Parse(String, IFormatProvider)` methods of that value's type. For example, use <xref:System.Double.Parse?qualifyHint=True> when converting a string to a `Double`, and use <xref:System.Double.ToString?qualifyHint=True> when converting a value of type `Double` to a string.  
  
## CType Function  
 The [CType Function](../Topic/CType%20Function%20\(Visual%20Basic\).md) takes a second argument, `typename`, and coerces `expression` to `typename`, where `typename` can be any data type, structure, class, or interface to which there exists a valid conversion.  
  
 For a comparison of `CType` with the other type conversion keywords, see [DirectCast](../Topic/DirectCast%20Operator%20\(Visual%20Basic\).md) and [TryCast](../Topic/TryCast%20Operator%20\(Visual%20Basic\).md).  
  
## CBool Example  
 The following example uses the `CBool` function to convert expressions to `Boolean` values. If an expression evaluates to a nonzero value, `CBool` returns `True`; otherwise, it returns `False`.  
  
 [!CODE [VbVbalrFunctions#1](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrFunctions#1)]  
  
## CByte Example  
 The following example uses the `CByte` function to convert an expression to a `Byte`.  
  
 [!CODE [VbVbalrFunctions#2](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrFunctions#2)]  
  
## CChar Example  
 The following example uses the `CChar` function to convert the first character of a `String` expression to a `Char` type.  
  
 [!CODE [VbVbalrFunctions#3](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrFunctions#3)]  
  
 The input argument to `CChar` must be of data type `Char` or `String`. You cannot use `CChar` to convert a number to a character, because `CChar` cannot accept a numeric data type. The following example obtains a number representing a code point (character code) and converts it to the corresponding character. It uses the <xref:Microsoft.VisualBasic.Interaction.InputBox?qualifyHint=False> function to obtain the string of digits, `CInt` to convert the string to type `Integer`, and `ChrW` to convert the number to type `Char`.  
  
 [!CODE [VbVbalrFunctions#4](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrFunctions#4)]  
  
## CDate Example  
 The following example uses the `CDate` function to convert strings to `Date` values. In general, hard-coding dates and times as strings (as shown in this example) is not recommended. Use date literals and time literals, such as #Feb 12, 1969# and #4:45:23 PM#, instead.  
  
 [!CODE [VbVbalrFunctions#5](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrFunctions#5)]  
  
## CDbl Example  
 [!CODE [VbVbalrFunctions#6](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrFunctions#6)]  
  
## CDec Example  
 The following example uses the `CDec` function to convert a numeric value to `Decimal`.  
  
 [!CODE [VbVbalrFunctions#7](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrFunctions#7)]  
  
## CInt Example  
 The following example uses the `CInt` function to convert a value to `Integer`.  
  
 [!CODE [VbVbalrFunctions#8](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrFunctions#8)]  
  
## CLng Example  
 The following example uses the `CLng` function to convert values to `Long`.  
  
 [!CODE [VbVbalrFunctions#9](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrFunctions#9)]  
  
## CObj Example  
 The following example uses the `CObj` function to convert a numeric value to `Object`. The `Object` variable itself contains only a four-byte pointer, which points to the `Double` value assigned to it.  
  
 [!CODE [VbVbalrFunctions#10](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrFunctions#10)]  
  
## CSByte Example  
 The following example uses the `CSByte` function to convert a numeric value to `SByte`.  
  
 [!CODE [VbVbalrFunctions#11](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrFunctions#11)]  
  
## CShort Example  
 The following example uses the `CShort` function to convert a numeric value to `Short`.  
  
 [!CODE [VbVbalrFunctions#12](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrFunctions#12)]  
  
## CSng Example  
 The following example uses the `CSng` function to convert values to `Single`.  
  
 [!CODE [VbVbalrFunctions#13](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrFunctions#13)]  
  
## CStr Example  
 The following example uses the `CStr` function to convert a numeric value to `String`.  
  
 [!CODE [VbVbalrFunctions#14](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrFunctions#14)]  
  
 The following example uses the `CStr` function to convert `Date` values to `String` values.  
  
 [!CODE [VbVbalrFunctions#15](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrFunctions#15)]  
  
 `CStr` always renders a `Date` value in the standard short format for the current locale, for example, "6/15/2003 4:35:47 PM". However, `CStr` suppresses the *neutral values* of 1/1/0001 for the date and 00:00:00 for the time.  
  
 For more detail on the values returned by `CStr`, see [Return Values for the CStr Function](../Topic/Return%20Values%20for%20the%20CStr%20Function%20\(Visual%20Basic\).md).  
  
## CUInt Example  
 The following example uses the `CUInt` function to convert a numeric value to `UInteger`.  
  
 [!CODE [VbVbalrFunctions#16](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrFunctions#16)]  
  
## CULng Example  
 The following example uses the `CULng` function to convert a numeric value to `ULong`.  
  
 [!CODE [VbVbalrFunctions#17](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrFunctions#17)]  
  
## CUShort Example  
 The following example uses the `CUShort` function to convert a numeric value to `UShort`.  
  
 [!CODE [VbVbalrFunctions#18](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrFunctions#18)]  
  
## See Also  
 <xref:Microsoft.VisualBasic.Strings.Asc?qualifyHint=False>   
 <xref:Microsoft.VisualBasic.Strings.AscW?qualifyHint=False>   
 <xref:Microsoft.VisualBasic.Strings.Chr?qualifyHint=False>   
 <xref:Microsoft.VisualBasic.Strings.ChrW?qualifyHint=False>   
 <xref:Microsoft.VisualBasic.Conversion.Int?qualifyHint=False>   
 <xref:Microsoft.VisualBasic.Conversion.Fix?qualifyHint=False>   
 <xref:Microsoft.VisualBasic.Strings.Format?qualifyHint=False>   
 <xref:Microsoft.VisualBasic.Conversion.Hex?qualifyHint=False>   
 <xref:Microsoft.VisualBasic.Conversion.Oct?qualifyHint=False>   
 <xref:Microsoft.VisualBasic.Conversion.Str?qualifyHint=False>   
 <xref:Microsoft.VisualBasic.Conversion.Val?qualifyHint=False>   
 [Conversion Functions](../vs140/Conversion-Functions--Visual-Basic-.md)   
 [Type Conversions in Visual Basic](../vs140/Type-Conversions-in-Visual-Basic.md)