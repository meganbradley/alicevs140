---
title: "isdigit, iswdigit, _isdigit_l, _iswdigit_l"
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
  - _isdigit_l
  - iswdigit
  - _iswdigit_l
  - isdigit
apilocation: 
  - msvcr110_clr0400.dll
  - msvcr110.dll
  - msvcr120.dll
  - msvcr80.dll
  - msvcrt.dll
  - msvcr90.dll
  - msvcr100.dll
apitype: DLLExport
ms.assetid: 350b0093-843a-47b0-954e-c1776e8a3853
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# isdigit, iswdigit, _isdigit_l, _iswdigit_l
Determines whether an integer represents a decimal-digit character.  
  
## Syntax  
  
```  
int isdigit(   
   int c   
);  
int iswdigit(   
   wint_t c   
);  
int _isdigit_l(   
   int c,  
   _locale_t locale  
);  
int _iswdigit_l(   
   wint_t c,  
   _locale_t locale  
);  
```  
  
#### Parameters  
 `c`  
 Integer to test.  
  
 `locale`  
 The locale to use.  
  
## Return Value  
 Each of these routines returns nonzero if `c` is a particular representation of a decimal-digit character. `isdigit` returns a nonzero value if `c` is a decimal digit (0 – 9). `iswdigit` returns a nonzero value if `c` is a wide character that corresponds to a decimal-digit character. Each of these routines returns 0 if `c` does not satisfy the test condition.  
  
 The versions of these functions that have the `_l` suffix use the locale that's passed in instead of the current locale for their locale-dependent behavior. For more information, see [Locale](../vs140/Locale.md).  
  
 The behavior of `isdigit` and `_isdigit_l` is undefined if `c` is not EOF or in the range 0 through 0xFF, inclusive. When a debug CRT library is used and `c` is not one of these values, the functions raise an assertion.  
  
### Generic-Text Routine Mappings  
  
|TCHAR.H routine|_UNICODE & _MBCS not defined|_MBCS defined|_UNICODE defined|  
|---------------------|------------------------------------|--------------------|-----------------------|  
|`_istdigit`|`isdigit`|[_ismbcdigit](../vs140/_ismbcalnum--_ismbcalnum_l--_ismbcalpha--_ismbcalpha_l--_ismbcdigit--_ismbcdigit_l.md)|`iswdigit`|  
|`_istdigit_l`|`_isdigit_l`|[_ismbcdigit_l](../vs140/_ismbcalnum--_ismbcalnum_l--_ismbcalpha--_ismbcalpha_l--_ismbcdigit--_ismbcdigit_l.md)|`_iswdigit_l`|  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`isdigit`|<ctype.h>|  
|`iswdigit`|<ctype.h> or <wchar.h>|  
|`_isdigit_l`|<ctype.h>|  
|`_iswdigit_l`|<ctype.h> or <wchar.h>|  
  
 For additional compatibility information, see [Compatibility](../vs140/Compatibility.md).  
  
## .NET Framework Equivalent  
 [System::Char::IsDigit](https://msdn.microsoft.com/en-us/library/system.char.isdigit.aspx)  
  
## See Also  
 [Character Classification](../vs140/Character-Classification.md)   
 [Locale](../vs140/Locale.md)   
 [is, isw Routines](../vs140/is--isw-Routines.md)