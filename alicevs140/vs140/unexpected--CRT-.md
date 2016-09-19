---
title: "unexpected (CRT)"
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
  - unexpected
apilocation: 
  - msvcr80.dll
  - msvcr120.dll
  - msvcr100.dll
  - msvcr110.dll
  - msvcr90.dll
  - msvcrt.dll
  - msvcr110_clr0400.dll
apitype: DLLExport
ms.assetid: 2f873763-15ad-4556-a924-dcf28f2b52b4
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# unexpected (CRT)
Calls `terminate` or function you specify using `set_unexpected`.  
  
## Syntax  
  
```  
void unexpected( void );  
```  
  
## Remarks  
 The `unexpected` routine is not used with the current implementation of C++ exception handling. `unexpected` calls `terminate` by default. You can change this default behavior by writing a custom termination function and calling `set_unexpected` with the name of your function as its argument. `unexpected` calls the last function given as an argument to `set_unexpected`.  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`unexpected`|<eh.h>|  
  
 For additional compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## .NET Framework Equivalent  
 [System::Exception Class](https://msdn.microsoft.com/en-us/library/system.exception.aspx)  
  
## See Also  
 [Exception Handling Routines](../vs140/Exception-Handling-Routines.md)   
 [abort](../vs140/abort.md)   
 [_set_se_translator](../vs140/_set_se_translator.md)   
 [set_terminate](../vs140/set_terminate--CRT-.md)   
 [set_unexpected](../vs140/set_unexpected--CRT-.md)   
 [terminate](../vs140/terminate--CRT-.md)