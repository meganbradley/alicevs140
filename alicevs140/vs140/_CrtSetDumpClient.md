---
title: "_CrtSetDumpClient"
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
  - _CrtSetDumpClient
apilocation: 
  - msvcr110.dll
  - msvcr120.dll
  - msvcr80.dll
  - msvcr110_clr0400.dll
  - msvcr90.dll
  - msvcr100.dll
  - msvcrt.dll
apitype: DLLExport
ms.assetid: f3dd06d0-c331-4a12-b68d-25378d112033
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _CrtSetDumpClient
Installs an application-defined function to dump `_CLIENT_BLOCK` type memory blocks (debug version only).  
  
## Syntax  
  
```  
  
      _CRT_DUMP_CLIENT _CrtSetDumpClient(   
   _CRT_DUMP_CLIENT dumpClient   
);  
```  
  
#### Parameters  
 `dumpClient`  
 New client-defined memory dump function to hook into the C run-time debug memory dump process.  
  
## Return Value  
 Returns the previously defined client block dump function.  
  
## Remarks  
 The `_CrtSetDumpClient` function allows the application to hook its own function to dump objects stored in `_CLIENT_BLOCK` memory blocks into the C run-time debug memory dump process. As a result, every time a debug dump function such as [_CrtMemDumpAllObjectsSince](../vs140/_CrtMemDumpAllObjectsSince.md) or [_CrtDumpMemoryLeaks](../vs140/_CrtDumpMemoryLeaks.md) dumps a `_CLIENT_BLOCK` memory block, the application's dump function is called as well. `_CrtSetDumpClient` provides an application with an easy method for detecting memory leaks and validating or reporting the contents of data stored in `_CLIENT_BLOCK` blocks. When [_DEBUG](../vs140/_DEBUG.md) is not defined, calls to `_CrtSetDumpClient` are removed during preprocessing.  
  
 The `_CrtSetDumpClient` function installs the new application-defined dump function specified in `dumpClient` and returns the previously defined dump function. An example of a client block dump function is as follows:  
  
```  
void DumpClientFunction( void *userPortion, size_t blockSize );  
```  
  
 The `userPortion` argument is a pointer to the beginning of the user data portion of the memory block and `blockSize` specifies the size of the allocated memory block in bytes. The client block dump function must return `void`. The pointer to the client dump function that is passed to `_CrtSetDumpClient` is of type `_CRT_DUMP_CLIENT`, as defined in Crtdbg.h:  
  
```  
typedef void (__cdecl *_CRT_DUMP_CLIENT)( void *, size_t );  
```  
  
 For more information about functions that operate on `_CLIENT_BLOCK` type memory blocks, see [Client Block Hook Functions](../vs140/Client-Block-Hook-Functions.md). The [_CrtReportBlockType](../vs140/_CrtReportBlockType.md) function can be used to return information about block types and subtypes.  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`_CrtSetDumpClient`|<crtdbg.h>|  
  
 For more compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## Libraries  
 Debug versions of [C run-time libraries](../vs140/CRT-Library-Features.md) only.  
  
## .NET Framework Equivalent  
 Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).  
  
## See Also  
 [Debug Routines](../vs140/Debug-Routines.md)   
 [_CrtReportBlockType](../vs140/_CrtReportBlockType.md)   
 [_CrtGetDumpClient](../vs140/_CrtGetDumpClient.md)