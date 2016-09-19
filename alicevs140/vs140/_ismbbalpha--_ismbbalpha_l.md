---
title: "_ismbbalpha, _ismbbalpha_l"
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
  - _ismbbalpha
  - _ismbbalpha_l
apilocation: 
  - msvcr80.dll
  - msvcr110.dll
  - msvcr110_clr0400.dll
  - msvcr90.dll
  - msvcr100.dll
  - msvcrt.dll
  - msvcr120.dll
apitype: DLLExport
ms.assetid: 8e54cb92-fc2b-41f5-8ab4-b22ac8aa9ad0
caps.latest.revision: 20
translation.priority.mt: 
  - de-de
  - ja-jp
---
# _ismbbalpha, _ismbbalpha_l
Determines whether a specified multibyte character is alpha.  
  
## Syntax  
  
```  
int _ismbbalpha(  
   unsigned int c   
);  
int _ismbbalpha_l(  
   unsigned int c   
);  
```  
  
#### Parameters  
 `c`  
 Integer to be tested.  
  
 `locale`  
 Locale to use.  
  
## Return Value  
 `_ismbbalpha` returns a nonzero value if the expression:  
  
```  
isalpha || _ismbbkalnum  
```  
  
 is nonzero for `c`, or 0 if it is not. `_ismbbalpha` uses the current locale for any locale-dependent character settings. `_ismbbalpha_l` is identical except that it uses the locale passed in.  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`_ismbbalpha`|<mbctype.h>|  
|`_ismbbalpha_l`|<mbctype.h>|  
  
 For more compatibility information, see [Compatibility](../vs140/Compatibility.md).  
  
## Libraries  
 All versions of the [C run-time libraries](../vs140/CRT-Library-Features.md).  
  
## .NET Framework Equivalent  
 Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).  
  
## See Also  
 [Byte Classification](../vs140/Byte-Classification.md)   
 [_ismbb Routines](../vs140/_ismbb-Routines.md)