---
title: "___setlc_active_func, ___unguarded_readlc_active_add_func"
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
  - ___setlc_active_func
  - ___unguarded_readlc_active_add_func
apilocation: 
  - msvcr90.dll
  - msvcr110_clr0400.dll
  - msvcrt.dll
  - msvcr110.dll
  - msvcr80.dll
  - msvcr120.dll
  - msvcr100.dll
apitype: DLLExport
ms.assetid: 605ec4e3-81e5-4ece-935a-f434768cc702
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ___setlc_active_func, ___unguarded_readlc_active_add_func
OBSOLETE. The CRT exports these internal functions only to preserve binary compatibility.  
  
## Syntax  
  
```cpp  
int ___setlc_active_func(void);  
int * ___unguarded_readlc_active_add_func(void);  
```  
  
## Return Value  
 The value returned is not significant.  
  
## Remarks  
 Although the internal CRT functions `___setlc_active_func` and `___unguarded_readlc_active_add_func` are obsolete and no longer used, they are exported by the CRT library to preserve binary compatibility. The original purpose of `___setlc_active_func` was to return the number of currently active calls to the `setlocale` function. The original purpose of `___unguarded_readlc_active_add_func` was to return the number of functions that referenced the locale without locking it.  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`___setlc_active_func`, `___unguarded_readlc_active_add_func`|none|  
  
## See Also  
 [setlocale, _wsetlocale](../vs140/setlocale--_wsetlocale.md)