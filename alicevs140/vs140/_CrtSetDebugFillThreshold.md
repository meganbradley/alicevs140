---
title: "_CrtSetDebugFillThreshold"
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
  - _CrtSetDebugFillThreshold
apilocation: 
  - msvcr110_clr0400.dll
  - msvcr80.dll
  - msvcr120.dll
  - msvcrt.dll
  - msvcr110.dll
  - msvcr100.dll
  - msvcr90.dll
apitype: DLLExport
ms.assetid: 6cb360e8-56ae-4248-b17f-e28aee3e0ed7
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _CrtSetDebugFillThreshold
Retrieves or modifies the threshold controlling buffer-filling behavior in debug functions.  
  
## Syntax  
  
```  
size_t _CrtSetDebugFillThreshold(  
   size_t _NewThreshold  
);  
```  
  
#### Parameters  
 `newThreshold`  
 New threshold.  
  
## Return Value  
 The previous threshold.  
  
## Remarks  
 The debug versions of some security-enhanced CRT functions fill the buffer passed to them with a special character (0xFD). This helps to find cases where the incorrect size was passed to the function. Unfortunately, it also reduces performance. To improve performance, use `_CrtSetDebugFillThreshold` to disable buffer-filling for buffers larger than the threshold. A threshold of 0 will disable it for all buffers.  
  
 The default threshold is `SIZE_T_MAX`.  
  
 Here is a list of the affected functions.  
  
-   [strcpy_s, wcscpy_s, _mbscpy_s](../vs140/strcpy_s--wcscpy_s--_mbscpy_s.md)  
  
-   [strncpy_s, _strncpy_s_l, wcsncpy_s, _wcsncpy_s_l, _mbsncpy_s, _mbsncpy_s_l](../vs140/strncpy_s--_strncpy_s_l--wcsncpy_s--_wcsncpy_s_l--_mbsncpy_s--_mbsncpy_s_l.md)  
  
-   [_mbsnbcpy_s, _mbsnbcpy_s_l](../vs140/_mbsnbcpy_s--_mbsnbcpy_s_l.md)  
  
-   [strcat_s, wcscat_s, _mbscat_s](../vs140/strcat_s--wcscat_s--_mbscat_s.md)  
  
-   [strncat_s, _strncat_s_l, wcsncat_s, _wcsncat_s_l, _mbsncat_s, _mbsncat_s_l](../vs140/strncat_s--_strncat_s_l--wcsncat_s--_wcsncat_s_l--_mbsncat_s--_mbsncat_s_l.md)  
  
-   [_mbsnbcat_s, _mbsnbcat_s_l](../vs140/_mbsnbcat_s--_mbsnbcat_s_l.md)  
  
-   [_strset_s, _wcsset_s, _wcsset_s_l, _mbsset_s, _mbsset_s_l](../vs140/_strset_s--_strset_s_l--_wcsset_s--_wcsset_s_l--_mbsset_s--_mbsset_s_l.md)  
  
-   [_strnset_s, _strnset_s_l, _wcsnset_s, _wcsnset_s_l, _mbsnset_s, _mbsnset_s_l](../vs140/_strnset_s--_strnset_s_l--_wcsnset_s--_wcsnset_s_l--_mbsnset_s--_mbsnset_s_l.md)  
  
-   [_mbsnbset_s, _mbsnbset_s_l](../vs140/_mbsnbset_s--_mbsnbset_s_l.md)  
  
-   [_makepath_s, _wmakepath_s](../vs140/_makepath_s--_wmakepath_s.md)  
  
-   [_splitpath_s, _wsplitpath_s](../vs140/_splitpath_s--_wsplitpath_s.md)  
  
-   [_strlwr_s, _strlwr_s_l, _mbslwr_s, _mbslwr_s_l, _wcslwr_s, _wcslwr_s_l](../vs140/_strlwr_s--_strlwr_s_l--_mbslwr_s--_mbslwr_s_l--_wcslwr_s--_wcslwr_s_l.md)  
  
-   [_strupr_s, _strupr_s_l, _mbsupr_s, _mbsupr_s_l, _wcsupr_s, _wcsupr_s_l](../vs140/_strupr_s--_strupr_s_l--_mbsupr_s--_mbsupr_s_l--_wcsupr_s--_wcsupr_s_l.md)  
  
-   [strerror_s, _strerror_s, _wcserror_s, \__wcserror_s](../vs140/strerror_s--_strerror_s--_wcserror_s--__wcserror_s.md)  
  
-   [_itoa_s, _i64toa_s, _ui64toa_s, _itow_s, _i64tow_s, _ui64tow_s](../vs140/_itoa_s--_i64toa_s--_ui64toa_s--_itow_s--_i64tow_s--_ui64tow_s.md)  
  
-   [_ecvt_s](../vs140/_ecvt_s.md)  
  
-   [_fcvt_s](../Topic/_fcvt_s.md)  
  
-   [_gcvt_s](../Topic/_gcvt_s.md)  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`_CrtSetDebugFillThreshold`|<crtdbg.h>|  
  
 For more compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## Libraries  
 Debug versions of [C run-time libraries](../vs140/CRT-Library-Features.md) only.  
  
## Example  
  
```  
// crt_crtsetdebugfillthreshold.cpp  
// compile with: /MTd  
#include <stdio.h>  
#include <stdlib.h>  
#include <string.h>  
#include <crtdbg.h>  
  
void Clear( char buff[], size_t size )  
{  
   for( int i=0; i<size; ++i )  
      buff[i] = 0;  
}  
  
void Print( char buff[], size_t size )  
{  
   for( int i=0; i<size; ++i )  
      printf( "%02x  %c\n", (unsigned char)buff[i], buff[i] );  
}  
  
int main( void )  
{  
   char buff[10];  
  
   printf( "With buffer-filling on:\n" );  
   strcpy_s( buff, _countof(buff), "howdy" );  
   Print( buff, _countof(buff) );  
  
   _CrtSetDebugFillThreshold( 0 );  
  
   printf( "With buffer-filling off:\n" );  
   Clear( buff, _countof(buff) );  
   strcpy_s( buff, _countof(buff), "howdy" );  
   Print( buff, _countof(buff) );  
}  
```  
  
```  
With buffer-filling on:  
68  h  
6f  o  
77  w  
64  d  
79  y  
00  
fd  ²  
fd  ²  
fd  ²  
fd  ²  
With buffer-filling off:  
68  h  
6f  o  
77  w  
64  d  
79  y  
00  
00  
00  
00  
00  
```  
  
## .NET Framework Equivalent  
 Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).  
  
## See Also  
 [Debug Routines](../vs140/Debug-Routines.md)