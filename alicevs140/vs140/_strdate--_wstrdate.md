---
title: "_strdate, _wstrdate"
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
  - _strdate
  - _wstrdate
apilocation: 
  - msvcr110.dll
  - msvcr120.dll
  - msvcr110_clr0400.dll
  - msvcr100.dll
  - msvcr80.dll
  - msvcr90.dll
  - msvcrt.dll
apitype: DLLExport
ms.assetid: de8e4097-58f8-42ba-9dcd-cb4d9a9f1696
caps.latest.revision: 26
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _strdate, _wstrdate
Copy current system date to a buffer. More secure versions of these functions are available; see [_strdate_s, _wstrdate_s](../vs140/_strdate_s--_wstrdate_s.md).  
  
## Syntax  
  
```  
char *_strdate(  
   char *datestr   
);  
wchar_t *_wstrdate(  
   wchar_t *datestr   
);  
template <size_t size>  
char *_strdate(  
   char (&datestr)[size]  
); // C++ only  
template <size_t size>  
wchar_t *_wstrdate(  
   wchar_t (&datestr)[size]  
); // C++ only  
```  
  
#### Parameters  
 `datestr`  
 A pointer to a buffer containing the formatted date string.  
  
## Return Value  
 Each of these functions returns a pointer to the resulting character string `datestr`.  
  
## Remarks  
 More secure versions of these functions are available; see [_strdate_s, _wstrdate_s](../vs140/_strdate_s--_wstrdate_s.md). It is recommended that the more secure functions be used wherever possible.  
  
 The `_strdate` function copies the current system date to the buffer pointed to by `datestr`, formatted `mm`/`dd`/`yy`, where `mm` is two digits representing the month, `dd` is two digits representing the day, and `yy` is the last two digits of the year. For example, the string `12/05/99` represents December 5, 1999. The buffer must be at least 9 bytes long.  
  
 If `datestr` is a `NULL` pointer, the invalid parameter handler is invoked, as described in [Parameter Validation](../vs140/Parameter-Validation.md). If execution is allowed to continue, these functions return -1 and set `errno` to `EINVAL`.  
  
 `_wstrdate` is a wide-character version of `_strdate`; the argument and return value of `_wstrdate` are wide-character strings. These functions behave identically otherwise.  
  
 In C++, these functions have template overloads that invoke the newer, secure counterparts of these functions. For more information, see [Secure Template Overloads](../vs140/Secure-Template-Overloads.md).  
  
### Generic-Text Routine Mappings  
  
|TCHAR.H routine|_UNICODE & _MBCS not defined|_MBCS defined|_UNICODE defined|  
|---------------------|------------------------------------|--------------------|-----------------------|  
|`_tstrdate`|`_strdate`|`_strdate`|`_wstrdate`|  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`_strdate`|<time.h>|  
|`_wstrdate`|<time.h> or <wchar.h>|  
  
 For additional compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## Example  
  
```  
// strdate.c  
// compile with: /W3  
#include <time.h>  
#include <stdio.h>  
int main()  
{  
    char tmpbuf[9];  
  
    // Set time zone from TZ environment variable. If TZ is not set,  
    // the operating system is queried to obtain the default value   
    // for the variable.   
    //  
    _tzset();  
  
    printf( "OS date: %s\n", _strdate(tmpbuf) ); // C4996  
    // Note: _strdate is deprecated; consider using _strdate_s instead  
}  
```  
  
 **OS date: 04/25/03**   
## .NET Framework Equivalent  
 [System::DateTime::Parse](https://msdn.microsoft.com/en-us/library/system.datetime.parse.aspx)  
  
## See Also  
 [Time Management](../vs140/Time-Management.md)   
 [asctime, _wasctime](../vs140/asctime--_wasctime.md)   
 [ctime, _ctime32, _ctime64, _wctime, _wctime32, _wctime64](../vs140/ctime--_ctime32--_ctime64--_wctime--_wctime32--_wctime64.md)   
 [gmtime, _gmtime32, _gmtime64](../vs140/gmtime--_gmtime32--_gmtime64.md)   
 [localtime, _localtime32, _localtime64](../vs140/localtime--_localtime32--_localtime64.md)   
 [mktime, _mktime32, _mktime64](../Topic/mktime,%20_mktime32,%20_mktime64.md)   
 [time, _time32, _time64](../vs140/time--_time32--_time64.md)   
 [_tzset](../vs140/_tzset.md)