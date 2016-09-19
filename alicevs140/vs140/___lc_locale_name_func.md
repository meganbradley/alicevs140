---
title: "___lc_locale_name_func"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
apiname: 
  - ___lc_locale_name_func
apilocation: 
  - msvcrt.dll
  - msvcr110.dll
  - msvcr100.dll
  - msvcr90.dll
  - msvcr120.dll
  - msvcr80.dll
  - msvcr110_clr0400.dll
apitype: DLLExport
ms.assetid: ef858308-872e-43de-95e0-9b1b4084343e
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ___lc_locale_name_func
Internal CRT function. Retrieves the current locale name of the thread.  
  
## Syntax  
  
```cpp  
wchar_t** ___lc_locale_name_func(void);  
```  
  
## Return Value  
 A pointer to a string that contains the current locale name of the thread.  
  
## Remarks  
 `___lc_locale_name_func` is an internal CRT function that is used by other CRT functions to get the current locale name from the thread local storage for CRT data. This information is also available by using the [_get_current_locale](../vs140/_get_current_locale.md) function or the [setlocale, _wsetlocale](../vs140/setlocale--_wsetlocale.md) functions.  
  
 Internal CRT functions are implementation-specific and subject to change with each release. We don't recommend their use in your code.  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`___lc_locale_name_func`|crt\src\setlocal.h|  
  
## See Also  
 [_get_current_locale](../vs140/_get_current_locale.md)   
 [setlocale, _wsetlocale](../vs140/setlocale--_wsetlocale.md)   
 [_create_locale](../vs140/_create_locale--_wcreate_locale.md)   
 [_free_locale](../vs140/_free_locale.md)