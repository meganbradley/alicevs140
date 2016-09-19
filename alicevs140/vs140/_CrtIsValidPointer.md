---
title: "_CrtIsValidPointer"
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
  - _CrtIsValidPointer
apilocation: 
  - msvcr90.dll
  - msvcr80.dll
  - msvcrt.dll
  - msvcr110_clr0400.dll
  - msvcr120.dll
  - msvcr100.dll
  - msvcr110.dll
apitype: DLLExport
ms.assetid: 91c35590-ea5e-450f-a15d-ad8d62ade1fa
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _CrtIsValidPointer
Verifies that a pointer is not null. In versions of the C run-time library before Visual Studio 2010, verifies that a specified memory range is valid for reading and writing (debug version only).  
  
## Syntax  
  
```  
int _CrtIsValidPointer(   
   const void *address,  
   unsigned int size,  
   int access   
);  
```  
  
#### Parameters  
 address  
 Points to the beginning of the memory range to test for validity.  
  
 `size`  
 Size of the specified memory range (in bytes).  
  
 access  
 Read/write accessibility to determine for the memory range.  
  
## Return Value  
 `_CrtIsValidPointer` returns TRUE if the specified pointer is not null. In CRT library versions before Visual Studio 2010, returns TRUE if the memory range is valid for the specified operation or operations. Otherwise, the function returns FALSE.  
  
## Remarks  
 Starting with the CRT library in Visual Studio 2010, the size and access parameters are ignored, and `_CrtIsValidPointer` only verifies that the specified address is not null. Because this test is easy to perform yourself, we do not recommend you use this function. In versions before Visual Studio 2010, the function verifies that the memory range beginning at `address` and extending for `size` bytes is valid for the specified accessibility operation or operations. When `access` is set to TRUE, the memory range is verified for both reading and writing. When `access` is FALSE, the memory range is only validated for reading. When [_DEBUG](../vs140/_DEBUG.md) is not defined, calls to `_CrtIsValidPointer` are removed during preprocessing.  
  
 Because this function returns TRUE or FALSE, it can be passed to one of the [_ASSERT](../vs140/_ASSERT--_ASSERTE--_ASSERT_EXPR-Macros.md) macros to create a simple debugging error handling mechanism. The following example causes an assertion failure if the memory range is not valid for both reading and writing operations:  
  
```  
_ASSERTE( _CrtIsValidPointer( address, size, TRUE ) );  
```  
  
 For more information about how `_CrtIsValidPointer` can be used with other debug functions and macros, see [Macros for Reporting](../vs140/Macros-for-Reporting.md). For information about how memory blocks are allocated, initialized, and managed in the debug version of the base heap, see [CRT Debug Heap Details](../vs140/CRT-Debug-Heap-Details.md).  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`_CrtIsValidPointer`|<crtdbg.h>|  
  
 `_CrtIsValidPointer` is a Microsoft extension. For compatibility information, see [Compatibility](../vs140/Compatibility.md).  
  
## Libraries  
 Debug versions of [C run-time libraries](../vs140/CRT-Library-Features.md) only.  
  
## Example  
 See the example for the [_CrtIsValidHeapPointer](../vs140/_CrtIsValidHeapPointer.md) topic.  
  
## .NET Framework Equivalent  
 Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).  
  
## See Also  
 [Debug Routines](../vs140/Debug-Routines.md)