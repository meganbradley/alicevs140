---
title: "set_terminate (CRT)"
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
  - set_terminate
apilocation: 
  - msvcrt.dll
  - msvcr110_clr0400.dll
  - msvcr100.dll
  - msvcr110.dll
  - msvcr80.dll
  - msvcr120.dll
  - msvcr90.dll
apitype: DLLExport
ms.assetid: 3ff1456a-7898-44bc-9266-a328a80b6006
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# set_terminate (CRT)
Installs your own termination routine to be called by `terminate`.  
  
## Syntax  
  
```  
terminate_function set_terminate(  
   terminate_function termFunction  
);  
```  
  
#### Parameters  
 `termFunction`  
 Pointer to a terminate function that you write.  
  
## Return Value  
 Returns a pointer to the previous function registered by `set_terminate` so that the previous function can be restored later. If no previous function has been set, the return value may be used to restore the default behavior; this value may be NULL.  
  
## Remarks  
 The `set_terminate` function installs `termFunction` as the function called by `terminate`. `set_terminate` is used with C++ exception handling and may be called at any point in your program before the exception is thrown. `terminate` calls `abort` by default. You can change this default by writing your own termination function and calling `set_terminate` with the name of your function as its argument. `terminate` calls the last function given as an argument to `set_terminate`. After performing any desired cleanup tasks, `termFunction` should exit the program. If it does not exit (if it returns to its caller), `abort` is called.  
  
 In a multithreaded environment, terminate functions are maintained separately for each thread. Each new thread needs to install its own terminate function. Thus, each thread is in charge of its own termination handling.  
  
 The `terminate_function` type is defined in EH.H as a pointer to a user-defined termination function, `termFunction` that returns `void`. Your custom function `termFunction` can take no arguments and should not return to its caller. If it does, `abort` is called. An exception may not be thrown from within `termFunction`.  
  
```  
typedef void ( *terminate_function )( );  
```  
  
> [!NOTE]
>  The `set_terminate` function only works outside the debugger.  
  
 There is a single `set_terminate` handler for all dynamically linked DLLs or EXEs; even if you call `set_terminate` your handler may be replaced by another, or you may be replacing a handler set by another DLL or EXE.  
  
 This function is not supported under **/clr:pure**.  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`set_terminate`|<eh.h>|  
  
 For additional compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## Example  
 See the example for [terminate](../vs140/terminate--CRT-.md).  
  
## .NET Framework Equivalent  
 Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).  
  
## See Also  
 [Exception Handling Routines](../vs140/Exception-Handling-Routines.md)   
 [abort](../vs140/abort.md)   
 [_get_terminate](../vs140/_get_terminate.md)   
 [set_unexpected](../vs140/set_unexpected--CRT-.md)   
 [terminate](../vs140/terminate--CRT-.md)   
 [unexpected](../vs140/unexpected--CRT-.md)