---
title: "_write"
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
  - _write
apilocation: 
  - msvcrt.dll
  - msvcr110.dll
  - msvcr100.dll
  - msvcr80.dll
  - msvcr120.dll
  - msvcr90.dll
  - msvcr110_clr0400.dll
apitype: DLLExport
ms.assetid: 7b868c33-766f-4e1a-95a7-e8d25f0604c4
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _write
Writes data to a file.  
  
## Syntax  
  
```  
int _write(  
   int fd,  
   const void *buffer,  
   unsigned int count   
);  
```  
  
#### Parameters  
 `fd`  
 File descriptor of file into which data is written.  
  
 `buffer`  
 Data to be written.  
  
 `count`  
 Number of bytes.  
  
## Return Value  
 If successful, `_write` returns the number of bytes actually written. If the actual space remaining on the disk is less than the size of the buffer the function is trying to write to the disk, `_write` fails and does not flush any of the buffer's contents to the disk. A return value of –1 indicates an error. If invalid parameters are passed, this function invokes the invalid parameter handler, as described in [Parameter Validation](../vs140/Parameter-Validation.md). If execution is allowed to continue, the function returns -1 and `errno` is set to one of three values: `EBADF`, which means the file descriptor is invalid or the file is not opened for writing; `ENOSPC`, which means there is not enough space left on the device for the operation; or `EINVAL`, which means that `buffer` was a null pointer or that an odd `count` of bytes was passed to be written to a file in Unicode mode.  
  
 For more information about these and other return codes, see [errno, _doserrno, _sys_errlist, and _sys_nerr](../vs140/errno--_doserrno--_sys_errlist--and-_sys_nerr.md).  
  
 If the file is opened in text mode, each linefeed character is replaced with a carriage return – linefeed pair in the output. The replacement does not affect the return value.  
  
 When the file is opened in Unicode translation mode—for example, if `fd` is opened by using `_open` or `_sopen` and a mode parameter that includes `_O_WTEXT`, `_O_U16TEXT`, or `_O_U8TEXT`, or if it is opened by using `fopen` and a mode parameter that includes `ccs=UNICODE`, `ccs=UTF-16LE`, or `ccs=UTF-8`, or if the mode is changed to a Unicode translation mode by using `_setmode`—`buffer` is interpreted as a pointer to an array of `wchar_t` that contains **UTF-16** data. An attempt to write an odd number of bytes in this mode causes a parameter validation error.  
  
## Remarks  
 The `_write` function writes `count` bytes from `buffer` into the file associated with `fd`. The write operation begins at the current position of the file pointer (if any) associated with the given file. If the file is open for appending, the operation begins at the current end of the file. After the write operation, the file pointer is increased by the number of bytes actually written.  
  
 When writing to files opened in text mode, `_write` treats a CTRL+Z character as the logical end-of-file. When writing to a device, `_write` treats a CTRL+Z character in the buffer as an output terminator.  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`_write`|<io.h>|  
  
 For additional compatibility information, see [Compatibility](../vs140/Compatibility.md).  
  
## Example  
  
```  
// crt__write.c  
//   
// This program opens a file for output and uses _write to write  
// some bytes to the file.  
  
#include <io.h>  
#include <stdio.h>  
#include <stdlib.h>  
#include <fcntl.h>  
#include <sys/types.h>  
#include <sys/stat.h>  
#include <errno.h>  
#include <share.h>  
  
char buffer[] = "This is a test of '_write' function";  
  
int main( void )  
{  
   int         fileHandle = 0;  
   unsigned    bytesWritten = 0;  
  
   if ( _sopen_s(&fileHandle, "write.o", _O_RDWR | _O_CREAT,  
                  _SH_DENYNO, _S_IREAD | _S_IWRITE) )  
      return -1;  
  
   if (( bytesWritten = _write( fileHandle, buffer, sizeof( buffer ))) == -1 )  
   {  
      switch(errno)  
      {  
         case EBADF:  
            perror("Bad file descriptor!");  
            break;  
         case ENOSPC:  
            perror("No space left on device!");  
            break;  
         case EINVAL:  
            perror("Invalid parameter: buffer was NULL!");  
            break;  
         default:  
            // An unrelated error occured   
            perror("Unexpected error!");  
      }  
   }  
   else  
   {  
      printf_s( "Wrote %u bytes to file.\n", bytesWritten );  
   }  
   _close( fileHandle );  
}  
```  
  
 **Wrote 36 bytes to file.**   
## See Also  
 [Low-Level I/O](../vs140/Low-Level-I-O.md)   
 [fwrite](../vs140/fwrite.md)   
 [_open, _wopen](../Topic/_open,%20_wopen.md)   
 [_read](../vs140/_read.md)   
 [_setmode](../vs140/_setmode.md)