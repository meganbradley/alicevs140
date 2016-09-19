---
title: "_fwrite_nolock"
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
  - _fwrite_nolock
apilocation: 
  - msvcr80.dll
  - msvcr110_clr0400.dll
  - msvcrt.dll
  - msvcr120.dll
  - msvcr110.dll
  - msvcr90.dll
  - msvcr100.dll
apitype: DLLExport
ms.assetid: 2b4ec6ce-742e-4615-8407-44a0a18ec1d7
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _fwrite_nolock
Writes data to a stream, without locking the thread.  
  
## Syntax  
  
```  
size_t _fwrite_nolock(  
   const void *buffer,  
   size_t size,  
   size_t count,  
   FILE *stream   
);  
```  
  
#### Parameters  
 `buffer`  
 Pointer to the data to be written.  
  
 `size`  
 Item size in bytes.  
  
 `count`  
 Maximum number of items to be written.  
  
 `stream`  
 Pointer to the `FILE` structure.  
  
## Return Value  
 Same as [fwrite](../vs140/fwrite.md).  
  
## Remarks  
 This function is a non-locking version of `fwrite`. It is identical to `fwrite` except that it is not protected from interference by other threads. It might be faster because it does not incur the overhead of locking out other threads. Use this function only in thread-safe contexts such as single-threaded applications or where the calling scope already handles thread isolation.  
  
## Requirements  
  
|Function|Required header|  
|--------------|---------------------|  
|`_fwrite_nolock`|<stdio.h>|  
  
 For more compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## Example  
 See the example for [fread](../vs140/fread.md).  
  
## .NET Framework Equivalent  
 [System::IO::FileStream::Write](https://msdn.microsoft.com/en-us/library/system.io.filestream.write.aspx)  
  
## See Also  
 [Stream I/O](../vs140/Stream-I-O.md)   
 [fread](../vs140/fread.md)   
 [_write](../vs140/_write.md)