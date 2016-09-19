---
title: "_ungetch, _ungetwch, _ungetch_nolock, _ungetwch_nolock"
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
  - _ungetch_nolock
  - _ungetwch_nolock
  - _ungetwch
  - _ungetch
apilocation: 
  - msvcr100.dll
  - msvcr90.dll
  - msvcr110.dll
  - msvcr120.dll
  - msvcr110_clr0400.dll
  - msvcrt.dll
  - msvcr80.dll
apitype: DLLExport
ms.assetid: 70ae71c6-228c-4883-a57d-de6d5f873825
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _ungetch, _ungetwch, _ungetch_nolock, _ungetwch_nolock
Pushes back the last character that's read from the console.  
  
> [!IMPORTANT]
>  This API cannot be used in applications that execute in the Windows Runtime. For more information, see [CRT functions not supported with /ZW](http://msdn.microsoft.com/library/windows/apps/jj606124.aspx).  
  
## Syntax  
  
```  
int _ungetch(  
   int c   
);  
wint_t _ungetwch(  
   wint_t c   
);  
int _ungetch_nolock(  
   int c   
);  
wint_t _ungetwch_nolock(  
   wint_t c   
);  
```  
  
#### Parameters  
 `c`  
 Character to be pushed.  
  
## Return Value  
 Both functions return the character `c` if successful. If there is an error, `_ungetch` returns a value of `EOF` and `_ungetwch`returns`WEOF`.  
  
## Remarks  
 These functions push the character `c` back to the console, causing `c` to be the next character read by `_getch` or `_getche` (or`_getwch` or`_getwche`). `_ungetch` and `_ungetwch` fail if they are called more than once before the next read. The `c` argument may not be `EOF` (or `WEOF`).  
  
 The versions with the `_nolock` suffix are identical except that they are not protected from interference by other threads. They may be faster since they do not incur the overhead of locking out other threads. Use these functions only in thread-safe contexts such as single-threaded applications or where the calling scope already handles thread isolation.  
  
### Generic-Text Routine Mappings  
  
|TCHAR.H routine|_UNICODE & _MBCS not defined|_MBCS defined|_UNICODE defined|  
|---------------------|------------------------------------|--------------------|-----------------------|  
|`_ungettch`|`_ungetch`|`_ungetch`|`_ungetwch`|  
|`_ungettch_nolock`|`_ungetch_nolock`|`_ungetch_nolock`|`_ungetwch_nolock`|  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`_ungetch`, `_ungetch_nolock`|<conio.h>|  
|`_ungetwch`, `_ungetwch_nolock`|<conio.h> or <wchar.h>|  
  
 For additional compatibility information, see [Compatibility](../vs140/Compatibility.md).  
  
## Example  
  
```  
// crt_ungetch.c  
// compile with: /c  
// In this program, a white-space delimited   
// token is read from the keyboard. When the program   
// encounters a delimiter, it uses _ungetch to replace   
// the character in the keyboard buffer.  
//  
  
#include <conio.h>  
#include <ctype.h>  
#include <stdio.h>  
  
int main( void )  
{  
   char buffer[100];  
   int count = 0;  
   int ch;  
  
   ch = _getche();  
   while( isspace( ch ) )      // Skip preceding white space.  
      ch = _getche();  
   while( count < 99 )         // Gather token.  
   {  
      if( isspace( ch ) )      // End of token.  
         break;  
      buffer[count++] = (char)ch;  
      ch = _getche();  
   }  
   _ungetch( ch );            // Put back delimiter.  
   buffer[count] = '\0';      // Null terminate the token.  
   printf( "\ntoken = %s\n", buffer );  
}  
```  
  
  **`White`token = White**   
## See Also  
 [Console and Port I/O](../vs140/Console-and-Port-I-O.md)   
 [_cscanf, _cwscanf](../vs140/_cscanf--_cscanf_l--_cwscanf--_cwscanf_l.md)   
 [_getch, _getwch](../vs140/_getch--_getwch.md)