---
title: "_mbccpy, _mbccpy_l"
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
  - _mbccpy
  - _mbccpy_l
apilocation: 
  - msvcr120.dll
  - msvcr80.dll
  - msvcr110_clr0400.dll
  - msvcr100.dll
  - msvcr90.dll
  - msvcr110.dll
  - msvcrt.dll
apitype: DLLExport
ms.assetid: 13f4de6e-7792-41ac-b319-dd9b135433aa
caps.latest.revision: 26
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _mbccpy, _mbccpy_l
Copies a multibyte character from one string to another string. More secure versions of these functions are available; see [_mbccpy_s, _mbccpy_s_l](../vs140/_mbccpy_s--_mbccpy_s_l.md).  
  
> [!IMPORTANT]
>  This API cannot be used in applications that execute in the Windows Runtime. For more information, see [CRT functions not supported with /ZW](http://msdn.microsoft.com/library/windows/apps/jj606124.aspx).  
  
## Syntax  
  
```  
void _mbccpy(  
   unsigned char *dest,  
   const unsigned char *src   
);  
void _mbccpy_l(  
   unsigned char *dest,  
   const unsigned char *src,  
   _locale_t locale  
);  
```  
  
#### Parameters  
 `dest`  
 Copy destination.  
  
 `src`  
 Multibyte character to copy.  
  
 `locale`  
 Locale to use.  
  
## Remarks  
 The `_mbccpy` function copies one multibyte character from `src` to `dest`.  
  
 This function validates its parameters. If `_mbccpy` is passed a null pointer for `dest` or `src`, the invalid parameter handler is invoked, as described in [Parameter Validation](../vs140/Parameter-Validation.md). If execution is allowed to continue, `errno` is set to `EINVAL`.  
  
 `_mbccpy` uses the current locale for any locale-dependent behavior. `_mbccpy_l` is identical to `_mbccpy` except that `_mbccpy_l` uses the locale passed in for any locale-dependent behavior. For more information, see [Locale](../vs140/Locale.md).  
  
 **Security Note** Use a null-terminated string. The null-terminated string must not exceed the size of the destination buffer. For more information, see [Avoiding Buffer Overruns](http://msdn.microsoft.com/library/windows/desktop/ms717795). Buffer overrun problems are a frequent method of system attack, resulting in an unwarranted elevation of privilege.  
  
### Generic-Text Routine Mappings  
  
|Tchar.h routine|_UNICODE and _MBCS not defined|_MBCS defined|_UNICODE defined|  
|---------------------|--------------------------------------|--------------------|-----------------------|  
|`_tccpy`|Maps to macro or inline function|`_mbccpy`|Maps to macro or inline function|  
|`_tccpy_l`|n/a|`_mbccpy_l`|n/a|  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`_mbccpy`|<mbctype.h>|  
|`_mbccpy_l`|<mbctype.h>|  
  
 For more compatibility information, see [Compatibility](../vs140/Compatibility.md).  
  
## NET Framework Equivalent  
 Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).  
  
## See Also  
 [Locale](../vs140/Locale.md)   
 [Interpretation of Multibyte-Character Sequences](../vs140/Interpretation-of-Multibyte-Character-Sequences.md)   
 [_mbclen, mblen, _mblen_l, _mbsnlen, _mbsnlen_l](../vs140/_mbclen--mblen--_mblen_l.md)