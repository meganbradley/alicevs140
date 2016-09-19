---
title: "_seh_filter_dll, _seh_filter_exe"
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
  - _XcptFilter
  - _seh_filter_dll
  - _seh_filter_exe
apilocation: 
  - msvcr90.dll
  - msvcr110.dll
  - msvcrt.dll
  - msvcr100.dll
  - msvcr110_clr0400.dll
  - msvcr80.dll
  - msvcr120.dll
  - api-ms-win-crt-runtime-l1-1-0.dll
apitype: DLLExport
ms.assetid: 747e5963-3a12-4bf5-b5c4-d4c1b6068e15
caps.latest.revision: 16
translation.priority.mt: 
  - de-de
  - ja-jp
---
# _seh_filter_dll, _seh_filter_exe
Identifies the exception and the related action to be taken.  
  
## Syntax  
  
```  
int __cdecl _seh_filter_dll(  
   unsigned long _ExceptionNum,  
   struct _EXCEPTION_POINTERS* _ExceptionPtr  
);  
int __cdecl _seh_filter_exe(  
   unsigned long _ExceptionNum,  
   struct _EXCEPTION_POINTERS* _ExceptionPtr  
);  
```  
  
#### Parameters  
 [in] `_ExceptionNum`  
 The identifier for the exception.  
  
 [in] `_ExceptionPtr`  
 A pointer to the exception information.  
  
## Return Value  
 An integer that indicates the action to be taken, based on the result of exception processing.  
  
## Remarks  
 These methods are called by the exception-filter expression of the [try-except statement](../vs140/try-except-Statement.md). The method consults a constant internal table to identify the exception and determine the appropriate action, as shown here. The exception numbers are defined in winnt.h and the signal numbers are defined in signal.h.  
  
|Exception Number (unsigned long)|Signal Number|  
|----------------------------------------|-------------------|  
|STATUS_ACCESS_VIOLATION|SIGSEGV|  
|STATUS_ILLEGAL_INSTRUCTION|SIGILL|  
|STATUS_PRIVILEGED_INSTRUCTION|SIGILL|  
|STATUS_FLOAT_DENORMAL_OPERAND|SIGFPE|  
|STATUS_FLOAT_DIVIDE_BY_ZERO|SIGFPE|  
|STATUS_FLOAT_INEXACT_RESULT|SIGFPE|  
|STATUS_FLOAT_INVALID_OPERATION|SIGFPE|  
|STATUS_FLOAT_OVERFLOW|SIGFPE|  
|STATUS_FLOAT_STACK_CHECK|SIGFPE|  
|STATUS_FLOAT_UNDERFLOW|SIGFPE|  
  
## Requirements  
 **Header:** corecrt_startup.h  
  
## See Also  
 [Alphabetical Function Reference](../vs140/CRT-Alphabetical-Function-Reference.md)