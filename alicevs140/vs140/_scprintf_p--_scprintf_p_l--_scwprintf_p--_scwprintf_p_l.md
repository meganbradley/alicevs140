---
title: "_scprintf_p, _scprintf_p_l, _scwprintf_p, _scwprintf_p_l"
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
  - _scwprintf_p
  - _scprintf_p_l
  - _scwprintf_p_l
  - _scprintf_p
apilocation: 
  - msvcrt.dll
  - msvcr90.dll
  - msvcr100.dll
  - msvcr110_clr0400.dll
  - msvcr120.dll
  - msvcr110.dll
  - msvcr80.dll
apitype: DLLExport
ms.assetid: 8390d1e1-2826-47a4-851f-6635a88087cc
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _scprintf_p, _scprintf_p_l, _scwprintf_p, _scwprintf_p_l
Returns the number of characters in the formatted string, with the ability to specify the order in which parameters are used in the format string.  
  
## Syntax  
  
```  
int _scprintf_p(  
   const char *format [,  
   argument] ...   
);  
int _scprintf_p_l(  
   const char *format,  
   locale_t locale [,  
   argument] ...   
);  
int _scwprintf_p (  
   const wchar_t *format [,  
   argument] ...   
);  
int _scwprintf_p _l(  
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
  
## Return Value  
 Returns the number of characters that would be generated if the string were to be printed or sent to a file or buffer using the specified formatting codes. The value returned does not include the terminating null character. `_scwprintf_p` performs the same function for wide characters.  
  
 The difference between `_scprintf_p` and `_scprintf` is that `_scprintf_p` supports positional parameters, which allows specifying the order in which the arguments are used in the format string. For more information, see [printf Positional Parameters](../vs140/printf_p-Positional-Parameters.md).  
  
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
|`_sctprintf_p`|`_scprintf_p`|`_scprintf_p`|`_scwprintf_p`|  
|`_sctprintf_p_l`|`_scprintf_p_l`|`_scprintf_p_l`|`_scwprintf_p_l`|  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`_scprintf_p`, `_scprintf_p_l`|<stdio.h>|  
|`_scwprintf_p`, `_scwprintf_p_l`|<stdio.h> or <wchar.h>|  
  
 For more compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## See Also  
 [Stream I/O](../vs140/Stream-I-O.md)   
 [_scprintf, _scprintf_l, _scwprintf, _scwprintf_l](../vs140/_scprintf--_scprintf_l--_scwprintf--_scwprintf_l.md)   
 [_printf_p, _printf_p_l, _wprintf_p, _wprintf_p_l](../vs140/_printf_p--_printf_p_l--_wprintf_p--_wprintf_p_l.md)