---
title: "_isctype, iswctype, _isctype_l, _iswctype_l"
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
  - _isctype_l
  - iswctype
  - _iswctype_l
  - _isctype
apilocation: 
  - msvcrt.dll
  - msvcr90.dll
  - msvcr110.dll
  - msvcr100.dll
  - msvcr80.dll
  - msvcr110_clr0400.dll
  - msvcr120.dll
apitype: DLLExport
ms.assetid: cf7509b7-12fc-4d95-8140-ad2eb98173d3
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _isctype, iswctype, _isctype_l, _iswctype_l
Tests `c` for the property specified by the `desc` argument. For each valid value of `desc`, there is an equivalent wide-character classification routine.  
  
## Syntax  
  
```  
int _isctype(  
   int c,  
   _ctype_t desc  
);  
int _isctype_l(  
   int c,  
   _ctype_t desc,  
   _locale_t locale  
);  
int iswctype(  
   wint_t c,  
   wctype_t desc   
);  
int _iswctype_l(  
   wint_t c,  
   wctype_t desc,  
   _locale_t locale  
);  
```  
  
#### Parameters  
 `c`  
 Integer to test.  
  
 `desc`  
 Property to test for. This is normally retrieved using ctype or [wctype](../vs140/wctype.md).  
  
 `locale`  
 The locale to use for any locale-dependent tests.  
  
## Return Value  
 `_isctype` and `iswctype` return a nonzero value if `c` has the property specified by `desc` in the current locale or 0 if it does not. The versions of these functions with the `_l` suffix are identical except that they use the locale passed in instead of the current locale for their locale-dependent behavior. For more information, see [Locale](../vs140/Locale.md).  
  
 The behavior of `_isctype` and `_isctype_l` is undefined if `c` is not EOF or in the range 0 through 0xFF, inclusive. When a debug CRT library is used and `c` is not one of these values, the functions raise an assertion.  
  
### Generic-Text Routine Mappings  
  
|Tchar.h routine|_UNICODE and _MBCS not defined|_MBCS defined|_UNICODE defined|  
|---------------------|--------------------------------------|--------------------|-----------------------|  
|`n/a`|`_isctype`|`n/a`|`_iswctype`|  
|`n/a`|`_isctype_l`|`n/a`|`_iswctype_l`|  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`_isctype`|<ctype.h>|  
|`iswctype`|<ctype.h> or <wchar.h>|  
|`_isctype_l`|<ctype.h>|  
|`_iswctype_l`|<ctype.h> or <wchar.h>|  
  
 For more compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## Libraries  
 All versions of the [C run-time libraries](../vs140/CRT-Library-Features.md).  
  
## .NET Framework Equivalent  
 Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).  
  
## See Also  
 [Character Classification](../vs140/Character-Classification.md)   
 [Locale](../vs140/Locale.md)   
 [is, isw Routines](../vs140/is--isw-Routines.md)