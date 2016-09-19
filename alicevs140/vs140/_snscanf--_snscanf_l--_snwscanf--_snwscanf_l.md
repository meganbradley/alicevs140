---
title: "_snscanf, _snscanf_l, _snwscanf, _snwscanf_l"
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
  - _snwscanf
  - _snscanf_l
  - _snscanf
  - _snwscanf_l
apilocation: 
  - msvcr90.dll
  - msvcr120.dll
  - msvcr100.dll
  - msvcr110.dll
  - msvcr110_clr0400.dll
  - msvcrt.dll
  - msvcr80.dll
apitype: DLLExport
ms.assetid: da1ac890-f905-4cd7-954b-3c90957b5551
caps.latest.revision: 24
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _snscanf, _snscanf_l, _snwscanf, _snwscanf_l
Reads formatted data of a specified length from a string. More secure versions of these functions are available; see [_snscanf_s, _snscanf_s_l, _snwscanf_s, _snwscanf_s_l](../vs140/_snscanf_s--_snscanf_s_l--_snwscanf_s--_snwscanf_s_l.md).  
  
## Syntax  
  
```  
int __cdecl _snscanf(  
   const char * input,  
   size_t length,  
   const char * format,  
   ...  
);  
int __cdecl _snscanf_l(  
   const char * input,  
   size_t length,  
   const char * format,  
   locale_t locale,  
   ...  
);  
int __cdecl _snwscanf(  
   const wchar_t * input,  
   size_t length,  
   const wchar_t * format,  
   ...  
);  
int __cdecl _snwscanf_l(  
   const wchar_t * input,  
   size_t length,  
   const wchar_t * format,  
   locale_t locale,  
   ...  
);  
```  
  
#### Parameters  
 `input`  
 Input string to examine.  
  
 `length`  
 Number of characters to examine in `input`.  
  
 `format`  
 One or more format specifiers.  
  
 `... (optional)`  
 Variables that will be used to store the values extracted from the input string by the format specifiers in `format`.  
  
 `locale`  
 The locale to use.  
  
## Return Value  
 Both of these functions returns the number of fields successfully converted and assigned; the return value does not include fields that were read but not assigned. A return value of 0 indicates that no fields were assigned. The return value is `EOF` for an error or if the end of the string is reached before the first conversion. For more information, see [sscanf](../vs140/sscanf--_sscanf_l--swscanf--_swscanf_l.md).  
  
 If `input` or `format` is a `NULL` pointer, or if `length` is less than or equal to zero, the invalid parameter handler is invoked, as described in [Parameter Validation](../vs140/Parameter-Validation.md). If execution is allowed to continue, these functions return `EOF` and set `errno` to `EINVAL`.  
  
 For information about these and other error codes, see [_doserrno, errno, _sys_errlist, and _sys_nerr](../vs140/errno--_doserrno--_sys_errlist--and-_sys_nerr.md).  
  
## Remarks  
 This function is like `sscanf` except that it provides the ability to specify a fixed number of characters to examine from the input string. For more information, see [sscanf](../vs140/sscanf--_sscanf_l--swscanf--_swscanf_l.md).  
  
 The versions of these functions with the `_l` suffix are identical except that they use the locale parameter passed in instead of the current thread locale.  
  
### Generic-Text Routine Mappings  
  
|Tchar.h routine|_UNICODE and _MBCS not defined|_MBCS defined|_UNICODE defined|  
|---------------------|--------------------------------------|--------------------|-----------------------|  
|`_sntscanf`|`_snscanf`|`_snscanf`|`_snwscanf`|  
|`_sntscanf_l`|`_snscanf_l`|`_snscanf_l`|`_snwscanf_l`|  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`_snscanf`, `_snscanf_l`|<stdio.h>|  
|`_snwscanf`, `_snwscanf_l`|<stdio.h> or <wchar.h>|  
  
 For more compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## Example  
  
```  
// crt_snscanf.c  
// compile with: /W3  
  
#include <stdio.h>  
int main( )  
{  
   char  str1[] = "15 12 14...";  
   wchar_t  str2[] = L"15 12 14...";  
   char  s1[3];  
   wchar_t  s2[3];  
   int   i;  
   float fp;  
  
   i = _snscanf( str1, 6,  "%s %f", s1, &fp); // C4996  
   // Note: _snscanf is deprecated; consider using _snscanf_s instead  
   printf("_snscanf converted %d fields: ", i);  
   printf("%s and %f\n", s1, fp);  
  
   i = _snwscanf( str2, 6,  L"%s %f", s2, &fp); // C4996  
   // Note: _snwscanf is deprecated; consider using _snwscanf_s instead  
   wprintf(L"_snwscanf converted %d fields: ", i);  
   wprintf(L"%s and %f\n", s2, fp);  
}  
```  
  
 **_snscanf converted 2 fields: 15 and 12.000000**  
**_snwscanf converted 2 fields: 15 and 12.000000**   
## .NET Framework Equivalent  
 Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).  
  
## See Also  
 [scanf Width Specification](../vs140/scanf-Width-Specification.md)