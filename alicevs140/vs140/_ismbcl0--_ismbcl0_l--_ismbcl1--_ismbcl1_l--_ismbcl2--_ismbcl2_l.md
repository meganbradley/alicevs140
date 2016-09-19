---
title: "_ismbcl0, _ismbcl0_l, _ismbcl1, _ismbcl1_l, _ismbcl2, _ismbcl2_l"
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
  - _ismbcl2
  - _ismbcl1
  - _ismbcl0
  - _ismbcl2_l
  - _ismbcl1_l
  - _ismbcl0_l
apilocation: 
  - msvcr120.dll
  - msvcr80.dll
  - msvcr110.dll
  - msvcr90.dll
  - msvcr110_clr0400.dll
  - msvcrt.dll
  - msvcr100.dll
apitype: DLLExport
ms.assetid: ee15ebd1-462c-4a43-95f3-6735836d626a
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _ismbcl0, _ismbcl0_l, _ismbcl1, _ismbcl1_l, _ismbcl2, _ismbcl2_l
**Code Page 932 Specific functions**, using the current locale or a specified LC_CTYPE conversion state category.  
  
> [!IMPORTANT]
>  This API cannot be used in applications that execute in the Windows Runtime. For more information, see [CRT functions not supported with /ZW](http://msdn.microsoft.com/library/windows/apps/jj606124.aspx).  
  
## Syntax  
  
```  
int _ismbcl0(  
   unsigned int c   
);  
int _ismbcl0_l(  
   unsigned int c,  
   _locale_t locale  
);  
int _ismbcl1(  
   unsigned int c   
);  
int _ismbcl1_l(  
   unsigned int c ,  
   _locale_t locale  
);  
int _ismbcl2(  
   unsigned int c   
);  
int _ismbcl2_l(  
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
  
 The output value is affected by the setting of the `LC_CTYPE` category setting of the locale; see [setlocale](../vs140/setlocale--_wsetlocale.md) for more information. The versions of these functions without the `_l` suffix use the current locale for this locale-dependent behavior; the versions with the `_l` suffix are identical except that they use the locale parameter passed in instead. For more information, see [Locale](../vs140/Locale.md).  
  
|Routine|Test condition (code page 932 only)|  
|-------------|-------------------------------------------|  
|`_ismbcl0`|JIS non-Kanji: 0x8140<=`c`<=0x889E.|  
|`_ismbcl0_l`|JIS non-Kanji: 0x8140<=`c`<=0x889E.|  
|`_ismbcl1`|JIS level-1: 0x889F<=`c`<=0x9872.|  
|`_ismbcl1_l`|JIS level-1: 0x889F<=`c`<=0x9872.|  
|`_ismbcl2`|JIS level-2: 0x989F<=`c`<=0xEAA4.|  
|`_ismbcl2_l`|JIS level-2: 0x989F<=`c`<=0xEAA4.|  
  
 The functions check that the specified value `c` matches the test conditions described above, but do not check that `c` is a valid multibyte character. If the lower byte is in the ranges 0x00 – 0x3F, 0x7F, or 0xFD – 0xFF, these functions return a nonzero value, indicating that the character satisfies the test condition. Use [_ismbbtrail](../vs140/_ismbbtrail--_ismbbtrail_l.md) to test whether the multibyte character is defined.  
  
 **End Code Page 932 Specific**  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`_ismbcl0`|<mbstring.h>|  
|`_ismbcl0_l`|<mbstring.h>|  
|`_ismbcl1`|<mbstring.h>|  
|`_ismbcl1_l`|<mbstring.h>|  
|`_ismbcl2`|<mbstring.h>|  
|`_ismbcl2_l`|<mbstring.h>|  
  
 For more compatibility information, see [Compatibility](../vs140/Compatibility.md).  
  
## .NET Framework Equivalent  
 Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).  
  
## See Also  
 [Character Classification](../vs140/Character-Classification.md)   
 [_ismbc Routines](../vs140/_ismbc-Routines.md)   
 [is, isw Routines](../vs140/is--isw-Routines.md)