---
title: "ferror"
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
  - ferror
apilocation: 
  - msvcr100.dll
  - msvcr80.dll
  - msvcr90.dll
  - msvcr120.dll
  - msvcr110_clr0400.dll
  - msvcrt.dll
  - msvcr110.dll
apitype: DLLExport
ms.assetid: 528a34bc-f2aa-4c3f-b89a-5b148e6864f7
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ferror
Tests for an error on a stream.  
  
## Syntax  
  
```  
int ferror(   
   FILE *stream   
);  
```  
  
#### Parameters  
 `stream`  
 Pointer to `FILE` structure.  
  
## Return Value  
 If no error has occurred on `stream`, `ferror` returns 0. Otherwise, it returns a nonzero value. If stream is `NULL`, `ferror` invokes the invalid parameter handler, as described in [Parameter Validation](../vs140/Parameter-Validation.md). If execution is allowed to continue, this function sets `errno` to `EINVAL` and returns 0.  
  
 See [_doserrno, errno, _sys_errlist, and _sys_nerr](../vs140/errno--_doserrno--_sys_errlist--and-_sys_nerr.md) for more information on these, and other, error codes.  
  
## Remarks  
 The `ferror` routine (implemented both as a function and as a macro) tests for a reading or writing error on the file associated with `stream`. If an error has occurred, the error indicator for the stream remains set until the stream is closed or rewound, or until `clearerr` is called against it.  
  
## Requirements  
  
|Function|Required header|  
|--------------|---------------------|  
|`ferror`|<stdio.h>|  
  
 For additional compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## Example  
 See the example for [feof](../vs140/feof.md).  
  
## .NET Framework Equivalent  
 Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).  
  
## See Also  
 [Error Handling](../vs140/Error-Handling--CRT-.md)   
 [Stream I/O](../vs140/Stream-I-O.md)   
 [clearerr](../vs140/clearerr.md)   
 [_eof](../vs140/_eof.md)   
 [feof](../vs140/feof.md)   
 [fopen, _wfopen](../vs140/fopen--_wfopen.md)   
 [perror, _wperror](../vs140/perror--_wperror.md)