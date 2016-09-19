---
title: "Size Specification"
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
  - msvcr120.dll
  - msvcr80.dll
  - msvcr110.dll
  - msvcr90.dll
  - msvcr110_clr0400.dll
  - msvcr100.dll
apitype: DLLExport
ms.assetid: 525dc5d8-e70a-4797-a6a0-ec504a27355c
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Size Specification
In a format specification, the fourth field is an argument length modifier for the conversion specifier. The `size` field prefixes to the `type` field—`h`, `l`, `w`, `I`, `I32`, `I64`, and `ll`—specify the "size" of the corresponding argument—long or short, 32-bit or 64-bit, single-byte character or wide character—depending on the conversion specifier that they modify. These size prefixes are used with `type` characters in the `printf` and `wprintf` families of functions to specify the interpretation of argument lengths, as shown in the following table. The `size` field is optional for some argument types. When no size prefix is specified, the formatter consumes integer arguments—for example, signed or unsigned `char`, `short`, `int`, `long`, and enumeration types—as 32-bit `int` types, and floating-point arguments are consumed as 64-bit `double` types. This matches the default argument promotion rules for variable argument lists. For more information about argument promotion, see [Ellipses and Default Arguments](../vs140/Ellipses-and-Default-Arguments.md). On both 32-bit and 64-bit systems, the format specification of a 64-bit integer argument must include a size prefix of `ll` or `I64`. Otherwise, the behavior of the formatter is undefined.  
  
 Some types are different sizes in 32-bit and 64-bit code. For example, `size_t` is 32 bits long in code compiled for x86, and 64 bits in code compiled for x64. To create platform-agnostic formatting code for variable-width types, you can use a variable-width argument length modifier. Alternatively, use a 64-bit argument length modifier and explicitly promote the variable-width argument type to 64 bits. The Microsoft-specific `I` argument length modifier handles variable-width integer arguments.  
  
> [!NOTE]
>  The `I`, `I32`, and `I64` length modifier prefixes are Microsoft extensions and are not ANSI-compatible. The `h` prefix when it's used with data of type `char`, the `w` prefix when it's used with data of type `wchar_t`, and the `l` prefix when it's used with data of type `double` are Microsoft extensions. The `hh`, `j`, `z`, and `t` length prefixes are not supported.  
  
### Size Prefixes for printf and wprintf Format-Type Specifiers  
  
|To specify|Use prefix|With type specifier|  
|----------------|----------------|-------------------------|  
|`long int`|`l` (lowercase L)|`d`, `i`, `o`, `x`, or `X`|  
|`long unsigned int`|`l`|`o`, `u`, `x`, or `X`|  
|`long long`|`ll`|`d`, `i`, `o`, `x`, or `X`|  
|`short int`|`h`|`d`, `i`, `o`, `x`, or `X`|  
|`short unsigned int`|`h`|`o`, `u`, `x`, or `X`|  
|`__int32`|`I32`|`d`, `i`, `o`, `x`, or `X`|  
|`unsigned __int32`|`I32`|`o`, `u`, `x`, or `X`|  
|`__int64`|`I64`|`d`, `i`, `o`, `x`, or `X`|  
|`unsigned __int64`|`I64`|`o`, `u`, `x`, or `X`|  
|`ptrdiff_t` (that is, `__int32` on 32-bit platforms, `__int64` on 64-bit platforms)|`I`|`d`, `i`, `o`, `x`, or `X`|  
|`size_t` (that is, `unsigned __int32` on 32-bit platforms, `unsigned __int64` on 64-bit platforms)|`I`|`o`, `u`, `x`, or `X`|  
|`long double` (In [!INCLUDE[vcprvc](../vs140/includes/vcprvc_md.md)], although `long double` is a distinct type, it has the same internal representation as `double`.)|`l` or `L`|`a`, `A`, `e`, `E`, `f`, `g`, or `G`|  
|Single-byte character with `printf` and `wprintf` functions. (An `hc` or `hC` type specifier is synonymous with `c` in `printf` functions and with `C` in `wprintf` functions.)|`h`|`c` or `C`|  
|Wide character with `printf` and `wprintf` functions. (An `lc`, `lC`, `wc` or `wC` type specifier is synonymous with `C` in `printf` functions and with `c` in `wprintf` functions.)|`l` or `w`|`c` or `C`|  
|Single-byte character string with `printf` and `wprintf` functions. (An `hs` or `hS` type specifier is synonymous with `s` in `printf` functions and with `S` in `wprintf` functions.)|`h`|`s`, `S`, or `Z`|  
|Wide-character string with `printf` and `wprintf` functions. (An `ls`, `lS`, `ws` or `wS` type specifier is synonymous with `S` in `printf` functions and with `s` in `wprintf` functions.)|`l` or `w`|`s`, `S`, or `Z`|  
  
## See Also  
 [printf, _printf_l, wprintf, _wprintf_l](../vs140/printf--_printf_l--wprintf--_wprintf_l.md)   
 [Format Specification Fields: printf and wprintf Functions](../vs140/Format-Specification-Syntax--printf-and-wprintf-Functions.md)   
 [Flag Directives](../vs140/Flag-Directives.md)   
 [Width Specification](../vs140/printf-Width-Specification.md)   
 [Precision Specification](../vs140/Precision-Specification.md)   
 [printf Type Field Characters](../vs140/printf-Type-Field-Characters.md)