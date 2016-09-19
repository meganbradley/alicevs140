---
title: "_scprintf, _scprintf_l, _scwprintf, _scwprintf_l"
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
  - _scprintf_l
  - _scwprintf
  - _scwprintf_l
  - _scprintf
apilocation: 
  - msvcr100.dll
  - msvcr80.dll
  - msvcr90.dll
  - msvcr110.dll
  - msvcr120.dll
  - msvcr110_clr0400.dll
  - msvcrt.dll
apitype: DLLExport
ms.assetid: ecbb0ba6-5f4c-4ce6-a64b-144ad8b5fe92
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _scprintf, _scprintf_l, _scwprintf, _scwprintf_l
Returns the number of characters in the formatted string.  
  
## Syntax  
  
```  
int _scprintf(  
   const char *format [,  
   argument] ...   
);  
int _scprintf_l(  
   const char *format,  
   locale_t locale [,  
   argument] ...   
);  
int _scwprintf(  
   const wchar_t *format [,  
   argument] ...   
);  
int _scwprintf_l(  
   const wchar_t *format,  
   locale_t locale [,  
   argument] ...   
);  
```  
  
#### Parameters  
 `format`  
 Format-control string.  
  
 `argument`  
 Optional arguments.  
  
 `locale`  
 The locale to use.  
  
 For more information, see [Format Specifications](../vs140/Format-Specification-Syntax--printf-and-wprintf-Functions.md).  
  
## Return Value  
 Returns the number of characters that would be generated if the string were to be printed or sent to a file or buffer using the specified formatting codes. The value returned does not include the terminating null character. `_scwprintf` performs the same function for wide characters.  
  
 If `format` is a `NULL` pointer, the invalid parameter handler is invoked, as described in [Parameter Validation](../vs140/Parameter-Validation.md). If execution is allowed to continue, these functions return -1 and set `errno` to `EINVAL`.  
  
 For information about these and other error codes, see [_doserrno, errno, _sys_errlist, and _sys_nerr](../vs140/errno--_doserrno--_sys_errlist--and-_sys_nerr.md).  
  
## Remarks  
 Each `argument` (if any) is converted according to the corresponding format specification in `format`. The format consists of ordinary characters and has the same form and function as the `format` argument for [printf](../vs140/printf--_printf_l--wprintf--_wprintf_l.md).  
  
 The versions of these functions with the `_l` suffix are identical except that they use the locale parameter passed in instead of the current thread locale.  
  
> [!IMPORTANT]
>  Ensure that `format` is not a user-defined string.  
  
### Generic-Text Routine Mappings  
  
|Tchar.h routine|_UNICODE and _MBCS not defined|_MBCS defined|_UNICODE defined|  
|---------------------|--------------------------------------|--------------------|-----------------------|  
|`_sctprintf`|`_scprintf`|`_scprintf`|`_scwprintf`|  
|`_sctprintf_l`|`_scprintf_l`|`_scprintf_l`|`_scwprintf_l`|  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`_scprintf`, `_scprintf_l`|<stdio.h>|  
|`_scwprintf`, `_scwprintf_l`|<stdio.h> or <wchar.h>|  
  
 For more compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## Example  
  
```  
// crt__scprintf.c  
  
#define _USE_MATH_DEFINES  
  
#include <stdio.h>  
#include <math.h>  
#include <malloc.h>  
  
int main( void )  
{  
   int count;  
   int size;  
   char *s = NULL;  
  
   count = _scprintf( "The value of Pi is calculated to be %f.\n",  
                      M_PI);  
  
   size = count + 1; // the string will need one more char for the null terminator  
   s = malloc(sizeof(char) * size);  
   sprintf_s(s, size, "The value of Pi is calculated to be %f.\n",  
                      M_PI);  
   printf("The length of the following string will be %i.\n", count);  
   printf("%s", s);  
   free( s );  
}  
```  
  
 **The length of the following string will be 46.**  
**The value of Pi is calculated to be 3.141593.**   
## See Also  
 [Stream I/O](../vs140/Stream-I-O.md)   
 [fprintf, fwprintf](../vs140/fprintf--_fprintf_l--fwprintf--_fwprintf_l.md)   
 [printf, wprintf](../vs140/printf--_printf_l--wprintf--_wprintf_l.md)   
 [scanf, wscanf](../vs140/scanf--_scanf_l--wscanf--_wscanf_l.md)   
 [sscanf, swscanf](../vs140/sscanf--_sscanf_l--swscanf--_swscanf_l.md)   
 [vprintf Functions](../vs140/vprintf-Functions.md)