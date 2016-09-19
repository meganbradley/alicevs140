---
title: "_ismbclegal, _ismbclegal_l, _ismbcsymbol, _ismbcsymbol_l"
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
  - _ismbclegal_l
  - _ismbclegal
  - _ismbcsymbol
  - _ismbcsymbol_l
apilocation: 
  - msvcr120.dll
  - msvcr90.dll
  - msvcr110.dll
  - msvcr110_clr0400.dll
  - msvcr100.dll
  - msvcrt.dll
  - msvcr80.dll
apitype: DLLExport
ms.assetid: 31bf1ea5-b56f-4e28-b21e-b49a2cf93ffc
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _ismbclegal, _ismbclegal_l, _ismbcsymbol, _ismbcsymbol_l
Checks whether a multibyte character is a legal or symbol character.  
  
> [!IMPORTANT]
>  This API cannot be used in applications that execute in the Windows Runtime. For more information, see [CRT functions not supported with /ZW](http://msdn.microsoft.com/library/windows/apps/jj606124.aspx).  
  
## Syntax  
  
```  
int _ismbclegal(  
   unsigned int c   
);  
int _ismbclegal_l(  
   unsigned int c,   
   _locale_t locale  
);  
int _ismbcsymbol(  
   unsigned int c   
);  
int _ismbcsymbol_l(  
   unsigned int c,  
   _locale_t locale  
);  
```  
  
#### Parameters  
 `c`  
 Character to be tested.  
  
 `locale`  
 Locale to use.  
  
## Return Value  
 Each of these routines returns a nonzero value if the character satisfies the test condition or 0 if it does not. If `c`<= 255 and there is a corresponding `_ismbb` routine (for example, `_ismbcalnum` corresponds to `_ismbbalnum`), the result is the return value of the corresponding `_ismbb` routine.  
  
## Remarks  
 Each of these functions tests a given multibyte character for a given condition.  
  
 The versions of these functions with the `_l` suffix are identical except that they use the locale passed in instead of the current locale for their locale-dependent behavior. For more information, see [Locale](../vs140/Locale.md).  
  
|Routine|Test condition|Code page 932 example|  
|-------------|--------------------|---------------------------|  
|`_ismbclegal`|Valid multibyte|Returns nonzero if and only if the first byte of `c` is within ranges 0x81 – 0x9F or 0xE0 – 0xFC, while the second byte is within ranges 0x40 - 0x7E or 0x80 - FC.|  
|`_ismbcsymbol`|Multibyte symbol|Returns nonzero if and only if 0x8141<=`c`<=0x81AC.|  
  
### Generic-Text Routine Mappings  
  
|Tchar.h routine|_UNICODE and _MBCS not defined|_MBCS defined|_UNICODE defined|  
|---------------------|--------------------------------------|--------------------|-----------------------|  
|`_istlegal`|Always returns false|`_ismbclegal`|Always returns false.|  
|`_istlegal_l`|Always returns false|`_ismbclegal_l`|Always returns false.|  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`_ismbclegal,_ismbclegal_l`|<mbstring.h>|  
|`_ismbcsymbol,_ismbcsymbol_l`|<mbstring.h>|  
  
 For more compatibility information, see [Compatibility](../vs140/Compatibility.md).  
  
## .NET Framework Equivalent  
 Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).  
  
## See Also  
 [Character Classification](../vs140/Character-Classification.md)   
 [_ismbc Routines](../vs140/_ismbc-Routines.md)   
 [is, isw Routines](../vs140/is--isw-Routines.md)   
 [_ismbb Routines](../vs140/_ismbb-Routines.md)