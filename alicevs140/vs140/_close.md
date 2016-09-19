---
title: "_close"
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
  - _close
apilocation: 
  - msvcr100.dll
  - msvcr90.dll
  - msvcr110_clr0400.dll
  - msvcrt.dll
  - msvcr80.dll
  - msvcr110.dll
  - msvcr120.dll
apitype: DLLExport
ms.assetid: 4708a329-8acf-4cd9-b7b0-a952e1897247
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _close
Closes a file.  
  
## Syntax  
  
```  
int _close(   
   int fd   
);  
```  
  
#### Parameters  
 `fd`  
 File descriptor referring to the open file.  
  
## Return Value  
 `_close` returns 0 if the file was successfully closed. A return value of –1 indicates an error.  
  
## Remarks  
 The `_close` function closes the file associated with `fd`.  
  
 The file descriptor and the underlying OS file handle are closed. Thus, it is not necessary to call `CloseHandle` if the file was originally opened using the Win32 function `CreateFile` and converted to a file descriptor using `_open_osfhandle`.  
  
 This function validates its parameters. If `fd` is a bad file descriptor, the invalid parameter handler is invoked, as described in [Parameter Validation](../vs140/Parameter-Validation.md). If execution is allowed to continue, the functions returns -1 and `errno` is set to `EBADF`.  
  
## Requirements  
  
|Routine|Required header|Optional header|  
|-------------|---------------------|---------------------|  
|`_close`|<io.h>|<errno.h>|  
  
 For more compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## Example  
 See the example for [_open](../Topic/_open,%20_wopen.md).  
  
## See Also  
 [Low-Level I/O](../vs140/Low-Level-I-O.md)   
 [_chsize](../vs140/_chsize.md)   
 [_creat, _wcreat](../vs140/_creat--_wcreat.md)   
 [_dup, _dup2](../vs140/_dup--_dup2.md)   
 [_open, _wopen](../Topic/_open,%20_wopen.md)   
 [_unlink, _wunlink](../vs140/_unlink--_wunlink.md)