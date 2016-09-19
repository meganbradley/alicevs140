---
title: "_get_unexpected"
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
  - _get_unexpected
apilocation: 
  - msvcr80.dll
  - msvcr100.dll
  - msvcrt.dll
  - msvcr90.dll
  - msvcr120.dll
  - msvcr110.dll
  - msvcr110_clr0400.dll
apitype: DLLExport
ms.assetid: a5f7a7a0-18e0-485e-953d-db291068a1e8
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _get_unexpected
Returns the termination routine to be called by `unexpected`.  
  
## Syntax  
  
```  
unexpected_function _get_unexpected( void );  
```  
  
## Return Value  
 Returns a pointer to the function registered by [set_unexpected](../vs140/set_unexpected--CRT-.md). If no function has been set, the return value may be used to restore the default behavior; this value may be NULL.  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`_get_unexpected`|<eh.h>|  
  
 For additional compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## .NET Framework Equivalent  
 Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).  
  
## See Also  
 [Exception Handling Routines](../vs140/Exception-Handling-Routines.md)   
 [abort](../vs140/abort.md)   
 [set_terminate](../vs140/set_terminate--CRT-.md)   
 [terminate](../vs140/terminate--CRT-.md)   
 [unexpected](../vs140/unexpected--CRT-.md)