---
title: "_unlock"
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
  - _unlock
apilocation: 
  - msvcrt.dll
  - msvcr100.dll
  - msvcr110_clr0400.dll
  - msvcr110.dll
  - msvcr80.dll
  - msvcr120.dll
  - msvcr90.dll
  - msvcr120_clr0400.dll
apitype: DLLExport
ms.assetid: 2eda2507-a134-4997-aa12-f2f8cb319e14
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _unlock
Releases a multi-thread lock.  
  
> [!IMPORTANT]
>  This function is obsolete. Beginning in Visual Studio 2015, it is not available in the CRT.  
  
## Syntax  
  
```  
void __cdecl _unlock(  
   int locknum  
);  
```  
  
#### Parameters  
 [in] `locknum`  
 The identifier of the lock to release.  
  
## Requirements  
 **Source:** mlock.c  
  
## See Also  
 [Alphabetical Function Reference](../vs140/CRT-Alphabetical-Function-Reference.md)   
 [_lock](../vs140/_lock.md)