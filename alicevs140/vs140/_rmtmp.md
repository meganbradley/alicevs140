---
title: "_rmtmp"
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
  - _rmtmp
apilocation: 
  - msvcr90.dll
  - msvcr110_clr0400.dll
  - msvcr80.dll
  - msvcr110.dll
  - msvcr120.dll
  - msvcrt.dll
  - msvcr100.dll
apitype: DLLExport
ms.assetid: 7419501e-2587-4f2a-b469-0dca07f84736
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _rmtmp
Removes temporary files.  
  
## Syntax  
  
```  
  
int _rmtmp( void );  
```  
  
## Return Value  
 `_rmtmp` returns the number of temporary files closed and deleted.  
  
## Remarks  
 The `_rmtmp` function cleans up all temporary files in the current directory. The function removes only those files created by `tmpfile`; use it only in the same directory in which the temporary files were created.  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`_rmtmp`|<stdio.h>|  
  
 For more compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## Libraries  
 All versions of the [C run-time libraries](../vs140/CRT-Library-Features.md).  
  
## Example  
 See the example for [tmpfile](../vs140/tmpfile.md).  
  
## .NET Framework Equivalent  
 Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).  
  
## See Also  
 [Stream I/O](../vs140/Stream-I-O.md)   
 [_flushall](../vs140/_flushall.md)   
 [tmpfile](../vs140/tmpfile.md)   
 [_tempnam, _wtempnam, tmpnam, _wtmpnam](../vs140/_tempnam--_wtempnam--tmpnam--_wtmpnam.md)