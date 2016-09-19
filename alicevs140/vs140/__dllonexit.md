---
title: "__dllonexit"
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
  - __dllonexit
apilocation: 
  - msvcrt.dll
  - msvcr110.dll
  - msvcr110_clr0400.dll
  - msvcr100.dll
  - msvcr80.dll
  - msvcr120.dll
  - msvcr90.dll
  - msvcr120_clr0400.dll
apitype: DLLExport
ms.assetid: 708f2ceb-f95c-46b0-a58d-d68b3fa36f12
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# __dllonexit
Registers a routine to be called at exit time.  
  
## Syntax  
  
```  
_onexit_t __dllonexit(   _onexit_t func,  
   _PVFV **  pbegin,   
   _PVFV **  pend   
   )  
```  
  
#### Parameters  
 `func`  
 Pointer to a function to be executed upon exit.  
  
 `pbegin`  
 Pointer to a variable that points to the beginning of a list of functions to execute on detach.  
  
 `pend`  
 Pointer to variable that points to the end of a list of functions to execute on detach.  
  
## Return Value  
 If successful, a pointer to the user’s function. Otherwise, a NULL pointer.  
  
## Remarks  
 The `__dllonexit` function is analogous to the [_onexit](../vs140/_onexit--_onexit_m.md) function except that the global variables used by that function are not visible to this routine. Instead of global variables, this function uses the `pbegin` and `pend` parameters.  
  
 The `_onexit` and `atexit` functions in a DLL linked with MSVCRT.LIB must maintain their own atexit/_onexit list. This routine is the worker that gets called by such DLLs.  
  
 The `_PVFV` type is defined as `typedef void (__cdecl *_PVFV)(void)`.  
  
## Requirements  
  
|Routine|Required file|  
|-------------|-------------------|  
|__dllonexit|onexit.c|  
  
## See Also  
 [_onexit, _onexit_m](../vs140/_onexit--_onexit_m.md)