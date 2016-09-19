---
title: "ispunct, iswpunct, _ispunct_l, _iswpunct_l"
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
  - ispunct
  - _iswpunct_l
  - iswpunct
  - _ispunct_l
apilocation: 
  - msvcr110.dll
  - msvcrt.dll
  - msvcr80.dll
  - msvcr100.dll
  - msvcr110_clr0400.dll
  - msvcr90.dll
  - msvcr120.dll
apitype: DLLExport
ms.assetid: 94403240-85c8-40a4-9c2b-e3e95c729c76
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ispunct, iswpunct, _ispunct_l, _iswpunct_l
Determines whether an integer represents a punctuation character.  
  
## Syntax  
  
```  
int ispunct(  
   int c   
);  
int iswpunct(  
   wint_t c   
);  
int _ispunct_l(  
   int c,  
   _locale_t locale  
);  
int _iswpunct_l(  
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
 Each of these routines returns nonzero if `c` is a particular representation of a punctuation character. `ispunct` returns a nonzero value for any printable character that is not a space character or a character for which `isalnum` is nonzero. `iswpunct` returns a nonzero value for any printable wide character that is neither the space wide character nor a wide character for which `iswalnum` is nonzero. Each of these routines returns 0 if `c` does not satisfy the test condition.  
  
 The result of the test condition for the `ispunct` function depends on the `LC_CTYPE` category setting of the locale; see [setlocale, _wsetlocale](../vs140/setlocale--_wsetlocale.md) for more information. The versions of these functions that do not have the `_l` suffix use the current locale for any locale-dependent behavior; the versions that do have the `_l` suffix are identical except that they use the locale that's passed in instead. For more information, see [Locale](../vs140/Locale.md).  
  
 The behavior of `ispunct` and `_ispunct_l` is undefined if `c` is not EOF or in the range 0 through 0xFF, inclusive. When a debug CRT library is used and `c` is not one of these values, the functions raise an assertion.  
  
### Generic-Text Routine Mappings  
  
|TCHAR.H routine|_UNICODE & _MBCS not defined|_MBCS defined|_UNICODE defined|  
|---------------------|------------------------------------|--------------------|-----------------------|  
|**_** `istpunct`|`ispunct`|[_ismbcpunct](../vs140/_ismbcgraph--_ismbcgraph_l--_ismbcprint--_ismbcprint_l--_ismbcpunct--_ismbcpunct_l--_ismbcblank--_ismbcblank_l--_ismbcspace--_ismbcspace_l.md)|`iswpunct`|  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`ispunct`|<ctype.h>|  
|`iswpunct`|<ctype.h> or <wchar.h>|  
|`_ispunct_l`|<ctype.h>|  
|`_iswpunct_l`|<ctype.h> or <wchar.h>|  
  
 For additional compatibility information, see [Compatibility](../vs140/Compatibility.md).  
  
## See Also  
 [Character Classification](../vs140/Character-Classification.md)   
 [Locale](../vs140/Locale.md)   
 [is, isw Routines](../vs140/is--isw-Routines.md)