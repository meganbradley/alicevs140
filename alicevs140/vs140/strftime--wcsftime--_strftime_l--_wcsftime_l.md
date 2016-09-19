---
title: "strftime, wcsftime, _strftime_l, _wcsftime_l"
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
  - strftime
  - _wcsftime_l
  - _strftime_l
  - wcsftime
apilocation: 
  - msvcrt.dll
  - msvcr110.dll
  - msvcr80.dll
  - msvcr100.dll
  - msvcr110_clr0400.dll
  - msvcr120.dll
  - msvcr90.dll
apitype: DLLExport
ms.assetid: 6330ff20-4729-4c4a-82af-932915d893ea
caps.latest.revision: 24
translation.priority.ht: 
  - de-de
  - ja-jp
---
# strftime, wcsftime, _strftime_l, _wcsftime_l
Format a time string.  
  
## Syntax  
  
```  
size_t strftime(  
   char *strDest,  
   size_t maxsize,  
   const char *format,  
   const struct tm *timeptr   
);  
size_t _strftime_l(  
   char *strDest,  
   size_t maxsize,  
   const char *format,  
   const struct tm *timeptr,  
   _locale_t locale  
);  
size_t wcsftime(  
   wchar_t *strDest,  
   size_t maxsize,  
   const wchar_t *format,  
   const struct tm *timeptr   
);  
size_t _wcsftime_l(  
   wchar_t *strDest,  
   size_t maxsize,  
   const wchar_t *format,  
   const struct tm *timeptr,  
   _locale_t locale  
);  
```  
  
#### Parameters  
 `strDest`  
 Output string.  
  
 `maxsize`  
 Size of the `strDest` buffer, measured in characters (`char` or `wchart_t`).  
  
 `format`  
 Format-control string.  
  
 `timeptr`  
 `tm` data structure.  
  
 `locale`  
 The locale to use.  
  
## Return Value  
 `strftime` returns the number of characters placed in `strDest` and `wcsftime` returns the corresponding number of wide characters.  
  
 If the total number of characters, including the terminating null, is more than `maxsize`, both `strftime` and `wcsftime` return 0 and the contents of `strDest` are indeterminate.  
  
 The number of characters in `strDest` is equal to the number of literal characters in `format` as well as any characters that may be added to `format` via formatting codes. The terminating null of a string is not counted in the return value.  
  
## Remarks  
 The `strftime` and `wcsftime` functions format the `tm` time value in `timeptr` according to the supplied `format` argument and store the result in the buffer `strDest`*.* At most, `maxsize` characters are placed in the string. For a description of the fields in the `timeptr` structure, see [asctime](../vs140/asctime--_wasctime.md). `wcsftime` is the wide-character equivalent of `strftime`; its string-pointer argument points to a wide-character string. These functions behave identically otherwise.  
  
> [!NOTE]
>  In versions before Visual C++ 2005, the documentation described the `format` parameter of `wcsftime` as having the data type `const wchar_t *`, but the actual implementation of the `format` data type was `const char *`. The implementation of the `format`data type has been updated to reflect the previous and current documentation, that is, `const wchar_t *`.  
  
 This function validates its parameters. If `strDest`, `format`, or`timeptr` is a null pointer, or if the `tm` data structure addressed by `timeptr` is invalid (for example, if it contains out of range values for the time or date), or if the `format` string contains an invalid formatting code, the invalid parameter handler is invoked, as described in [Parameter Validation](../vs140/Parameter-Validation.md). If execution is allowed to continue, the function returns 0 and sets `errno` to `EINVAL`.  
  
### Generic-Text Routine Mappings  
  
