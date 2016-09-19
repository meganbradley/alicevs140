---
title: "_get_current_locale"
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
  - _get_current_locale
apilocation: 
  - msvcr120.dll
  - msvcr110_clr0400.dll
  - msvcrt.dll
  - msvcr110.dll
  - msvcr90.dll
  - msvcr100.dll
  - msvcr80.dll
apitype: DLLExport
ms.assetid: 572217f2-a37a-4105-a293-a250b4fabd99
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _get_current_locale
Gets a locale object representing the current locale.  
  
## Syntax  
  
```  
_locale_t _get_current_locale(void);  
```  
  
## Return Value  
 A locale object representing the current locale.  
  
## Remarks  
 The `_get_current_locale`function gets the currently set locale for the thread and returns a locale object representing that locale.  
  
 The previous name of this function, `__get_current_locale` (with two leading underscores) has been deprecated.  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`_get_current_locale`|<locale.h>|  
  
 For more compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## .NET Framework Equivalent  
 No equivalent.  
  
## See Also  
 [setlocale, _wsetlocale](../vs140/setlocale--_wsetlocale.md)   
 [_create_locale](../vs140/_create_locale--_wcreate_locale.md)   
 [_free_locale](../vs140/_free_locale.md)