---
title: "Format Specification Syntax: printf and wprintf Functions"
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
apilocation: 
  - msvcr90.dll
  - msvcr110_clr0400.dll
  - msvcr100.dll
  - msvcr110.dll
  - msvcr80.dll
  - msvcr120.dll
apitype: DLLExport
ms.assetid: 664b1717-2760-4c61-bd9c-22eee618d825
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Format Specification Syntax: printf and wprintf Functions
Describes the syntax for format string arguments to `printf`, `wprintf`, and related functions. More secure versions of these functions are available; for more information, see [Security Features in the CRT](../vs140/Security-Features-in-the-CRT.md). For information about the individual functions, see the documentation for those specific functions. For a listing of these functions, see [Stream I/O](../vs140/Stream-I-O.md).  
  
 A format specification, which consists of optional and required fields, has the following form:  
  
 `%`[[flags](../vs140/Flag-Directives.md)] [[width](../vs140/printf-Width-Specification.md)] [**.**[precision](../vs140/Precision-Specification.md)] [{`h` &#124; `l` &#124; `ll` &#124; `w` &#124; `I` &#124; `I32` &#124; `I64`}] [type](../vs140/printf-Type-Field-Characters.md)  
  
 Each field of the format specification is a character or a number that signifies a particular format option or conversion specifier. The required `type` character specifies the kind of conversion to be applied to an argument. The optional `flags`, `width`, and `precision` fields control additional format aspects. A basic format specification contains only the percent sign and a `type` character—for example, `%s`, which specifies a string conversion. In the secure versions of the functions, if a percent sign is followed by a character that has no meaning as a format field, the invalid parameter handler is invoked. For more information, see [Parameter Validation](../vs140/Parameter-Validation.md). In the non-secure versions, the character is copied to the output unchanged. To print a percent-sign character, use `%%`.  
  
 The fields of the format specification control the following aspects of argument conversion and formatting:  
  
 `type`  
 Required conversion specifier character that determines whether the associated `argument` is interpreted as a character, a string, an integer, or a floating-point number. For more information, see [printf Type Field Characters](../vs140/printf-Type-Field-Characters.md).  
  
 `flags`  
 Optional character or characters that control output justification and output of signs, blanks, leading zeros, decimal points, and octal and hexadecimal prefixes. For more information, see [Flag Directives](../vs140/Flag-Directives.md). More than one flag can appear in a format specification, and flags can appear in any order.  
  
 `width`  
 Optional decimal number that specifies the minimum number of characters that are output. For more information, see [printf Width Specification](../vs140/printf-Width-Specification.md).  
  
 `precision`  
 Optional decimal number that specifies the maximum number of characters that are printed for strings, the number of significant digits or the number of digits after the decimal-point character for floating-point values, or the minimum number of digits that are printed for integer values. For more information, see "How Precision Values Affect Type" in [Precision Specification](../vs140/Precision-Specification.md).  
  
 `h` &#124; `l` &#124; `ll` &#124; `w` &#124; `I` &#124; `I32` &#124; `I64`  
 Optional prefixes to `type` that specify the size of the corresponding argument. For more information, see"Size Prefixes" in [Size Specification](../vs140/Size-Specification.md).  
  
> [!IMPORTANT]
>  Ensure that format specification strings are not user-defined. For example, consider a program that prompts the user to enter a name and stores the input in a string variable that's named `name`. To print `name`, do not do this:  
>   
>  `printf( name ); /* Danger!  If name contains "%s", program will crash */`  
>   
>  Instead, do this:  
>   
>  `printf( "%s", name );`  
  
## See Also  
 [printf, _printf_l, wprintf, _wprintf_l](../vs140/printf--_printf_l--wprintf--_wprintf_l.md)   
 [printf_s, wprintf_s](../vs140/printf_s--_printf_s_l--wprintf_s--_wprintf_s_l.md)   
 [printf_p Positional Parameters](../vs140/printf_p-Positional-Parameters.md)   
 [Flag Directives](../vs140/Flag-Directives.md)   
 [Width Specification](../vs140/printf-Width-Specification.md)   
 [Precision Specification](../vs140/Precision-Specification.md)   
 [Size Specification](../vs140/Size-Specification.md)   
 [printf Type Field Characters](../vs140/printf-Type-Field-Characters.md)