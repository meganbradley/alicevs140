---
title: "_mbsnbset, _mbsnbset_l"
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
  - _mbsnbset
  - _mbsnbset_l
apilocation: 
  - msvcr80.dll
  - msvcr110.dll
  - msvcr90.dll
  - msvcrt.dll
  - msvcr100.dll
  - msvcr120.dll
  - msvcr110_clr0400.dll
apitype: DLLExport
ms.assetid: 8e46ef75-9a56-42d2-a522-a08450c67c19
caps.latest.revision: 26
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _mbsnbset, _mbsnbset_l
Sets the first `n` bytes of a multibyte-character string to a specified character. More secure versions of these functions are available; see [_mbsnbset_s, _mbsnbset_s_l](../vs140/_mbsnbset_s--_mbsnbset_s_l.md).  
  
> [!IMPORTANT]
>  This API cannot be used in applications that execute in the Windows Runtime. For more information, see [CRT functions not supported with /ZW](http://msdn.microsoft.com/library/windows/apps/jj606124.aspx).  
  
## Syntax  
  
```  
unsigned char *_mbsnbset(  
   unsigned char *str,  
   unsigned int c,  
   size_t count   
);  
unsigned char *_mbsnbset_l(  
   unsigned char *str,  
   unsigned int c,  
   size_t count,  
   _locale_t locale  
);  
```  
  
#### Parameters  
 `str`  
 String to be altered.  
  
 `c`  
 Single-byte or multibyte-character setting.  
  
 `count`  
 Number of bytes to be set.  
  
 `locale`  
 Locale to use.  
  
## Return Value  
 `_mbsnbset` returns a pointer to the altered string.  
  
## Remarks  
 The `_mbsnbset` and `_mbsnbset_l` functions set, at most, the first `count` bytes of `str` to `c`. If `count` is greater than the length of `str`, the length of `str` is used instead of `count`. If `c` is a multibyte character and cannot be set entirely into the last byte specified by `count`, the last byte is padded with a blank character. `_mbsnbset` and `_mbsnbset_l`does not place a terminating null at the end of `str`.  
  
 `_mbsnbset` and `_mbsnbset_l`is similar to `_mbsnset`, except that it sets `count` bytes rather than `count` characters of `c`.  
  
 If `str` is `NULL` or `count` is zero, this function generates an invalid parameter exception as described in [Parameter Validation](../vs140/Parameter-Validation.md). If execution is allowed to continue, `errno` is set to `EINVAL` and the function returns `NULL`. Also, if `c` is not a valid multibyte character, `errno` is set to `EINVAL` and a space is used instead.  
  
 The output value is affected by the setting of the `LC_CTYPE` category setting of the locale; see [setlocale](../vs140/setlocale--_wsetlocale.md) for more information. The `_mbsnbset` version of this function uses the current locale for this locale-dependent behavior; the `_mbsnbset_l` version is identical except that it use the locale parameter passed in instead. For more information, see [Locale](../vs140/Locale.md).  
  
 **Security Note** This API incurs a potential threat brought about by a buffer overrun problem. Buffer overrun problems are a frequent method of system attack, resulting in an unwarranted elevation of privilege. For more information, see [Avoiding Buffer Overruns](http://msdn.microsoft.com/library/windows/desktop/ms717795).  
  
### Generic-Text Routine Mappings  
  
|Tchar.h routine|_UNICODE and _MBCS not defined|_MBCS defined|_UNICODE defined|  
|---------------------|--------------------------------------|--------------------|-----------------------|  
|`_tcsnset`|`_strnset`|`_mbsnbset`|`_wcsnset`|  
|`_tcsnset_l`|`_strnset_l`|`_mbsnbset_l`|`_wcsnset_l`|  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`_mbsnbset`|<mbstring.h>|  
|`_mbsnbset_l`|<mbstring.h>|  
  
 For more compatibility information, see [Compatibility](../vs140/Compatibility.md).  
  
## Example  
  
```  
// crt_mbsnbset.c  
// compile with: /W3  
#include <mbstring.h>  
#include <stdio.h>  
  
int main( void )  
{  
   char string[15] = "This is a test";  
   /* Set not more than 4 bytes of string to be *'s */  
   printf( "Before: %s\n", string );  
   _mbsnbset( string, '*', 4 ); // C4996  
   // Note; _mbsnbset is deprecated; consider _mbsnbset_s  
   printf( "After:  %s\n", string );  
}  
```  
  
## Output  
  
```  
Before: This is a test  
After:  **** is a test  
```  
  
## .NET Framework Equivalent  
 Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).  
  
## See Also  
 [String Manipulation](../vs140/String-Manipulation--CRT-.md)   
 [_mbsnbcat, _mbsnbcat_l](../vs140/_mbsnbcat--_mbsnbcat_l.md)   
 [_strnset, _wcsnset, _mbsnset, _mbsnset_l](../vs140/_strnset--_strnset_l--_wcsnset--_wcsnset_l--_mbsnset--_mbsnset_l.md)   
 [_strset, _wcsset, _mbsset, _mbsset_l](../vs140/_strset--_strset_l--_wcsset--_wcsset_l--_mbsset--_mbsset_l.md)