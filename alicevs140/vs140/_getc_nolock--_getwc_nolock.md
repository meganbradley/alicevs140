---
title: "_getc_nolock, _getwc_nolock"
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
  - _getc_nolock
  - _getwc_nolock
apilocation: 
  - msvcrt.dll
  - msvcr100.dll
  - msvcr80.dll
  - msvcr120.dll
  - msvcr90.dll
  - msvcr110.dll
  - msvcr110_clr0400.dll
apitype: DLLExport
ms.assetid: eb37b272-e177-41c9-b077-12ce7ffd3b88
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _getc_nolock, _getwc_nolock
Reads a character from a stream.  
  
## Syntax  
  
```  
int _getc_nolock(   
   FILE *stream   
);  
wint_t _getwc_nolock(   
   FILE *stream   
);  
```  
  
#### Parameters  
 `stream`  
 Input stream.  
  
## Return Value  
 See [getc, getwc](../vs140/getc--getwc.md).  
  
## Remarks  
 These functions are identical to `getc` and `getwc` except that they do not lock the calling thread. They might be faster because they do not incur the overhead of locking out other threads. Use these functions only in thread-safe contexts such as single-threaded applications or where the calling scope already handles thread isolation.  
  
### Generic-Text Routine Mappings  
  
|Tchar.h routine|_UNICODE and _MBCS not defined|_MBCS defined|_UNICODE defined|  
|---------------------|--------------------------------------|--------------------|-----------------------|  
|`_gettc_nolock`|`getc_nolock`|`getc_nolock`|`getwc_nolock`|  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`getc_nolock`|<stdio.h>|  
|`getwc_nolock`|<stdio.h> or <wchar.h>|  
  
 For more compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## Example  
  
```  
// crt_getc_nolock.c  
// Use getc to read a line from a file.  
  
#include <stdio.h>  
  
int main()  
{  
    char buffer[81];  
    int i, ch;  
    FILE* fp;  
  
    // Read a single line from the file "crt_getc_nolock.txt".  
    fopen_s(&fp, "crt_getc_nolock.txt", "r");  
    if (!fp)  
    {  
       printf("Failed to open file crt_getc_nolock.txt.\n");  
       exit(1);  
    }  
  
    for (i = 0; (i < 80) && ((ch = getc(fp)) != EOF)  
                         && (ch != '\n'); i++)  
    {  
        buffer[i] = (char) ch;  
    }  
  
    // Terminate string with a null character   
    buffer[i] = '\0';  
    printf( "Input was: %s\n", buffer);  
  
    fclose(fp);  
}  
```  
  
## Input: crt_getc_nolock.txt  
  
```  
Line the first.  
Line the second.  
```  
  
### Output  
  
```  
Input was: Line the first.  
```  
  
## .NET Framework Equivalent  
  
-   [System::IO::StreamReader::Read](https://msdn.microsoft.com/en-us/library/system.io.streamreader.read.aspx)  
  
-   [System::Console::Read](https://msdn.microsoft.com/en-us/library/system.console.read.aspx)  
  
## See Also  
 [Stream I/O](../vs140/Stream-I-O.md)   
 [fgetc, fgetwc](../vs140/fgetc--fgetwc.md)   
 [_getch, _getwch](../vs140/_getch--_getwch.md)   
 [putc, putwc](../vs140/putc--putwc.md)   
 [ungetc, ungetwc](../vs140/ungetc--ungetwc.md)