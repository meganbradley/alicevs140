---
title: "isascii, __isascii, iswascii"
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
  - iswascii
  - __isascii
apilocation: 
  - msvcr90.dll
  - msvcr120.dll
  - msvcr110_clr0400.dll
  - msvcrt.dll
  - msvcr80.dll
  - msvcr100.dll
  - msvcr110.dll
  - ntdll.dll
  - api-ms-win-crt-string-l1-1-0.dll
apitype: DLLExport
ms.assetid: ba4325ad-7cb3-4fb9-b096-58906d67971a
caps.latest.revision: 24
translation.priority.mt: 
  - de-de
  - ja-jp
---
# isascii, __isascii, iswascii
Determines whether a particular character is an ASCII character.  
  
## Syntax  
  
```  
int __isascii(   
   int c   
);  
int iswascii(   
   wint_t c   
);  
#define isascii __isascii  
```  
  
#### Parameters  
 `c`  
 Integer to test.  
  
## Return Value  
 Each of these routines returns nonzero if `c` is a particular representation of an ASCII character. `__isascii` returns a nonzero value if `c` is an ASCII character (in the range 0x00 – 0x7F). `iswascii` returns a nonzero value if `c` is a wide-character representation of an ASCII character. Each of these routines returns 0 if `c` does not satisfy the test condition.  
  
## Remarks  
 Both `__isascii` and `iswascii` are implemented as macros unless the preprocessor macro _CTYPE_DISABLE_MACROS is defined.  
  
 For backward compatibility, `isascii` is implemented as a macro only if [__STDC\_\_](../vs140/Predefined-Macros.md) is not defined or is defined as 0; otherwise it is undefined.  
  
### Generic-Text Routine Mappings  
  
|Tchar.h routine|_UNICODE and _MBCS not defined|_MBCS defined|_UNICODE defined|  
|---------------------|--------------------------------------|--------------------|-----------------------|  
|`_istascii`|`__isascii`|`__isascii`|`iswascii`|  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`isascii`, `__isascii`|C: <ctype.h><br /><br /> C++: <cctype\> or <ctype.h>|  
|`iswascii`|C: <wctype.h>, <ctype.h>, or <wchar.h><br /><br /> C++: <cwctype\>, <cctype\>, <wctype.h>, <ctype.h>, or <wchar.h>|  
  
 The `isascii`, `__isascii` and `iswascii` functions are Microsoft specific. For additional compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## See Also  
 [Character Classification](../vs140/Character-Classification.md)   
 [Locale](../vs140/Locale.md)   
 [is, isw Routines](../vs140/is--isw-Routines.md)