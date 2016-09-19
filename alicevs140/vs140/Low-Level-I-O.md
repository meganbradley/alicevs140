---
title: "Low-Level I-O"
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
H1: Low-Level I/O
ms.assetid: 53e11bdd-6720-481c-8b2b-3a3a569ed534
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Low-Level I-O
These functions invoke the operating system directly for lower-level operation than that provided by stream I/O. Low-level input and output calls do not buffer or format data.  
  
 Low-level routines can access the standard streams opened at program startup using the following predefined file descriptors.  
  
|Stream|File Descriptor|  
|------------|---------------------|  
|`stdin`|0|  
|`stdout`|1|  
|`stderr`|2|  
  
 Low-level I/O routines set the [errno](../vs140/errno--_doserrno--_sys_errlist--and-_sys_nerr.md) global variable when an error occurs. You must include STDIO.H when you use low-level functions only if your program requires a constant that is defined in STDIO.H, such as the end-of-file indicator (`EOF`).  
  
### Low-Level I/O Functions  
  
|Function|Use|  
|--------------|---------|  
|[_close](../vs140/_close.md)|Close file|  
|[_commit](../vs140/_commit.md)|Flush file to disk|  
|[_creat, _wcreat](../vs140/_creat--_wcreat.md)|Create file|  
|[_dup](../vs140/_dup--_dup2.md)|Return next available file descriptor for given file|  
|[_dup2](../vs140/_dup--_dup2.md)|Create second descriptor for given file|  
|[_eof](../vs140/_eof.md)|Test for end of file|  
|[_lseek, _lseeki64](../vs140/_lseek--_lseeki64.md)|Reposition file pointer to given location|  
|[_open, _wopen](../Topic/_open,%20_wopen.md)|Open file|  
|[_read](../vs140/_read.md)|Read data from file|  
|[_sopen, _wsopen](../vs140/_sopen--_wsopen.md), [_sopen_s, _wsopen_s](../vs140/_sopen_s--_wsopen_s.md)|Open file for file sharing|  
|[_tell, _telli64](../vs140/_tell--_telli64.md)|Get current file-pointer position|  
|[_umask](../vs140/_umask.md), [_umask_s](../vs140/_umask_s.md)|Set file-permission mask|  
|[_write](../vs140/_write.md)|Write data to file|  
  
 `_dup` and `_dup2` are typically used to associate the predefined file descriptors with different files.  
  
## See Also  
 [Input and Output](../vs140/Input-and-Output.md)   
 [Run-Time Routines by Category](../vs140/Run-Time-Routines-by-Category.md)   
 [System Calls](../vs140/System-Calls.md)