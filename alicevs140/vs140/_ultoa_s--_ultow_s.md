---
title: "_ultoa_s, _ultow_s"
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
  - _ultow_s
  - _ultoa_s
apilocation: 
  - msvcr100.dll
  - msvcr90.dll
  - msvcr110.dll
  - msvcr110_clr0400.dll
  - msvcr120.dll
  - msvcr80.dll
  - msvcrt.dll
apitype: DLLExport
ms.assetid: 606ce905-6752-46ac-a15a-bdc22920e1d4
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _ultoa_s, _ultow_s
Convert an unsigned long integer to a string. These are versions of [_ultoa, _ultow](../vs140/_ultoa--_ultow.md) with security enhancements as described in [Security Enhancements in the CRT](../vs140/Security-Features-in-the-CRT.md).  
  
## Syntax  
  
```  
errno_t _ultoa_s(  
    unsigned long value,  
    char *str,  
    size_t sizeOfstr,  
    int radix   
);  
errno_t _ultow_s(  
    unsigned long value,  
    wchar_t *str,  
    size_t sizeOfstr,  
    int radix   
);  
template <size_t size>  
errno_t _ultoa_s(  
    unsigned long value,  
    char (&str)[size],  
    int radix   
); // C++ only  
template <size_t size>  
errno_t _ultow_s(  
    unsigned long value,  
    wchar_t (&str)[size],  
    int radix   
); // C++ only  
```  
  
#### Parameters  
 `value`  
 Number to be converted.  
  
 `str`  
 String result.  
  
 `sizeOfstr`  
 The size of the `str` in bytes for `_ultoa_s` or words for `_ultow_s`.  
  
 `radix`  
 Base of `value`.  
  
## Return Value  
 Zero if the function was successful or an error code.  
  
## Remarks  
 The `_ultoa_s` function converts the digits of `value` to a null-terminated character string and stores the result (up to 33 bytes) in `str`. The `radix` argument specifies the base of `value`, which must be in the range 2 – 36. `_ultow_s` is a wide character version of `_ultoa_s`; the second argument of `_ultow_s` is a wide character strings.  
  
 If `str` is a `NULL` pointer, or if `sizeOfstr` is less than or equal to zero, the invalid parameter handler is invoked, as described in [Parameter Validation](../vs140/Parameter-Validation.md). If execution is allowed to continue, these functions return -1 and set `errno` to `EINVAL` or if the `value` or `str` out of range of a long integer, these functions will return a -1 and set the `errno` to `ERANGE`.  
  
 In C++, using these functions is simplified by template overloads; the overloads can infer buffer length automatically (eliminating the need to specify a size argument) and they can automatically replace older, non-secure functions with their newer, secure counterparts. For more information, see [Secure Template Overloads](../vs140/Secure-Template-Overloads.md).  
  
### Generic-Text Routine Mappings  
  
|TCHAR.H routine|_UNICODE & _MBCS not defined|_MBCS defined|_UNICODE defined|  
|---------------------|------------------------------------|--------------------|-----------------------|  
|`_ultot_s`|`_ultoa_s`|`_ultoa_s`|`_ultow_s`|  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`_ultoa_s`|<stdlib.h>|  
|`_ultow_s`|<stdlib.h>|  
  
 For additional compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## .NET Framework Equivalent  
 [System::Convert::ToString](https://msdn.microsoft.com/en-us/library/system.convert.tostring.aspx)  
  
## See Also  
 [Data Conversion](../vs140/Data-Conversion.md)   
 [_ultoa, _ultow](../vs140/_ultoa--_ultow.md)   
 [_ltoa, _ltow](../vs140/_ltoa--_ltow.md)   
 [_ltoa_s, _ltow_s](../vs140/_ltoa_s--_ltow_s.md)   
 [_ltoa_s, _ltow_s](../vs140/_ltoa_s--_ltow_s.md)