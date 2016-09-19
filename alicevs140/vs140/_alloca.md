---
title: "_alloca"
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
  - _alloca
apilocation: 
  - msvcr80.dll
  - msvcr110.dll
  - msvcr120.dll
  - msvcrt.dll
  - msvcr90.dll
  - msvcr110_clr0400.dll
  - msvcr100.dll
apitype: DLLExport
ms.assetid: 74488eb1-b71f-4515-88e1-cdd03b6f8225
caps.latest.revision: 23
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _alloca
Allocates memory on the stack. This function is deprecated because a more secure version is available; see [_alloca_s](../vs140/_malloca.md).  
  
## Syntax  
  
```  
void *_alloca(   
   size_t size   
);  
```  
  
#### Parameters  
 [in] `size`  
 Bytes to be allocated from the stack.  
  
## Return Value  
 The `_alloca` routine returns a `void` pointer to the allocated space, which is guaranteed to be suitably aligned for storage of any type of object. If `size` is 0, `_alloca` allocates a zero-length item and returns a valid pointer to that item.  
  
 A stack overflow exception is generated if the space cannot be allocated. The stack overflow exception is not a C++ exception; it is a structured exception. Instead of using C++ exception handling, you must use [Structured Exception Handling](../vs140/Structured-Exception-Handling--C-C---.md) (SEH).  
  
## Remarks  
 `_alloca` allocates `size` bytes from the program stack. The allocated space is automatically freed when the calling function exits (not when the allocation merely passes out of scope). Therefore, do not pass the pointer value returned by `_alloca` as an argument to [free](../vs140/free.md).  
  
 There are restrictions to explicitly calling `_alloca` in an exception handler (EH). EH routines that run on x86-class processors operate in their own memory frame: They perform their tasks in memory space that is not based on the current location of the stack pointer of the enclosing function. The most common implementations include Windows NT structured exception handling (SEH) and C++ catch clause expressions. Therefore, explicitly calling `_alloca` in any of the following scenarios results in program failure during the return to the calling EH routine:  
  
-   Windows NT SEH exception filter expression: `__except` (`_alloca ()` )  
  
-   Windows NT SEH final exception handler: `__finally` {`_alloca ()` }  
  
-   C++ EH catch clause expression  
  
 However, `_alloca` can be called directly from within an EH routine or from an application-supplied callback that gets invoked by one of the EH scenarios previously listed.  
  
> [!IMPORTANT]
>  In Windows XP, if `_alloca` is called inside a try/catch block, you must call [_resetstkoflw](../vs140/_resetstkoflw.md) in the catch block.  
  
 In addition to the above restrictions, when using the[/clr (Common Language Runtime Compilation)](../Topic/-clr%20\(Common%20Language%20Runtime%20Compilation\).md) option, `_alloca` cannot be used in `__except` blocks. For more information, see [/clr Restrictions](../Topic/-clr%20Restrictions.md).  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`_alloca`|<malloc.h>|  
  
## Example  
  
```  
// crt_alloca.c  
// This program demonstrates the use of  
// _alloca and trapping any exceptions  
// that may occur.  
  
#include <windows.h>  
#include <stdio.h>  
#include <malloc.h>  
  
int main()  
{  
    int     size = 1000;  
    int     errcode = 0;  
    void    *pData = NULL;  
  
    // Note: Do not use try/catch for _alloca,  
    // use __try/__except, since _alloca throws  
    // Structured Exceptions, not C++ exceptions.  
  
    __try {  
        // An unbounded _alloca can easily result in a   
        // stack overflow.  
        // Checking for a size < 1024 bytes is recommended.  
        if (size > 0 && size < 1024)  
        {  
            pData = _alloca( size );  
            printf_s( "Allocated %d bytes of stack at 0x%p",  
                      size, pData);  
        }  
        else  
        {  
            printf_s("Tried to allocate too many bytes.\n");  
        }  
    }  
  
    // If an exception occured with the _alloca function  
    __except( GetExceptionCode() == STATUS_STACK_OVERFLOW )  
    {  
        printf_s("_alloca failed!\n");  
  
        // If the stack overflows, use this function to restore.  
        errcode = _resetstkoflw();  
        if (errcode)  
        {  
            printf_s("Could not reset the stack!\n");  
            _exit(1);  
        }  
    };  
}  
```  
  
 **Allocated 1000 bytes of stack at 0x0012FB50**   
## .NET Framework Equivalent  
 Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).  
  
## See Also  
 [Memory Allocation](../vs140/Memory-Allocation.md)   
 [calloc](../vs140/calloc.md)   
 [malloc](../vs140/malloc.md)   
 [realloc](../vs140/realloc.md)   
 [_resetstkoflw](../vs140/_resetstkoflw.md)   
 [_alloca_s](../vs140/_malloca.md)