---
title: "gmtime_s, _gmtime32_s, _gmtime64_s"
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
  - _gmtime32_s
  - gmtime_s
  - _gmtime64_s
apilocation: 
  - msvcr120.dll
  - msvcr90.dll
  - msvcr110_clr0400.dll
  - msvcrt.dll
  - msvcr100.dll
  - msvcr110.dll
  - msvcr80.dll
apitype: DLLExport
ms.assetid: 261c7df0-2b0c-44ba-ba61-cb83efaec60f
caps.latest.revision: 29
translation.priority.mt: 
  - de-de
  - ja-jp
---
# gmtime_s, _gmtime32_s, _gmtime64_s
Converts a time value to a structure. These are versions of [_gmtime32, _gmtime64](../vs140/gmtime--_gmtime32--_gmtime64.md) with security enhancements as described in [Security Enhancements in the CRT](../vs140/Security-Features-in-the-CRT.md).  
  
## Syntax  
  
```  
errno_t gmtime_s(  
   struct tm* _tm,  
   const __time_t* time  
);  
errno_t _gmtime32_s(  
   struct tm* _tm,  
   const __time32_t* time  
);  
errno_t _gmtime64_s(  
   struct tm* _tm,  
   const __time64_t* time   
);  
```  
  
#### Parameters  
 `_tm`  
 Pointer to a `tm` structure. The fields of the returned structure hold the evaluated value of the `timer` argument in UTC rather than in local time.  
  
 `time`  
 Pointer to stored time. The time is represented as seconds elapsed since midnight (00:00:00), January 1, 1970, coordinated universal time (UTC).  
  
## Return Value  
 Zero if successful. The return value is an error code if there is a failure. Error codes are defined in Errno.h; for a listing of these errors, see [errno](../vs140/errno-Constants.md).  
  
### Error Conditions  
  
|`_tm`|`time`|Return|Value in `_tm`|  
|-----------|------------|------------|--------------------|  
|`NULL`|any|`EINVAL`|Not modified.|  
|Not `NULL` (points to valid memory)|`NULL`|`EINVAL`|All fields set to -1.|  
|Not `NULL`|< 0|`EINVAL`|All fields set to -1.|  
  
 In the case of the first two error conditions, the invalid parameter handler is invoked, as described in [Parameter Validation](../vs140/Parameter-Validation.md). If execution is allowed to continue, these functions set `errno` to `EINVAL` and return `EINVAL`.  
  
## Remarks  
 The `_gmtime32_s` function breaks down the `time` value and stores it in a structure of type `tm`, defined in Time.h. The address of the structure is passed in `_tm`. The value of `time` is usually obtained from a call to the `time` function.  
  
> [!NOTE]
>  The target environment should try to determine whether daylight savings time is in effect. The C run-time library assumes the United States rules for implementing the calculation of daylight saving time .  
  
 Each of the structure fields is of type `int`, as shown in the following table.  
  
 `tm_sec`  
 Seconds after minute (0 – 59).  
  
 `tm_min`  
 Minutes after hour (0 – 59).  
  
 `tm_hour`  
 Hours since midnight (0 – 23).  
  
 `tm_mday`  
 Day of month (1 – 31).  
  
 `tm_mon`  
 Month (0 – 11; January = 0).  
  
 `tm_year`  
 Year (current year minus 1900).  
  
 `tm_wday`  
 Day of week (0 – 6; Sunday = 0).  
  
 `tm_yday`  
 Day of year (0 – 365; January 1 = 0).  
  
 `tm_isdst`  
 Always 0 for `gmtime`.  
  
 `_gmtime64_s`, which uses the `__time64_t` structure, allows dates to be expressed up through 23:59:59, December 31, 3000, UTC; whereas `gmtime32_s` only represent dates through 23:59:59 January 18, 2038, UTC. Midnight, January 1, 1970, is the lower bound of the date range for both these functions.  
  
 `gmtime_s` is an inline function which evaluates to `_gmtime64_s` and `time_t` is equivalent to `__time64_t`. If you need to force the compiler to interpret `time_t` as the old 32-bit `time_t`, you can define `_USE_32BIT_TIME_T`. Doing this will cause `gmtime_s` to be in-lined to `_gmtime32_s`. This is not recommended because your application may fail after January 18, 2038, and it is not allowed on 64-bit platforms.  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`gmtime_s`|<time.h>|  
|`_gmtime32_s`|<time.h>|  
|`_gmtime64_s`|<time.h>|  
  
 For more compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## Example  
  
```  
// crt_gmtime64_s.c  
// This program uses _gmtime64_s to convert a 64-bit  
// integer representation of coordinated universal time  
// to a structure named newtime, then uses asctime_s to  
// convert this structure to an output string.  
  
#include <time.h>  
#include <stdio.h>  
  
int main( void )  
{  
   struct tm newtime;  
   __int64 ltime;  
   char buf[26];  
   errno_t err;  
  
   _time64( &ltime );  
  
   // Obtain coordinated universal time:   
   err = _gmtime64_s( &newtime, &ltime );  
   if (err)  
   {  
      printf("Invalid Argument to _gmtime64_s.");  
   }  
  
   // Convert to an ASCII representation   
   err = asctime_s(buf, 26, &newtime);  
   if (err)  
   {  
      printf("Invalid Argument to asctime_s.");  
   }  
  
   printf( "Coordinated universal time is %s\n",   
           buf );  
}  
```  
  
 **Coordinated universal time is Fri Apr 25 20:12:33 2003**   
## .NET Framework Equivalent  
  
-   [System::DateTime::UtcNow](https://msdn.microsoft.com/en-us/library/system.datetime.utcnow.aspx)  
  
-   [System::DateTime::ToUniversalTime](https://msdn.microsoft.com/en-us/library/system.datetime.touniversaltime.aspx)  
  
## See Also  
 [Time Management](../vs140/Time-Management.md)   
 [asctime_s, _wasctime_s](../vs140/asctime_s--_wasctime_s.md)   
 [ctime, _ctime32, _ctime64, _wctime, _wctime32, _wctime64](../vs140/ctime--_ctime32--_ctime64--_wctime--_wctime32--_wctime64.md)   
 [_ftime, _ftime32, _ftime64](../vs140/_ftime--_ftime32--_ftime64.md)   
 [gmtime, _gmtime32, _gmtime64](../vs140/gmtime--_gmtime32--_gmtime64.md)   
 [localtime_s, _localtime32_s, _localtime64_s](../vs140/localtime_s--_localtime32_s--_localtime64_s.md)   
 [_mkgmtime, _mkgmtime32, _mkgmtime64](../vs140/_mkgmtime--_mkgmtime32--_mkgmtime64.md)   
 [mktime, _mktime32, _mktime64](../Topic/mktime,%20_mktime32,%20_mktime64.md)   
 [time, _time32, _time64](../vs140/time--_time32--_time64.md)