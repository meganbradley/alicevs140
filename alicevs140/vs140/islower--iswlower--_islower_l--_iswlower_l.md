---
title: "islower, iswlower, _islower_l, _iswlower_l"
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
  - iswlower
  - _islower_l
  - islower
  - _iswlower_l
apilocation: 
  - msvcr100.dll
  - msvcr110_clr0400.dll
  - msvcr110.dll
  - msvcrt.dll
  - msvcr120.dll
  - msvcr90.dll
  - msvcr80.dll
apitype: DLLExport
ms.assetid: fcc3b70a-2b47-45fd-944d-e5c1942e6457
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# islower, iswlower, _islower_l, _iswlower_l
Determines whether an integer represents a lowercase character.  
  
## Syntax  
  
```  
int islower(  
   int c   
);  
int iswlower(  
   wint_t c   
);  
int islower_l(  
   int c,  
   _locale_t locale  
);  
int _iswlower_l(  
   wint_t c,  
   _locale_t locale  
);  
```  
  
#### Parameters  
 `c`  
 Integer to test.  
  
 `locale`  
 Locale to use.  
  
## Return Value  
 Each of these routines returns nonzero if `c` is a particular representation of a lowercase character. `islower` returns a nonzero value if `c` is a lowercase character (a – z). `iswlower` returns a nonzero value if `c` is a wide character that corresponds to a lowercase letter, or if `c` is one of an implementation-defined set of wide characters for which none of `iswcntrl`, `iswdigit`, `iswpunct`, or `iswspace` is nonzero. Each of these routines returns 0 if `c` does not satisfy the test condition.  
  
 The versions of these functions that have the `_l` suffix use the locale that's passed in instead of the current locale for their locale-dependent behavior. For more information, see [Locale](../vs140/Locale.md).  
  
 The behavior of `islower` and `_islower_l` is undefined if `c` is not EOF or in the range 0 through 0xFF, inclusive. When a debug CRT library is used and `c` is not one of these values, the functions raise an assertion.  
  
### Generic-Text Routine Mappings  
  
|TCHAR.H routine|_UNICODE & _MBCS not defined|_MBCS defined|_UNICODE defined|  
|---------------------|------------------------------------|--------------------|-----------------------|  
|`_istlower`|`islower`|[_ismbclower](../vs140/_ismbclower--_ismbclower_l--_ismbcupper--_ismbcupper_l.md)|`iswlower`|  
|`_istlower_l`|`_islower _l`|[_ismbclower_l](../vs140/_ismbclower--_ismbclower_l--_ismbcupper--_ismbcupper_l.md)|`_liswlower_l`|  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`islower`|<ctype.h>|  
|`iswlower`|<ctype.h> or <wchar.h>|  
|`_islower_l`|<ctype.h>|  
|`_swlower_l`|<ctype.h> or <wchar.h>|  
  
 For additional compatibility information, see [Compatibility](../vs140/Compatibility.md).  
  
## .NET Framework Equivalent  
 [System::Char::IsLower](https://msdn.microsoft.com/en-us/library/system.char.islower.aspx)  
  
## See Also  
 [Character Classification](../vs140/Character-Classification.md)   
 [Locale](../vs140/Locale.md)   
 [is, isw Routines](../vs140/is--isw-Routines.md)