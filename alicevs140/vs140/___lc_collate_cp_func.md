---
title: "___lc_collate_cp_func"
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
  - ___lc_collate_cp_func
apilocation: 
  - msvcr120.dll
  - msvcrt.dll
  - msvcr100.dll
  - msvcr80.dll
  - msvcr110_clr0400.dll
  - msvcr110.dll
  - msvcr90.dll
apitype: DLLExport
ms.assetid: 46ccc084-7ac9-4e5d-9138-e12cb5845615
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ___lc_collate_cp_func
Internal CRT function. Retrieves the current collation code page of the thread.  
  
## Syntax  
  
```cpp  
UINT ___lc_codepage_func(void);  
```  
  
## Return Value  
 The current collation code page of the thread.  
  
## Remarks  
 `___lc_collate_cp_func` is an internal CRT function that is used by other CRT functions to get the current collation code page from the thread local storage for CRT data. This information is also available by using the [_get_current_locale](../vs140/_get_current_locale.md) function.  
  
 Internal CRT functions are implementation-specific and subject to change with each release. We don't recommend their use in your code.  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`___lc_collate_cp_func`|crt\src\setlocal.h|  
  
## See Also  
 [_get_current_locale](../vs140/_get_current_locale.md)   
 [setlocale, _wsetlocale](../vs140/setlocale--_wsetlocale.md)   
 [_create_locale](../vs140/_create_locale--_wcreate_locale.md)   
 [_free_locale](../vs140/_free_locale.md)