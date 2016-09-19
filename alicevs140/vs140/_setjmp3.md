---
title: "_setjmp3"
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
  - _setjmp3
apilocation: 
  - msvcrt.dll
  - msvcr90.dll
  - msvcr110.dll
  - msvcr80.dll
  - msvcr110_clr0400.dll
  - msvcr100.dll
  - msvcr120.dll
apitype: DLLExport
ms.assetid: 6129c2f3-8bac-4fdb-a827-44e1eebba500
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _setjmp3
Internal CRT function. A new implementation of the `setjmp` function.  
  
## Syntax  
  
```  
int _setjmp3(  
   OUT jmp_buf env,  
   int count,  
   (optional parameters)  
);  
```  
  
#### Parameters  
 [out] `env`  
 Address of the buffer for storing state information.  
  
 [in] `count`  
 The number of additional `DWORD`s of information that are stored in the `optional parameters`.  
  
 [in] `optional parameters`  
 Additional data pushed down by the `setjmp` intrinsic. The first `DWORD` is a function pointer that is used to unwind extra data and return to a nonvolatile register state. The second `DWORD` is the try level to be restored. Any further data is saved in the generic data array in the `jmp_buf`.  
  
## Return Value  
 Always returns 0.  
  
## Remarks  
 Do not use this function in a C++ program. It is an intrinsic function that does not support C++. For more information about how to use `setjmp`, see [Using setjmp/longjmp](../vs140/Using-setjmp-longjmp.md).  
  
## Requirements  
  
## See Also  
 [Alphabetical Function Reference](../vs140/CRT-Alphabetical-Function-Reference.md)   
 [setjmp](../vs140/setjmp.md)