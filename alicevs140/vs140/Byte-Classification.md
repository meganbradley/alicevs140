---
title: "Byte Classification"
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
ms.assetid: 1cb52d71-fb0c-46ca-aad7-6472c1103370
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Byte Classification
Each of these routines tests a specified byte of a multibyte character for satisfaction of a condition. Except where specified otherwise, the output value is affected by the setting of the `LC_CTYPE` category setting of the locale; see [setlocale](../vs140/setlocale--_wsetlocale.md) for more information. The versions of these functions without the `_l` suffix use the current locale for this locale-dependent behavior; the versions with the `_l` suffix are identical except that they use the locale parameter passed in instead.  
  
> [!NOTE]
>  By definition, the ASCII characters between 0 and 127 are a subset of all multibyte-character sets. For example, the Japanese katakana character set includes ASCII as well as non-ASCII characters.  
  
 The predefined constants in the following table are defined in CTYPE.H.  
  
### Multibyte-Character Byte-Classification Routines  
  
|Routine|Byte Test Condition|.NET Framework equivalent|  
|-------------|-------------------------|-------------------------------|  
|[isleadbyte, _isleadbyte_l](../vs140/isleadbyte--_isleadbyte_l.md)|Lead byte; test result depends on `LC_CTYPE` category setting of current locale|Not applicable, but see [System::Globalization::CultureInfo](https://msdn.microsoft.com/en-us/library/system.globalization.cultureinfo.aspx)|  
|[_ismbbalnum, _ismbbalnum_l](../vs140/_ismbbalnum--_ismbbalnum_l.md)|`isalnum &#124;&#124; _ismbbkalnum`|Not applicable, but see [System::Globalization::CultureInfo](https://msdn.microsoft.com/en-us/library/system.globalization.cultureinfo.aspx)|  
|[_ismbbalpha, _ismbbalpha_l](../vs140/_ismbbalpha--_ismbbalpha_l.md)|`isalpha &#124;&#124; _ismbbkalnum`|Not applicable, but see [System::Globalization::CultureInfo](https://msdn.microsoft.com/en-us/library/system.globalization.cultureinfo.aspx)|  
|[_ismbbgraph, _ismbbgraph_l](../vs140/_ismbbgraph--_ismbbgraph_l.md)|Same as `_ismbbprint`, but `_ismbbgraph` does not include the space character (0x20)|Not applicable, but see [System::Globalization::CultureInfo](https://msdn.microsoft.com/en-us/library/system.globalization.cultureinfo.aspx)|  
|[_ismbbkalnum, _ismbbkalnum_l](../vs140/_ismbbkalnum--_ismbbkalnum_l.md)|Non-ASCII text symbol other than punctuation. For example, in code page 932 only, `_ismbbkalnum` tests for katakana alphanumeric|Not applicable, but see [System::Globalization::CultureInfo](https://msdn.microsoft.com/en-us/library/system.globalization.cultureinfo.aspx)|  
|[_ismbbkana, _ismbbkana_l](../vs140/_ismbbkana--_ismbbkana_l.md)|Katakana (0xA1 – 0xDF), code page 932 only|Not applicable, but see [System::Globalization::CultureInfo](https://msdn.microsoft.com/en-us/library/system.globalization.cultureinfo.aspx)|  
|[_ismbbkprint, _ismbbkprint_l](../vs140/_ismbbkprint--_ismbbkprint_l.md)|Non-ASCII text or non-ASCII punctuation symbol. For example, in code page 932 only, `_ismbbkprint` tests for katakana alphanumeric or katakana punctuation (range: 0xA1 – 0xDF).|Not applicable, but see [System::Globalization::CultureInfo](https://msdn.microsoft.com/en-us/library/system.globalization.cultureinfo.aspx)|  
|[_ismbbkpunct, _ismbbkpunct_l](../vs140/_ismbbkpunct--_ismbbkpunct_l.md)|Non-ASCII punctuation. For example, in code page 932 only, `_ismbbkpunct` tests for katakana punctuation.|Not applicable, but see [System::Globalization::CultureInfo](https://msdn.microsoft.com/en-us/library/system.globalization.cultureinfo.aspx)|  
|[_ismbblead, _ismbblead_l](../vs140/_ismbblead--_ismbblead_l.md)|First byte of multibyte character. For example, in code page 932 only, valid ranges are 0x81 – 0x9F, 0xE0 – 0xFC.|Not applicable, but see [System::Globalization::CultureInfo](https://msdn.microsoft.com/en-us/library/system.globalization.cultureinfo.aspx)|  
|[_ismbbprint, _ismbbprint_l](../vs140/_ismbbprint--_ismbbprint_l.md)|`isprint &#124;&#124; _ismbbkprint. ismbbprint` includes the space character (0x20)|Not applicable, but see [System::Globalization::CultureInfo](https://msdn.microsoft.com/en-us/library/system.globalization.cultureinfo.aspx)|  
|[_ismbbpunct, _ismbbpunct_l](../vs140/_ismbbpunct--_ismbbpunct_l.md)|`ispunct &#124;&#124; _ismbbkpunct`|Not applicable, but see [System::Globalization::CultureInfo](https://msdn.microsoft.com/en-us/library/system.globalization.cultureinfo.aspx)|  
|[_ismbbtrail, _ismbbtrail_l](../vs140/_ismbbtrail--_ismbbtrail_l.md)|Second byte of multibyte character. For example, in code page 932 only, valid ranges are 0x40 – 0x7E, 0x80 – 0xEC.|Not applicable, but see [System::Globalization::CultureInfo](https://msdn.microsoft.com/en-us/library/system.globalization.cultureinfo.aspx)|  
|[_ismbslead, _ismbslead_l](../vs140/_ismbslead--_ismbstrail--_ismbslead_l--_ismbstrail_l.md)|Lead byte (in string context)|Not applicable, but see [System::Globalization::CultureInfo](https://msdn.microsoft.com/en-us/library/system.globalization.cultureinfo.aspx)|  
|[ismbstrail, _ismbstrail_l](../vs140/_ismbslead--_ismbstrail--_ismbslead_l--_ismbstrail_l.md)|Trail byte (in string context)|Not applicable, but see [System::Globalization::CultureInfo](https://msdn.microsoft.com/en-us/library/system.globalization.cultureinfo.aspx)|  
|[_mbbtype, _mbbtype_l](../vs140/_mbbtype--_mbbtype_l.md)|Return byte type based on previous byte|Not applicable, but see [System::Globalization::CultureInfo](https://msdn.microsoft.com/en-us/library/system.globalization.cultureinfo.aspx)|  
|[_mbsbtype, _mbsbtype_l](../vs140/_mbsbtype--_mbsbtype_l.md)|Return type of byte within string|Not applicable, but see [System::Globalization::CultureInfo](https://msdn.microsoft.com/en-us/library/system.globalization.cultureinfo.aspx)|  
|[mbsinit](../vs140/mbsinit.md)|Tracks the state of a multibyte character conversion.|Not applicable, but see [System::Globalization::CultureInfo](https://msdn.microsoft.com/en-us/library/system.globalization.cultureinfo.aspx)|  
  
 The `MB_LEN_MAX` macro, defined in LIMITS.H, expands to the maximum length in bytes that any multibyte character can have. `MB_CUR_MAX`, defined in STDLIB.H, expands to the maximum length in bytes of any multibyte character in the current locale.  
  
## See Also  
 [Run-Time Routines by Category](../vs140/Run-Time-Routines-by-Category.md)