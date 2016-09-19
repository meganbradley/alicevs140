---
title: "_mbsnbcat_s, _mbsnbcat_s_l"
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
  - _mbsnbcat_s_l
  - _mbsnbcat_s
apilocation: 
  - msvcr80.dll
  - msvcr110.dll
  - msvcr90.dll
  - msvcr110_clr0400.dll
  - msvcrt.dll
  - msvcr120.dll
  - msvcr100.dll
apitype: DLLExport
ms.assetid: 2c9e9be7-d979-4a54-8ada-23428b6648a9
caps.latest.revision: 30
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _mbsnbcat_s, _mbsnbcat_s_l
Appends to a multibyte character string, at most, the first `n` bytes of another multibyte-character string. These are versions of [_mbsnbcat](../vs140/_mbsnbcat--_mbsnbcat_l.md) that have security enhancements, as described in [Security Enhancements in the CRT](../vs140/Security-Features-in-the-CRT.md).  
  
> [!IMPORTANT]
>  This API cannot be used in applications that execute in the [!INCLUDE[wrt](../vs140/includes/wrt_md.md)]. For more information, see [CRT functions not supported with /ZW](http://msdn.microsoft.com/library/windows/apps/jj606124.aspx).  
  
## Syntax  
  
```  
errno_t _mbsnbcat_s(  
   unsigned char *dest,  
   size_t sizeInBytes,  
   const unsigned char *src,  
   size_t count   
);  
errno_t _mbsnbcat_s_l(  
   unsigned char *dest,  
   size_t sizeInBytes,  
   const unsigned char *src,  
   size_t count,  
   _locale_t locale  
);  
template <size_t size>  
errno_t _mbsnbcat_s(  
   unsigned char (&dest)[size],  
   const unsigned char *src,  
   size_t count   
); // C++ only  
template <size_t size>  
errno_t _mbsnbcat_s_l(  
   unsigned char (&dest)[size],  
   const unsigned char *src,  
   size_t count,  
   _locale_t locale  
); // C++ only  
```  
  
#### Parameters  
 `dest`  
 Null-terminated multibyte-character destination string.  
  
 `sizeInBytes`  
 Size of the `dest` buffer in bytes.  
  
 `src`  
 Null-terminated multibyte-character source string.  
  
 `Count`  
 Number of bytes from `src` to append to `dest`.  
  
 `locale`  
 Locale to use.  
  
## Return Value  
 Zero if successful; otherwise, an error code.  
  
### Error Conditions  
  
|`Dest`|`sizeInBytes`|`src`|Return value|  
|------------|-------------------|-----------|------------------|  
|`NULL`|any|any|`EINVAL`|  
|Any|<= 0|any|`EINVAL`|  
|Any|any|`NULL`|`EINVAL`|  
  
 If any of the error conditions occurs, the function generates an invalid parameter error, as described in [Parameter Validation](../vs140/Parameter-Validation.md). If the error is handled, the function returns `EINVAL` and sets `errno` to `EINVAL`.  
  
## Remarks  
 The `_mbsnbcat_s` function appends to `dest`, at most, the first `count` bytes of `src`. If the byte that immediately precedes the null character in `dest` is a lead byte, it is overwritten by the initial byte of `src`. Otherwise, the initial byte of `src` overwrites the terminating null character of `dest`. If a null byte appears in `src` before `count` bytes are appended, `_mbsnbcat_s` appends all bytes from `src`, up to the null character. If `count` is greater than the length of `src`, the length of `src` is used in place of `count`. The resulting string is terminated by a null character. If copying takes place between strings that overlap, the behavior is undefined.  
  
 The output value is affected by the setting of the `LC_CTYPE` category setting of the locale; see [setlocale, _wsetlocale](../vs140/setlocale--_wsetlocale.md) for more information. The versions of these functions are identical, except that the ones that don't have the `_l` suffix use the current locale and the ones that do have the `_l` suffix instead use the locale parameter that's passed in. For more information, see [Locale](../vs140/Locale.md).  
  
 In C++, the use of these functions is simplified by template overloads; the overloads can infer buffer length automatically and thereby eliminate the need to specify a size argument, and they can automatically use their newer, more secure functions to replace older, less-secure functions. For more information, see [Secure Template Overloads](../vs140/Secure-Template-Overloads.md).  
  
 The debug versions of these functions first fill the buffer with 0xFD. To disable this behavior, use [_CrtSetDebugFillThreshold](../vs140/_CrtSetDebugFillThreshold.md).  
  
### Generic-Text Routine Mappings  
  
|Tchar.h routine|_UNICODE and _MBCS not defined|_MBCS defined|_UNICODE defined|  
|---------------------|--------------------------------------|--------------------|-----------------------|  
|`_tcsncat`|[strncat](../vs140/strncat--_strncat_l--wcsncat--_wcsncat_l--_mbsncat--_mbsncat_l.md)|`_mbsnbcat_s`|[wcsncat](../vs140/strncat--_strncat_l--wcsncat--_wcsncat_l--_mbsncat--_mbsncat_l.md)|  
|`_tcsncat_s_l`|`_strncat_s_l`|`_mbsnbcat_s_l`|`_wcsncat_s_l`|  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`_mbsnbcat_s`|<mbstring.h>|  
|`_mbsnbcat_s_l`|<mbstring.h>|  
  
 For more compatibility information, see [Compatibility](../vs140/Compatibility.md).  
  
## .NET Framework Equivalent  
 Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).  
  
## See Also  
 [String Manipulation](../vs140/String-Manipulation--CRT-.md)   
 [_mbsnbcmp, _mbsnbcmp_l](../vs140/_mbsnbcmp--_mbsnbcmp_l.md)   
 [_mbsnbcnt, _mbsnbcnt_l, _mbsnccnt, _mbsnccnt_l, _strncnt, _wcsncnt](../vs140/_strncnt--_wcsncnt--_mbsnbcnt--_mbsnbcnt_l--_mbsnccnt--_mbsnccnt_l.md)   
 [_mbsnbcpy, _mbsnbcpy_l](../vs140/_mbsnbcpy--_mbsnbcpy_l.md)   
 [_mbsnbcpy_s, _mbsnbcpy_s_l](../vs140/_mbsnbcpy_s--_mbsnbcpy_s_l.md)   
 [_mbsnbset, _mbsnbset_l](../vs140/_mbsnbset--_mbsnbset_l.md)   
 [strncat, _strncat_l, wcsncat, _wcsncat_l, _mbsncat _mbsncat_l](../vs140/strncat--_strncat_l--wcsncat--_wcsncat_l--_mbsncat--_mbsncat_l.md)   
 [strncat_s, _strncat_s_l, wcsncat_s, _wcsncat_s_l, _mbsncat_s, _mbsncat_s_l](../vs140/strncat_s--_strncat_s_l--wcsncat_s--_wcsncat_s_l--_mbsncat_s--_mbsncat_s_l.md)