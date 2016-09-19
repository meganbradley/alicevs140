---
title: "_ismbcgraph, _ismbcgraph_l, _ismbcprint, _ismbcprint_l, _ismbcpunct, _ismbcpunct_l, _ismbcblank, _ismbcblank_l, _ismbcspace, _ismbcspace_l"
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
  - _ismbcpunct_l
  - _ismbcblank
  - _ismbcprint
  - _ismbcgraph_l
  - _ismbcblank_l
  - _ismbcpunct
  - _ismbcprint_l
  - _ismbcspace_l
  - _ismbcspace
  - _ismbcgraph
apilocation: 
  - msvcr100.dll
  - msvcr90.dll
  - msvcr80.dll
  - msvcrt.dll
  - msvcr110_clr0400.dll
  - msvcr120.dll
  - msvcr110.dll
apitype: DLLExport
ms.assetid: 8e0a5f47-ba64-4411-92a3-3c525d16e3be
caps.latest.revision: 23
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _ismbcgraph, _ismbcgraph_l, _ismbcprint, _ismbcprint_l, _ismbcpunct, _ismbcpunct_l, _ismbcblank, _ismbcblank_l, _ismbcspace, _ismbcspace_l
Determines whether character is a graphical character, a display character, a punctuation character, or a space character.  
  
> [!IMPORTANT]
>  This API cannot be used in applications that execute in the [!INCLUDE[wrt](../vs140/includes/wrt_md.md)]. For more information, see[CRT functions not supported with /ZW](http://msdn.microsoft.com/library/windows/apps/jj606124.aspx).  
  
## Syntax  
  
```  
int _ismbcgraph(  
   unsigned int c   
);  
int _ismbcgraph_l(  
   unsigned int c,  
   _locale_t locale   
);  
int _ismbcprint(  
   unsigned int c   
);  
int _ismbcprint_l(  
   unsigned int c,  
   _locale_t locale  
);  
int _ismbcpunct(  
   unsigned int c  
);  
int _ismbcpunct_l(  
   unsigned int c,  
   _locale_t locale  
);  
int _ismbcblank(  
   unsigned int c   
);  
int _ismbcblank_l(  
   unsigned int c,  
   _locale_t locale  
);  
int _ismbcspace(  
   unsigned int c   
);  
int _ismbcspace_l(  
   unsigned int c,  
   _locale_t locale  
);  
```  
  
#### Parameters  
 `c`  
 Character to be determined.  
  
 `locale`  
 Locale to use.  
  
## Return Value  
 Each of these routines returns a nonzero value if the character satisfies the test condition, or 0 if it does not. If `c` <= 255 and there is a corresponding `_ismbb` routine (for example, `_ismbcalnum` corresponds to `_ismbbalnum`), the result is the return value of the corresponding `_ismbb` routine.  
  
 The versions of these functions are identical, except that the ones that have the `_l` suffix use the locale that's passed in for their locale-dependent behavior, instead of the current locale. For more information, see [Locale](../vs140/Locale.md).  
  
## Remarks  
 Each of these functions tests a given multibyte character for a given condition.  
  
|Routine|Test condition|Code page 932 example|  
|-------------|--------------------|---------------------------|  
|`_ismbcgraph`|Graphic|Returns nonzero if and only if `c` is a single-byte representation of any ASCII or katakana printable character except a white space ( ).|  
|`_ismbcprint`|Printable|Returns nonzero if and only if `c` is a single-byte representation of any ASCII or katakana printable character including a white space ( ).|  
|`_ismbcpunct`|Punctuation|Returns nonzero if and only if `c` is a single-byte representation of any ASCII or katakana punctuation character.|  
|`_ismbcblank`|Space or horizontal tab|Returns nonzero if and only if `c` is a space or horizontal tab character: `c`=0x20 or `c`=0x09.|  
|`_ismbcspace`|White space|Returns nonzero if and only if `c` is a white-space character: `c`=0x20 or 0x09<=`c`<=0x0D.|  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`_ismbcgraph`|<mbstring.h>|  
|`_ismbcgraph_l`|<mbstring.h>|  
|`_ismbcprint`|<mbstring.h>|  
|`_ismbcprint_l`|<mbstring.h>|  
|`_ismbcpunct`|<mbstring.h>|  
|`_ismbcpunct_l`|<mbstring.h>|  
|`_ismbcblank`|<mbstring.h>|  
|`_ismbcblank_l`|<mbstring.h>|  
|`_ismbcspace`|<mbstring.h>|  
|`_ismbcspace_l`|<mbstring.h>|  
  
 For more compatibility information, see [Compatibility](../vs140/Compatibility.md).  
  
## Libraries  
 All versions of the [C run-time libraries](../vs140/CRT-Library-Features.md).  
  
## .NET Framework Equivalent  
  
-   [System::Char::IsPunctuation](https://msdn.microsoft.com/en-us/library/system.char.ispunctuation.aspx)  
  
-   [System::Char::IsWhiteSpace](https://msdn.microsoft.com/en-us/library/system.char.iswhitespace.aspx)  
  
-   For `_ismbcgraph` and `_ismbcprint`: Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).  
  
## See Also  
 [Character Classification](../vs140/Character-Classification.md)   
 [Locale](../vs140/Locale.md)   
 [Interpretation of Multibyte-Character Sequences](../vs140/Interpretation-of-Multibyte-Character-Sequences.md)   
 [_ismbc Routines](../vs140/_ismbc-Routines.md)   
 [is, isw Routines](../vs140/is--isw-Routines.md)   
 [_ismbb Routines](../vs140/_ismbb-Routines.md)