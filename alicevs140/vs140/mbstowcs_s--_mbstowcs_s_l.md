---
title: "mbstowcs_s, _mbstowcs_s_l"
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
  - _mbstowcs_s_l
  - mbstowcs_s
apilocation: 
  - msvcr80.dll
  - msvcrt.dll
  - msvcr90.dll
  - msvcr100.dll
  - msvcr110.dll
  - msvcr110_clr0400.dll
  - msvcr120.dll
apitype: DLLExport
ms.assetid: 2fbda953-6918-498f-b440-3e7b21ed65a4
caps.latest.revision: 33
translation.priority.ht: 
  - de-de
  - ja-jp
---
# mbstowcs_s, _mbstowcs_s_l
Converts a sequence of multibyte characters to a corresponding sequence of wide characters. Versions of [mbstowcs](../vs140/mbstowcs--_mbstowcs_l.md) with security enhancements as described in [Security Enhancements in the CRT](../vs140/Security-Features-in-the-CRT.md).  
  
## Syntax  
  
```  
errno_t mbstowcs_s(  
   size_t *pReturnValue,  
   wchar_t *wcstr,  
   size_t sizeInWords,  
   const char *mbstr,  
   size_t count   
);  
errno_t _mbstowcs_s_l(  
   size_t *pReturnValue,  
   wchar_t *wcstr,  
   size_t sizeInWords,  
   const char *mbstr,  
   size_t count,  
   _locale_t locale  
);  
template <size_t size>  
errno_t mbstowcs_s(  
   size_t *pReturnValue,  
   wchar_t (&wcstr)[size],  
   const char *mbstr,  
   size_t count   
); // C++ only  
template <size_t size>  
errno_t _mbstowcs_s_l(  
   size_t *pReturnValue,  
   wchar_t (&wcstr)[size],  
   const char *mbstr,  
   size_t count,  
   _locale_t locale  
); // C++ only  
```  
  
#### Parameters  
 [out] `pReturnValue`  
 The number of characters converted.  
  
 [out] `wcstr`  
 Address of buffer for the resulting converted wide character string.  
  
 [in] `sizeInWords`  
 The size of the `wcstr` buffer in words.  
  
 [in]`mbstr`  
 The address of a sequence of null terminated multibyte characters.  
  
 [in] `count`  
 The maximum number of wide characters to store in the `wcstr` buffer, not including the terminating null, or [_TRUNCATE](../vs140/_TRUNCATE.md).  
  
 [in] `locale`  
 The locale to use.  
  
## Return Value  
 Zero if successful, an error code on failure.  
  
|Error condition|Return value and `errno`|  
|---------------------|------------------------------|  
|`wcstr` is `NULL` and `sizeInWords` > 0|`EINVAL`|  
|`mbstr` is `NULL`|`EINVAL`|  
|The destination buffer is too small to contain the converted string (unless `count` is `_TRUNCATE`; see Remarks below)|`ERANGE`|  
|`wcstr` is not `NULL` and `sizeInWords` == 0|`EINVAL`|  
  
 If any of these conditions occurs, the invalid parameter exception is invoked as described in [Parameter Validation](../vs140/Parameter-Validation.md) . If execution is allowed to continue, the function returns an error code and sets `errno` as indicated in the table.  
  
## Remarks  
 The `mbstowcs_s` function converts a string of multibyte characters pointed to by `mbstr` into wide characters stored in the buffer pointed to by `wcstr`. The conversion will continue for each character until one of these conditions is met:  
  
-   A multibyte null character is encountered  
  
-   An invalid multibyte character is encountered  
  
-   The number of wide characters stored in the `wcstr` buffer equals `count`.  
  
 The destination string is always null-terminated (even in the case of an error).  
  
 If `count` is the special value [_TRUNCATE](../vs140/_TRUNCATE.md), then `mbstowcs_s` converts as much of the string as will fit into the destination buffer, while still leaving room for a null terminator.  
  
 If `mbstowcs_s` successfully converts the source string, it puts the size in wide characters of the converted string, including the null terminator, into `*``pReturnValue` (provided `pReturnValue` is not `NULL`). This occurs even if the `wcstr` argument is `NULL` and provides a way to determine the required buffer size. Note that if `wcstr` is `NULL`, `count` is ignored, and `sizeInWords` must be 0.  
  
 If `mbstowcs_s` encounters an invalid multibyte character, it puts 0 in `*``pReturnValue`, sets the destination buffer to an empty string, sets `errno` to `EILSEQ`, and returns `EILSEQ`.  
  
 If the sequences pointed to by `mbstr` and `wcstr` overlap, the behavior of `mbstowcs_s` is undefined.  
  
> [!IMPORTANT]
>  Ensure that `wcstr` and `mbstr` do not overlap, and that `count` correctly reflects the number of multibyte characters to convert.  
  
 `mbstowcs_s` uses the current locale for any locale-dependent behavior; `_mbstowcs_s_l` is identical except that it uses the locale passed in instead. For more information, see [Locale](../vs140/Locale.md).  
  
 In C++, using these functions is simplified by template overloads; the overloads can infer buffer length automatically (eliminating the need to specify a size argument) and they can automatically replace older, non-secure functions with their newer, secure counterparts. For more information, see [Secure Template Overloads](../vs140/Secure-Template-Overloads.md).  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`mbstowcs_s`|<stdlib.h>|  
|`_mbstowcs_s_l`|<stdlib.h>|  
  
 For additional compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## .NET Framework Equivalent  
 Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).  
  
## See Also  
 [Data Conversion](../vs140/Data-Conversion.md)   
 [Locale](../vs140/Locale.md)   
 [MultiByteToWideChar](http://msdn.microsoft.com/library/windows/desktop/dd319072)   
 [Interpretation of Multibyte-Character Sequences](../vs140/Interpretation-of-Multibyte-Character-Sequences.md)   
 [_mbclen, mblen, _mblen_l, _mbsnlen, _mbsnlen_l](../vs140/_mbclen--mblen--_mblen_l.md)   
 [mbtowc, _mbtowc_l](../vs140/mbtowc--_mbtowc_l.md)   
 [wcstombs, _wcstombs_l](../vs140/wcstombs--_wcstombs_l.md)   
 [wctomb, _wctomb_l](../vs140/wctomb--_wctomb_l.md)