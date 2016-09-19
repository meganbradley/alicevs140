---
title: "_lock_file"
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
  - _lock_file
apilocation: 
  - msvcr110_clr0400.dll
  - msvcr110.dll
  - msvcr80.dll
  - msvcrt.dll
  - msvcr100.dll
  - msvcr90.dll
  - msvcr120.dll
apitype: DLLExport
ms.assetid: 75c7e0e6-efff-4747-b6ed-9bcf2b0894c3
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _lock_file
Locks a `FILE` object to ensure consistency for threads accessing the `FILE` object concurrently.  
  
## Syntax  
  
```  
void _lock_file(  
   FILE* file  
);  
```  
  
#### Parameters  
 `file`  
 File handle.  
  
## Remarks  
 The `_lock_file` function locks the `FILE` object specified by `file`. The underlying file is not locked by `_lock_file`. Use [_unlock_file](../vs140/_unlock_file.md) to release the lock on the file. Calls to `_lock_file` and `_unlock_file` must be matched in a thread.  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`_lock_file`|<stdio.h>|  
  
 For more compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## Example  
  
```  
// crt_lock_file.c  
// This example creates multiple threads that write to standard output  
// concurrently, first with _file_lock, then without.  
  
#include <stdio.h>  
#include <process.h>// _beginthread  
#include <windows.h>// HANDLE  
  
void Task_locked( void* str )  
{  
    for( int i=0; i<1000; ++i )  
    {  
        _lock_file( stdout );  
        for( char* cp = (char*)str; *cp; ++cp )  
        {  
            _fputc_nolock( *cp, stdout );  
        }  
        _unlock_file( stdout );  
    }  
}  
  
void Task_unlocked( void* str )  
{  
    for( int i=0; i<1000; ++i )  
    {  
        for( char* cp = (char*)str; *cp; ++cp )  
        {  
            fputc( *cp, stdout );  
        }  
    }  
}  
  
int main()  
{  
    HANDLE h[3];  
    h[0] = (HANDLE)_beginthread( &Task_locked, 0, "First\n" );  
    h[1] = (HANDLE)_beginthread( &Task_locked, 0, "Second\n" );  
    h[2] = (HANDLE)_beginthread( &Task_locked, 0, "Third\n" );  
  
    WaitForMultipleObjects( 3, h, true, INFINITE );  
  
    h[0] = (HANDLE)_beginthread( &Task_unlocked, 0, "First\n" );  
    h[1] = (HANDLE)_beginthread( &Task_unlocked, 0, "Second\n" );  
    h[2] = (HANDLE)_beginthread( &Task_unlocked, 0, "Third\n" );  
  
    WaitForMultipleObjects( 3, h, true, INFINITE );  
}  
```  
  
 **...**  
**First**  
**Second**  
**First**  
**Second**  
**Third**  
**Second**  
**Third**  
**Second**  
**...**  
**FSiercsotn**  
**dF**  
**iSrescto**  
**nFdi**  
**rSsetc**  
**oFnidr**  
**sSte**  
**cFoinrds**  
**tS**  
**eFciornsdt**   
## .NET Framework Equivalent  
 [System::IO::FileStream::Lock](https://msdn.microsoft.com/en-us/library/system.io.filestream.lock.aspx)  
  
## See Also  
 [File Handling](../Topic/File%20Handling.md)   
 [_creat, _wcreat](../vs140/_creat--_wcreat.md)   
 [_open, _wopen](../Topic/_open,%20_wopen.md)   
 [_unlock_file](../vs140/_unlock_file.md)