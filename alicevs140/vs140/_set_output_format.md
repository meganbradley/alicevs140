---
title: "_set_output_format"
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
apiname: 
  - _set_output_format
apilocation: 
  - msvcrt.dll
  - msvcr120.dll
  - msvcr100.dll
  - msvcr110_clr0400.dll
  - msvcr90.dll
  - msvcr110.dll
  - msvcr80.dll
apitype: DLLExport
ms.assetid: 1cb48df8-44b4-4400-bd27-287831d6b3ff
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _set_output_format
Customizes output formats used by formatted I/O functions.  
  
> [!IMPORTANT]
>  This function is obsolete. Beginning in Visual Studio 2015, it is not available in the CRT.  
  
## Syntax  
  
```  
unsigned int _set_output_format(  
   unsigned int format  
);  
```  
  
#### Parameters  
 [in] `format`  
 An value representing the format to use.  
  
## Return value  
 The previous output format.  
  
## Remarks  
 `_set_output_format` is used to configure the output of formatted I/O functions such as [printf_s](../vs140/printf_s--_printf_s_l--wprintf_s--_wprintf_s_l.md). At present, the only formatting convention that can be changed by this function is the number of digits displayed in exponents in the output of floating point numbers.  
  
 By default, the output of floating point numbers by functions such as `printf_s`, `wprintf_s`, and related functions in the Visual C++ Standard C library prints three digits for the exponent, even if three digits are not required to represent the value of the exponent. Zeroes are used to pad the value to three digits. `_set_output_format` allows you to change this behavior so that only two digits are printed in the exponent unless a third digit is required by the size of the exponent.  
  
 To enable two-digit exponents, call this function with the parameter `_TWO_DIGIT_EXPONENT`, as shown in the example. To disable two digit exponents, call this function with an argument of 0.  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`_set_output_format`|<stdio.h>|  
  
 For more compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## .NET Framework Equivalent  
 Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).  
  
## Example  
  
```  
// crt_set_output_format.c  
#include <stdio.h>  
  
void printvalues(double x, double y)  
{  
   printf_s("%11.4e %11.4e\n", x, y);  
   printf_s("%11.4E %11.4E\n", x, y);  
   printf_s("%11.4g %11.4g\n", x, y);  
   printf_s("%11.4G %11.4G\n", x, y);  
}  
  
int main()  
{  
   double x = 1.211E-5;  
   double y = 2.3056E-112;  
   unsigned int old_exponent_format;  
  
   // Use the default format  
   printvalues(x, y);  
  
   // Enable two-digit exponent format  
   old_exponent_format = _set_output_format(_TWO_DIGIT_EXPONENT);  
  
   printvalues(x, y);  
  
   // Disable two-digit exponent format  
   _set_output_format( old_exponent_format );  
  
   printvalues(x, y);  
}  
```  
  
 **1.2110e-005 2.3056e-112**  
**1.2110E-005 2.3056E-112**  
 **1.211e-005  2.306e-112**  
 **1.211E-005  2.306E-112**  
 **1.2110e-05 2.3056e-112**  
 **1.2110E-05 2.3056E-112**  
 **1.211e-05  2.306e-112**  
 **1.211E-05  2.306E-112**  
**1.2110e-005 2.3056e-112**  
**1.2110E-005 2.3056E-112**  
 **1.211e-005  2.306e-112**  
 **1.211E-005  2.306E-112**   
## See Also  
 [printf_s, _printf_s_l, wprintf_s, _wprintf_s_l](../vs140/printf_s--_printf_s_l--wprintf_s--_wprintf_s_l.md)   
 [printf Type Field Characters](../vs140/printf-Type-Field-Characters.md)   
 [_get_output_format](../vs140/_get_output_format.md)