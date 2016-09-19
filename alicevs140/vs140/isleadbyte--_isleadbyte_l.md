---
title: "isleadbyte, _isleadbyte_l"
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
  - _isleadbyte_l
  - isleadbyte
apilocation: 
  - msvcr110_clr0400.dll
  - msvcr80.dll
  - msvcr100.dll
  - msvcr110.dll
  - msvcr120.dll
  - msvcrt.dll
  - msvcr90.dll
apitype: DLLExport
ms.assetid: 3b2bcf09-d82b-4803-9e80-59d04942802a
caps.latest.revision: 22
translation.priority.mt: 
  - de-de
  - ja-jp
---
# isleadbyte, _isleadbyte_l
Determines whether a character is the lead byte of a multibyte character.  
  
> [!IMPORTANT]
>  This API cannot be used in applications that execute in the Windows Runtime. For more information, see                  [CRT functions not supported with /ZW](http://msdn.microsoft.com/library/windows/apps/jj606124.aspx).  
  
## Syntax  
  
```  
int isleadbyte(  
   int c   
);  
int _isleadbyte_l(  
   int c   
);  
```  
  
#### Parameters  
 `c`  
 Integer to test.  
  
## Return Value  
 `isleadbyte` returns a nonzero value if the argument satisfies the test condition or 0 if it does not. In the "C" locale and in single-byte character set (SBCS) locales, `isleadbyte` always returns 0.  
  
## Remarks  
 The `isleadbyte` macro returns a nonzero value if its argument is the first byte of a multibyte character. `isleadbyte` produces a meaningful result for any integer argument from –1 (`EOF`) to `UCHAR_MAX` (0xFF), inclusive.  
  
 The expected argument type of `isleadbyte` is `int`; if a signed character is passed, the compiler may convert it to an integer by sign extension, yielding unpredictable results.  
  
 The version of this function with the `_l` suffix is identical except that it uses the locale passed in instead of the current locale for its locale-dependent behavior.  
  
### Generic-Text Routine Mappings  
  
|TCHAR.H routine|_UNICODE & _MBCS not defined|_MBCS defined|_UNICODE defined|  
|---------------------|------------------------------------|--------------------|-----------------------|  
|`_istleadbyte`|Always returns false|**_** `isleadbyte`|Always returns false|  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`isleadbyte`|<ctype.h>|  
|`_isleadbyte_l`|<ctype.h>|  
  
 For additional compatibility information, see [Compatibility](../vs140/Compatibility.md).  
  
## .NET Framework Equivalent  
 Not applicable, but see [System::Globalization::CultureInfo](https://msdn.microsoft.com/en-us/library/system.globalization.cultureinfo.aspx).  
  
## See Also  
 [Byte Classification](../vs140/Byte-Classification.md)   
 [Locale](../vs140/Locale.md)   
 [_ismbb Routines](../vs140/_ismbb-Routines.md)