---
title: "_ismbchira, _ismbchira_l, _ismbckata, _ismbckata_l"
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
  - _ismbckata
  - _ismbchira_l
  - _ismbchira
  - _ismbckata_l
apilocation: 
  - msvcr110.dll
  - msvcr120.dll
  - msvcrt.dll
  - msvcr100.dll
  - msvcr80.dll
  - msvcr110_clr0400.dll
  - msvcr90.dll
apitype: DLLExport
ms.assetid: 2db388a2-be31-489b-81c8-f6bf3f0582d3
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _ismbchira, _ismbchira_l, _ismbckata, _ismbckata_l
**Code Page 932 Specific functions**  
  
> [!IMPORTANT]
>  This API cannot be used in applications that execute in the Windows Runtime. For more information, see [CRT functions not supported with /ZW](http://msdn.microsoft.com/library/windows/apps/jj606124.aspx).  
  
## Syntax  
  
```  
int _ismbchira(  
   unsigned int c   
);  
int _ismbchira_l(  
   unsigned int c,  
   _locale_t locale  
);  
int _ismbckata(  
   unsigned int c   
);  
int _ismbckata_l(  
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
 Each of these routines returns a nonzero value if the character satisfies the test condition or 0 if it does not. If `c` <= 255 and there is a corresponding `_ismbb` routine (for example, `_ismbcalnum` corresponds to `_ismbbalnum`), the result is the return value of the corresponding `_ismbb` routine.  
  
## Remarks  
 Each of these functions tests a given multibyte character for a given condition.  
  
 The versions of these functions with the `_l` suffix are identical except that they use the locale passed in instead of the current locale for their locale-dependent behavior. For more information, see [Locale](../vs140/Locale.md).  
  
|Routine|Test condition (code page 932 only)|  
|-------------|-------------------------------------------|  
|`_ismbchira`|Double-byte Hiragana: 0x829F<=`c`<=0x82F1.|  
|`_ismbchira_l`|Double-byte Hiragana: 0x829F<=`c`<=0x82F1.|  
|`_ismbckata`|Double-byte katakana: 0x8340<=`c`<=0x8396.|  
|`_ismbckata_l`|Double-byte katakana: 0x8340<=`c`<=0x8396.|  
  
 **End Code Page 932 Specific**  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`_ismbchira`|<mbstring.h>|  
|`_ismbchira_l`|<mbstring.h>|  
|`_ismbckata`|<mbstring.h>|  
|`_ismbckata_l`|<mbstring.h>|  
  
 For more compatibility information, see [Compatibility](../vs140/Compatibility.md).  
  
## .NET Framework Equivalent  
 Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).  
  
## See Also  
 [Character Classification](../vs140/Character-Classification.md)   
 [_ismbc Routines](../vs140/_ismbc-Routines.md)   
 [is, isw Routines](../vs140/is--isw-Routines.md)   
 [Locale](../vs140/Locale.md)   
 [Interpretation of Multibyte-Character Sequences](../vs140/Interpretation-of-Multibyte-Character-Sequences.md)