|TCHAR.H routine|_UNICODE & _MBCS not defined|_MBCS defined|_UNICODE defined|  
|---------------------|------------------------------------|--------------------|-----------------------|  
|`_tcsftime`|`strftime`|`strftime`|`wcsftime`|  
  
 The `format` argument consists of one or more codes; as in `printf`, the formatting codes are preceded by a percent sign (`%`). Characters that do not begin with `%` are copied unchanged to `strDest`*.* The `LC_TIME` category of the current locale affects the output formatting of `strftime`. (For more information on `LC_TIME`, see [setlocale](../vs140/setlocale--_wsetlocale.md).) The functions without the `_l` suffix use the currently set locale. The versions of these functions with the `_l` suffix are identical except that they take the locale as a parameter and use that instead of the currently set locale. For more information, see [Locale](../vs140/Locale.md).  
  
 The formatting codes for `strftime` are listed below:  
  
 `%a`  
 Abbreviated weekday name  
  
 `%A`  
 Full weekday name  
  
 `%b`  
 Abbreviated month name  
  
 `%B`  
 Full month name  
  
 `%c`  
 Date and time representation appropriate for locale  
  
 `%d`  
 Day of month as decimal number (01 – 31)  
  
 `%H`  
 Hour in 24-hour format (00 – 23)  
  
 `%I`  
 Hour in 12-hour format (01 – 12)  
  
 `%j`  
 Day of year as decimal number (001 – 366)  
  
 `%m`  
 Month as decimal number (01 – 12)  
  
 `%M`  
 Minute as decimal number (00 – 59)  
  
 `%p`  
 Current locale's A.M./P.M. indicator for 12-hour clock  
  
 `%S`  
 Second as decimal number (00 – 59)  
  
 `%U`  
 Week of year as decimal number, with Sunday as first day of week (00 – 53)  
  
 `%w`  
 Weekday as decimal number (0 – 6; Sunday is 0)  
  
 `%W`  
 Week of year as decimal number, with Monday as first day of week (00 – 53)  
  
 `%x`  
 Date representation for current locale  
  
 `%X`  
 Time representation for current locale  
  
 `%y`  
 Year without century, as decimal number (00 – 99)  
  
 `%Y`  
 Year with century, as decimal number  
  
 `%z, %Z`  
 Either the time-zone name or time zone abbreviation, depending on registry settings; no characters if time zone is unknown  
  
 `%%`  
 Percent sign  
  
 As in the `printf` function, the `#` flag may prefix any formatting code. In that case, the meaning of the format code is changed as follows.  
  
|Format code|Meaning|  
|-----------------|-------------|  
|`%#a, %#A, %#b, %#B, %#p, %#X, %#z, %#Z, %#%`|`#` flag is ignored.|  
|`%#c`|Long date and time representation, appropriate for current locale. For example: "Tuesday, March 14, 1995, 12:41:29".|  
|`%#x`|Long date representation, appropriate to current locale. For example: "Tuesday, March 14, 1995".|  
|`%#d, %#H, %#I, %#j, %#m, %#M, %#S, %#U, %#w, %#W, %#y, %#Y`|Remove leading zeros (if any).|  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`strftime`|<time.h>|  
|`wcsftime`|<time.h> or <wchar.h>|  
|`_strftime_l`|<time.h>|  
|`_wcsftime_l`|<time.h> or <wchar.h>|  
  
 For additional compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## Example  
 See the example for [time](../vs140/time--_time32--_time64.md).  
  
## .NET Framework Equivalent  
  
-   [System::DateTime::ToLongDateString](https://msdn.microsoft.com/en-us/library/system.datetime.tolongdatestring.aspx)  
  
-   [System::DateTime::ToLongTimeString](https://msdn.microsoft.com/en-us/library/system.datetime.tolongtimestring.aspx)  
  
-   [System::DateTime::ToShortDateString](https://msdn.microsoft.com/en-us/library/system.datetime.toshortdatestring.aspx)  
  
-   [System::DateTime::ToShortTimeString](https://msdn.microsoft.com/en-us/library/system.datetime.toshorttimestring.aspx)  
  
-   [System::DateTime::ToString](https://msdn.microsoft.com/en-us/library/system.datetime.tostring.aspx)  
  
## See Also  
 [Locale](../vs140/Locale.md)   
 [Time Management](../vs140/Time-Management.md)   
 [String Manipulation](../vs140/String-Manipulation--CRT-.md)   
 [localeconv](../vs140/localeconv.md)   
 [setlocale, _wsetlocale](../vs140/setlocale--_wsetlocale.md)   
 [strcoll Functions](../vs140/strcoll-Functions.md)   
 [strxfrm, wcsxfrm, _strxfrm_l, _wcsxfrm_l](../vs140/strxfrm--wcsxfrm--_strxfrm_l--_wcsxfrm_l.md)