---
title: "isprint, iswprint, _isprint_l, _iswprint_l"
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
  - iswprint
  - isprint
  - _isprint_l
  - _iswprint_l
apilocation: 
  - msvcr80.dll
  - msvcr110_clr0400.dll
  - msvcr90.dll
  - msvcr110.dll
  - msvcr100.dll
  - msvcrt.dll
  - msvcr120.dll
apitype: DLLExport
ms.assetid: a8bbcdb0-e8d0-4d8c-ae4e-56d3bdee6ca3
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# isprint, iswprint, _isprint_l, _iswprint_l
Determines whether an integer represents a printable character.  
  
## Syntax  
  
```  
int isprint(  
   int c   
);  
int iswprint(  
   wint_t c   
);  
int _isprint_l(  
   int c,  
   _locale_t locale  
);  
int _iswprint_l(  
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
 Each of these routines returns nonzero if `c` is a particular representation of a printable character. `isprint` returns a nonzero value if `c` is a printable character—this includes the space character (0x20 – 0x7E). `iswprint` returns a nonzero value if `c` is a printable wide character—this includes the space wide character. Each of these routines returns 0 if `c` does not satisfy the test condition.  
  
 The result of the test condition for these functions depends on the `LC_CTYPE` category setting of the locale; see [setlocale, _wsetlocale](../vs140/setlocale--_wsetlocale.md) for more information. The versions of these functions that do not have the `_l` suffix use the current locale for any locale-dependent behavior; the versions that do have the `_l` suffix are identical except that they use the locale that's passed in instead. For more information, see [Locale](../vs140/Locale.md).  
  
 The behavior of `isprint` and `_isprint_l` is undefined if `c` is not EOF or in the range 0 through 0xFF, inclusive. When a debug CRT library is used and `c` is not one of these values, the functions raise an assertion.  
  
### Generic-Text Routine Mappings  
  
|TCHAR.H routine|_UNICODE & _MBCS not defined|_MBCS defined|_unicode defined|  
|---------------------|------------------------------------|--------------------|-----------------------|  
|**_** `istprint`|`isprint`|[_ismbcprint](../vs140/_ismbcgraph--_ismbcgraph_l--_ismbcprint--_ismbcprint_l--_ismbcpunct--_ismbcpunct_l--_ismbcblank--_ismbcblank_l--_ismbcspace--_ismbcspace_l.md)|`iswprint`|  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`isprint`|<ctype.h>|  
|`iswprint`|<ctype.h> or <wchar.h>|  
|`_isprint_l`|<ctype.h>|  
|`_iswprint_l`|<ctype.h> or <wchar.h>|  
  
 For additional compatibility information, see [Compatibility](../vs140/Compatibility.md).  
  
## .NET Framework Equivalent  
 Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).  
  
## See Also  
 [Character Classification](../vs140/Character-Classification.md)   
 [Locale](../vs140/Locale.md)   
 [is, isw Routines](../vs140/is--isw-Routines.md)