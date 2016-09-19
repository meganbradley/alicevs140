---
title: "Conversions Between Strings and Other Types (Visual Basic)"
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
ms.assetid: c3a99596-f09a-44a5-81dd-1b89a094f1df
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Conversions Between Strings and Other Types (Visual Basic)
You can convert a numeric, `Boolean`, or date/time value to a `String`. You can also convert in the reverse direction — from a string value to numeric, `Boolean`, or `Date` — provided the contents of the string can be interpreted as a valid value of the destination data type. If they cannot, a run-time error occurs.  
  
 The conversions for all these assignments, in either direction, are narrowing conversions. You should use the type conversion keywords (`CBool`, `CByte`, `CDate`, `CDbl`, `CDec`, `CInt`, `CLng`, `CSByte`, `CShort`, `CSng`, `CStr`, `CUInt`, `CULng`, `CUShort`, and `CType`). The <xref:Microsoft.VisualBasic.Strings.Format?qualifyHint=False> and <xref:Microsoft.VisualBasic.Conversion.Val?qualifyHint=False> functions give you additional control over conversions between strings and numbers.  
  
 If you have defined a class or structure, you can define type conversion operators between `String` and the type of your class or structure. For more information, see [How to: Define a Conversion Operator](../vs140/How-to--Define-a-Conversion-Operator--Visual-Basic-.md).  
  
## Conversion of Numbers to Strings  
 You can use the `Format` function to convert a number to a formatted string, which can include not only the appropriate digits but also formatting symbols such as a currency sign (such as `$`), thousands separators or *digit grouping symbols* (such as `,`), and a decimal separator (such as `.`). `Format` automatically uses the appropriate symbols according to the **Regional Options** settings specified in the Windows **Control Panel**.  
  
 Note that the concatenation (`&`) operator can convert a number to a string implicitly, as the following example shows.  
  
```  
' The following statement converts count to a String value.  
Str = "The total count is " & count  
```  
  
## Conversion of Strings to Numbers  
 You can use the `Val` function to explicitly convert the digits in a string to a number. `Val` reads the string until it encounters a character other than a digit, space, tab, line feed, or period. The sequences "&O" and "&H" alter the base of the number system and terminate the scanning. Until it stops reading, `Val` converts all appropriate characters to a numeric value. For example, the following statement returns the value `141.825`.  
  
 `Val("   14   1.825 miles")`  
  
 When [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] converts a string to a numeric value, it uses the **Regional Options** settings specified in the Windows **Control Panel** to interpret the thousands separator, decimal separator, and currency symbol. This means that a conversion might succeed under one setting but not another. For example, `"$14.20"` is acceptable in the English (United States) locale but not in any French locale.  
  
## See Also  
 [Type Conversions in Visual Basic](../vs140/Type-Conversions-in-Visual-Basic.md)   
 [Widening and Narrowing Conversions](../Topic/Widening%20and%20Narrowing%20Conversions%20\(Visual%20Basic\).md)   
 [Implicit and Explicit Conversions](../Topic/Implicit%20and%20Explicit%20Conversions%20\(Visual%20Basic\).md)   
 [How to: Convert an Object to Another Type in Visual Basic](../vs140/How-to--Convert-an-Object-to-Another-Type-in-Visual-Basic.md)   
 [Array Conversions](../Topic/Array%20Conversions%20\(Visual%20Basic\).md)   
 [Data Types](../Topic/Data%20Type%20Summary%20\(Visual%20Basic\).md)   
 [Type Conversion Functions](../vs140/Type-Conversion-Functions--Visual-Basic-.md)   
 [Introduction to International Applications Based on the .NET Framework](../vs140/Introduction-to-International-Applications-Based-on-the-.NET-Framework.md)