---
title: "isalnum, iswalnum, _isalnum_l, _iswalnum_l"
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
  - _iswalnum_l
  - _isalnum_l
  - iswalnum
  - isalnum
apilocation: 
  - msvcrt.dll
  - msvcr110.dll
  - msvcr100.dll
  - msvcr90.dll
  - msvcr110_clr0400.dll
  - msvcr80.dll
  - msvcr120.dll
apitype: DLLExport
ms.assetid: 0dc51306-ade8-4944-af27-e4176fc89093
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# isalnum, iswalnum, _isalnum_l, _iswalnum_l
Determines whether an integer represents an alphanumeric character.  
  
## Syntax  
  
```  
int isalnum(   
   int c   
);  
int iswalnum(   
   wint_t c   
);  
int _isalnum_l(   
   int c,  
   _locale_t locale  
);  
int _iswalnum_l(   
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
 Each of these routines returns nonzero if `c` is a particular representation of an alphanumeric character. `isalnum` returns a nonzero value if either `isalpha` or `isdigit` is nonzero for `c`, that is, if `c` is within the ranges A – Z, a – z, or 0 – 9. `iswalnum` returns a nonzero value if either `iswalpha` or `iswdigit` is nonzero for `c`. Each of these routines returns 0 if `c` does not satisfy the test condition.  
  
 The versions of these functions that have the `_l` suffix use the locale parameter that's passed in instead of the current locale. For more information, see [Locale](../vs140/Locale.md).  
  
 The behavior of `isalnum` and `_isalnum_l` is undefined if `c` is not EOF or in the range 0 through 0xFF, inclusive. When a debug CRT library is used and `c` is not one of these values, the functions raise an assertion.  
  
### Generic-Text Routine Mappings  
  
|TCHAR.H routine|_UNICODE & _MBCS not defined|_MBCS defined|_UNICODE defined|  
|---------------------|------------------------------------|--------------------|-----------------------|  
|`_istalnum`|`isalnum`|[_ismbcalnum](../vs140/_ismbcalnum--_ismbcalnum_l--_ismbcalpha--_ismbcalpha_l--_ismbcdigit--_ismbcdigit_l.md)|`iswalnum`|  
|`_istalnum_l`|`_isalnum_l`|`_ismbcalnum_l`|`_iswalnum_l`|  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`isalnum`|<ctype.h>|  
|`iswalnum`|<ctype.h> or <wchar.h>|  
|`_isalnum_l`|<ctype.h>|  
|`_iswalnum_l`|<ctype.h> or <wchar.h>|  
  
 For additional compatibility information, see [Compatibility](../vs140/Compatibility.md).  
  
## .NET Framework Equivalent  
 [System::Char::IsLetterOrDigit](https://msdn.microsoft.com/en-us/library/system.char.isletterordigit.aspx)  
  
## See Also  
 [Character Classification](../vs140/Character-Classification.md)   
 [Locale](../vs140/Locale.md)   
 [is, isw Routines](../vs140/is--isw-Routines.md)