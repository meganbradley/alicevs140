---
title: "_ismbblead, _ismbblead_l"
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
  - _ismbblead_l
  - _ismbblead
apilocation: 
  - msvcrt.dll
  - msvcr110.dll
  - msvcr110_clr0400.dll
  - msvcr100.dll
  - msvcr80.dll
  - msvcr90.dll
  - msvcr120.dll
apitype: DLLExport
ms.assetid: 2abc6f75-ed5c-472e-bfd0-e905a1835ccf
caps.latest.revision: 23
translation.priority.mt: 
  - de-de
  - ja-jp
---
# _ismbblead, _ismbblead_l
Tests a character to determine whether it is a lead byte of a multibyte character.  
  
## Syntax  
  
```  
int _ismbblead(  
   unsigned int c   
);  
int _ismbblead_l(  
   unsigned int c,  
   _locale_t locale  
);  
```  
  
#### Parameters  
 `c`  
 Integer to be tested.  
  
 `locale`  
 Locale to use.  
  
## Return Value  
 Returns a nonzero value if the integer `c` is the first byte of a multibyte character.  
  
## Remarks  
 Multibyte characters consist of a lead byte followed by a trailing byte. Lead bytes are distinguished by being in a particular range for a given character set. For example, in code page 932 only, lead bytes range from 0x81 – 0x9F and 0xE0 – 0xFC.  
  
 `_ismbblead` uses the current locale for locale-dependent behavior. `_ismbblead_l` is identical except that it uses the locale passed in instead. For more information, see [Locale](../vs140/Locale.md).  
  
### Generic-Text Routine Mappings  
  
|Tchar.h routine|_UNICODE and _MBCS not defined|_MBCS defined|_UNICODE defined|  
|---------------------|--------------------------------------|--------------------|-----------------------|  
|`_istlead`|Always returns false|`_ismbblead`|Always returns false|  
  
## Requirements  
  
|Routine|Required header|Optional header|  
|-------------|---------------------|---------------------|  
|`_ismbblead`|<mbctype.h> or <mbstring.h>|<ctype.h>,* <limits.h>, <stdlib.h>|  
|`_ismbblead_l`|<mbctype.h> or <mbstring.h>|<ctype.h>,* <limits.h>, <stdlib.h>|  
  
 \* For manifest constants for the test conditions.  
  
 For more compatibility information, see [Compatibility](../vs140/Compatibility.md).  
  
## .NET Framework Equivalent  
 Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).  
  
## See Also  
 [Byte Classification](../vs140/Byte-Classification.md)   
 [_ismbb Routines](../vs140/_ismbb-Routines.md)