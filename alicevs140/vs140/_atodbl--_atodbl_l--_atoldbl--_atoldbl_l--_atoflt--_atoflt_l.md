---
title: "_atodbl, _atodbl_l, _atoldbl, _atoldbl_l, _atoflt, _atoflt_l"
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
  - _atoldbl
  - _atoldbl_l
  - _atodbl
  - _atoflt
  - _atoflt_l
  - _atodbl_l
apilocation: 
  - msvcr100.dll
  - msvcrt.dll
  - msvcr110.dll
  - msvcr80.dll
  - msvcr90.dll
  - msvcr110_clr0400.dll
  - msvcr120.dll
apitype: DLLExport
ms.assetid: 2d2530f4-4bd4-42e3-8083-f2d2fbc8432a
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _atodbl, _atodbl_l, _atoldbl, _atoldbl_l, _atoflt, _atoflt_l
Converts a string to a double (`_atodbl`), long double (`_atoldbl`), or float (`_atoflt`).  
  
## Syntax  
  
```  
int _atodbl(  
   _CRT_DOUBLE * value,  
   char * str  
);  
int _atodbl_l (  
   _CRT_DOUBLE * value,  
   char * str,  
   locale_t locale  
);  
int _atoldbl(  
   _LDOUBLE * value,  
   char * str  
);  
int _atoldbl_l (  
   _LDOUBLE * value,  
   char * str,  
   locale_t locale  
);  
int _atoflt(  
   _CRT_FLOAT * value,  
   const char * str  
);  
int _atoflt_l(  
   _CRT_FLOAT * value,  
   const char * str,  
   locale_t locale  
);  
```  
  
#### Parameters  
 `value`  
 The double, long double, or float value that's produced by converting the string to a floating-point value. These values are wrapped in a structure.  
  
 `str`  
 The string to be parsed to convert into a floating-point value.  
  
 `locale`  
 The locale to use.  
  
## Return Value  
 Returns 0 if successful. Possible error codes are `_UNDERFLOW` or `_OVERFLOW`, which are defined in the header file Math.h.  
  
## Remarks  
 These functions convert a string to a floating-point value. The difference between these functions and the `atof` family of functions is that these functions do not generate floating-point code and do not cause hardware exceptions. Instead, error conditions are reported as error codes.  
  
 If a string does not have a valid interpretation as a floating-point value, `value` is set to zero and the return value is zero.  
  
 The versions of these functions that have the `_l` suffix are identical the versions that don't have the suffix, except that they use the locale parameter that's passed in instead of the current thread locale.  
  
## Requirements  
  
|Routines|Required header|  
|--------------|---------------------|  
|`_atodbl`, `_atoldbl`, `_atoflt`<br /><br /> `_atodbl_l`, `_atoldbl_l`, `_atoflt_l`|<stdlib.h>|  
  
## Example  
  
```  
// crt_atodbl.c  
// Uses _atodbl to convert a string to a double precision  
// floating point value.  
  
#include <stdlib.h>  
#include <stdio.h>  
  
int main()  
{  
   char str1[256] = "3.141592654";  
   char abc[256] = "abc";  
   char oflow[256] = "1.0E+5000";  
   _CRT_DOUBLE dblval;  
   _CRT_FLOAT fltval;  
   int retval;  
  
   retval = _atodbl(&dblval, str1);  
  
   printf("Double value: %lf\n", dblval.x);  
   printf("Return value: %d\n\n", retval);  
  
   retval = _atoflt(&fltval, str1);  
   printf("Float value: %f\n", fltval.f);  
   printf("Return value: %d\n\n", retval);  
  
   // A non-floating point value: returns 0.  
   retval = _atoflt(&fltval, abc);  
   printf("Float value: %f\n", fltval.f);  
   printf("Return value: %d\n\n", retval);  
  
   // Overflow.  
   retval = _atoflt(&fltval, oflow);  
   printf("Float value: %f\n", fltval.f);  
   printf("Return value: %d\n\n", retval);  
  
   return 0;  
}  
```  
  
 **Double value: 3.141593**  
**Return value: 0**  
**Float value: 3.141593**  
**Return value: 0**  
**Float value: 0.000000**  
**Return value: 0**  
**Float value: 1.#INF00**  
**Return value: 3**   
## See Also  
 [Data Conversion](../vs140/Data-Conversion.md)   
 [Floating-Point Support](../vs140/Floating-Point-Support.md)   
 [Locale](../vs140/Locale.md)   
 [atof, _atof_l, _wtof, _wtof_l](../vs140/atof--_atof_l--_wtof--_wtof_l.md)