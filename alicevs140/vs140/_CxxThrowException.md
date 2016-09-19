---
title: "_CxxThrowException"
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
  - _CxxThrowException
apilocation: 
  - msvcr110.dll
  - msvcr100.dll
  - msvcrt.dll
  - msvcr120.dll
  - msvcr110_clr0400.dll
  - msvcr80.dll
  - msvcr90.dll
apitype: DLLExport
ms.assetid: 0b90bef5-b7d2-46e0-88e2-59e531e01a4d
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _CxxThrowException
Builds the exception record and calls the runtime environment to start processing the exception.  
  
## Syntax  
  
```  
extern "C" void __stdcall _CxxThrowException(  
   void* pExceptionObject  
   _ThrowInfo* pThrowInfo  
);  
```  
  
#### Parameters  
 [in] `pExceptionObject`  
 The object that generated the exception.  
  
 [in] `pThrowInfo`  
 The information that is required to process the exception.  
  
## Remarks  
 This method is included in a compiler-only file that the compiler uses to process exceptions. Do not call the method directly from your code.  
  
## Requirements  
 **Source:** Throw.cpp  
  
## See Also  
 [Alphabetical Function Reference](../vs140/CRT-Alphabetical-Function-Reference.md)