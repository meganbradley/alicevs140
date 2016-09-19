---
title: "feupdateenv"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - cpp
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
apiname: 
  - feupdateenv
apitype: HeaderDef
ms.assetid: 3d170042-dfd5-4e4f-a55f-038cf2296cc9
caps.latest.revision: 5
translation.priority.mt: 
  - de-de
  - ja-jp
---
# feupdateenv
Saves the currently raised floating-point exceptions, restores the specified floating-point environment state, and then raises the saved floating-point exceptions.  
  
## Syntax  
  
```  
int feupdateenv(  
   const fenv_t* penv  
);  
```  
  
#### Parameters  
 `penv`  
 Pointer to a `fenv_t` object that contains a floating-point environment as set by a call to [fegetenv](assetId:///61df848d-6ba8-4c6e-be35-216436fe7736) or [feholdexcept](assetId:///c286ace3-ec39-482a-be8b-f998d31003d9). You can also specify the default startup floating-point environment by using the FE_DFL_ENV macro.  
  
## Return Value  
 Returns 0 if all actions completed successfully.        Otherwise, returns a nonzero value.  
  
## Remarks  
 The `feupdateenv` function performs multiple actions. First, it stores the current raised floating-point exception status flags in automatic storage. Then, it sets the current floating-point environment from the value stored in the `fenv_t` object pointed to by `penv`. If `penv` is not FE_DFL_ENV or does not point to a valid `fenv_t` object, subsequent behavior is undefined. Finally, `feupdateenv` raises the locally stored floating-point exceptions.  
  
 To use this function, you must turn off floating-point optimizations that could prevent access by using the `#pragma fenv_access(on)` directive prior to the call. For more information, see [fenv_access](../vs140/fenv_access.md).  
  
## Requirements  
  
|Function|C header|C++ header|  
|--------------|--------------|------------------|  
|`feupdateenv`|<fenv.h>|<cfenv\>|  
  
 For additional compatibility information, see [Compatibility](../vs140/Compatibility.md).  
  
## See Also  
 [fegetenv](../vs140/fegetenv.md)   
 [feclearexcept](../vs140/feclearexcept.md)   
 [feholdexcept](../vs140/feholdexcept.md)   
 [fesetexceptflag](../vs140/fesetexceptflag.md)