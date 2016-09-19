---
title: "_strnextc, _wcsnextc, _mbsnextc, _mbsnextc_l"
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
  - _strnextc
  - _mbsnextc_l
  - _mbsnextc
  - _wcsnextc
apilocation: 
  - msvcr110.dll
  - msvcr110_clr0400.dll
  - msvcr80.dll
  - msvcr90.dll
  - msvcrt.dll
  - msvcr100.dll
  - msvcr120.dll
apitype: DLLExport
ms.assetid: e3086173-9eb5-4540-a23a-5d866bd05340
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _strnextc, _wcsnextc, _mbsnextc, _mbsnextc_l
Finds the next character in a string.  
  
> [!IMPORTANT]
>  `_mbsnextc` and `_mbsnextc_l` cannot be used in applications that execute in the Windows Runtime. For more information, see [CRT functions not supported with /ZW](http://msdn.microsoft.com/library/windows/apps/jj606124.aspx).  
  
## Syntax  
  
```  
unsigned int _strnextc(  
   const char *str  
);  
unsigned int _wscnextc(  
   const wchar_t *str  
);   
unsigned int _mbsnextc(  
   const unsigned char *str   
);  
unsigned int _mbsnextc_l(  
   const unsigned char *str,  
   _locale_t locale  
);  
  
```  
  
#### Parameters  
 `str`  
 Source string.  
  
 `locale`  
 Locale to use.  
  
## Return Value  
 Each of these functions returns the integer value of the next character in `str`*.*  
  
## Remarks  
 The `_mbsnextc` function returns the integer value of the next multibyte character in `str`, without advancing the string pointer. `_mbsnextc` recognizes multibyte-character sequences according to the [multibyte code page](../vs140/Code-Pages.md) currently in use.  
  
 If `str` is `NULL`, the invalid parameter handler is invoked, as described in [Parameter Validation](../vs140/Parameter-Validation.md). If execution is allowed to continue, `errno` is set to `EINVAL` and the function returns 0.  
  
 **Security Note** This API incurs a potential threat brought about by a buffer overrun problem. Buffer overrun problems are a frequent method of system attack, resulting in an unwarranted elevation of privilege. For more information, see [Avoiding Buffer Overruns](http://msdn.microsoft.com/library/windows/desktop/ms717795).  
  
### Generic-Text Routine Mappings  
  
|Tchar.h routine|_UNICODE and _MBCS not defined|_MBCS defined|_UNICODE defined|  
|---------------------|--------------------------------------|--------------------|-----------------------|  
|`_tcsnextc`|`_strnextc`|`_mbsnextc`|`_wcsnextc`|  
  
 `_strnextc` and `_wcsnextc` are single-byte–character string and wide-character string versions of `_mbsnextc`. `_wcsnextc` returns the integer value of the next wide character in `string`; `_strnextc` returns the integer value of the next single-byte character in `string`. `_strnextc` and `_wcsnextc` are provided only for this mapping and should not be used otherwise. For more information, see [Using Generic-Text Mappings](../vs140/Using-Generic-Text-Mappings.md) and [Generic-Text Mappings](../vs140/Generic-Text-Mappings.md).  
  
 `_mbsnextc_l` is identical except that it uses the locale parameter passed in instead. For more information, see [Locale](../vs140/Locale.md).  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`_mbsnextc`|<mbstring.h>|  
|`_mbsnextc_l`|<mbstring.h>|  
|`_strnextc`|<tchar.h>|  
|`_wcsnextc`|<tchar.h>|  
  
 For more compatibility information, see [Compatibility](../vs140/Compatibility.md).  
  
## .NET Framework Equivalent  
 Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).  
  
## See Also  
 [String Manipulation](../vs140/String-Manipulation--CRT-.md)   
 [Locale](../vs140/Locale.md)   
 [Interpretation of Multibyte-Character Sequences](../vs140/Interpretation-of-Multibyte-Character-Sequences.md)   
 [_mbsdec, _mbsdec_l, _strdec, _wcsdec](../vs140/_strdec--_wcsdec--_mbsdec--_mbsdec_l.md)   
 [_mbsinc, _mbsinc_l, _strinc, _wcsinc](../vs140/_strinc--_wcsinc--_mbsinc--_mbsinc_l.md)   
 [_mbsninc, _mbsninc_l, _strninc, _wcsninc](../vs140/_strninc--_wcsninc--_mbsninc--_mbsninc_l.md)