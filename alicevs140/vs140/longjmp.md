---
title: "longjmp"
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
  - longjmp
apilocation: 
  - msvcr110.dll
  - msvcrt.dll
  - msvcr110_clr0400.dll
  - msvcr80.dll
  - msvcr120.dll
  - msvcr90.dll
  - msvcr100.dll
apitype: DLLExport
ms.assetid: 0e13670a-5130-45c1-ad69-6862505b7a2f
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# longjmp
Restores stack environment and execution locale.  
  
## Syntax  
  
```  
  
      void longjmp(  
   jmp_buf env,  
   int value   
);  
```  
  
#### Parameters  
 `env`  
 Variable in which environment is stored.  
  
 *value*  
 Value to be returned to `setjmp` call.  
  
## Remarks  
 The `longjmp` function restores a stack environment and execution locale previously saved in `env` by `setjmp`. `setjmp` and `longjmp` provide a way to execute a nonlocal `goto`; they are typically used to pass execution control to error-handling or recovery code in a previously called routine without using the normal call and return conventions.  
  
 A call to `setjmp` causes the current stack environment to be saved in `env`. A subsequent call to `longjmp` restores the saved environment and returns control to the point immediately following the corresponding `setjmp` call. Execution resumes as if *value* had just been returned by the `setjmp` call. The values of all variables (except register variables) that are accessible to the routine receiving control contain the values they had when `longjmp` was called. The values of register variables are unpredictable. The value returned by `setjmp` must be nonzero. If *value* is passed as 0, the value 1 is substituted in the actual return.  
  
 Call `longjmp` before the function that called `setjmp` returns; otherwise the results are unpredictable.  
  
 Observe the following restrictions when using `longjmp`:  
  
-   Do not assume that the values of the register variables will remain the same. The values of register variables in the routine calling `setjmp` may not be restored to the proper values after `longjmp` is executed.  
  
-   Do not use `longjmp` to transfer control out of an interrupt-handling routine unless the interrupt is caused by a floating-point exception. In this case, a program may return from an interrupt handler via `longjmp` if it first reinitializes the floating-point math package by calling `_fpreset`.  
  
     **Note** Be careful when using `setjmp` and `longjmp` in C++ programs. Because these functions do not support C++ object semantics, it is safer to use the C++ exception-handling mechanism.  
  
 For more information, see [Using setjmp and longjmp](../vs140/Using-setjmp-longjmp.md).  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`longjmp`|<setjmp.h>|  
  
 For additional compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## Libraries  
 All versions of the [C run-time libraries](../vs140/CRT-Library-Features.md).  
  
## Example  
 See the example for [_fpreset](../vs140/_fpreset.md).  
  
## .NET Framework Equivalent  
 Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).  
  
## See Also  
 [Process and Environment Control](../vs140/Process-and-Environment-Control.md)   
 [setjmp](../vs140/setjmp.md)