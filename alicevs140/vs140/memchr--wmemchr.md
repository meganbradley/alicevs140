---
title: "memchr, wmemchr"
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
  - wmemchr
  - memchr
apilocation: 
  - msvcr110.dll
  - msvcr90.dll
  - msvcr80.dll
  - msvcr120.dll
  - msvcr100.dll
  - msvcrt.dll
  - msvcr110_clr0400.dll
apitype: DLLExport
ms.assetid: 5a348581-28f1-4256-8434-687245f7fc9f
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# memchr, wmemchr
Find characters in a buffer.  
  
## Syntax  
  
```  
void *memchr(  
   const void *buf,  
   int c,  
   size_t count  
); // C only  
void *memchr(  
   void *buf,  
   int c,  
   size_t count  
); // C++ only  
const void *memchr(  
   const void *buf,  
   int c,  
   size_t count  
); // C++ only  
wchar_t *wmemchr(  
   const wchar_t * buf,   
   wchar_t c,  
   size_t count  
); // C only  
wchar_t *wmemchr(  
   wchar_t * buf,   
   wchar_t c,  
   size_t count  
); // C++ only  
const wchar_t *wmemchr(  
   const wchar_t * buf,   
   wchar_t c,  
   size_t count  
); // C++ only  
```  
  
#### Parameters  
 `buf`  
 Pointer to buffer.  
  
 `c`  
 Character to look for.  
  
 `count`  
 Number of characters to check.  
  
## Return Value  
 If successful, returns a pointer to the first location of `c` in `buf`. Otherwise it returns `NULL`.  
  
## Remarks  
 `memchr` and `wmemchr` look for the first occurrence of `c` in the first `count` bytes of `buf`. It stops when it finds `c` or when it has checked the first `count` bytes.  
  
 In C, these functions take a `const` pointer for the first argument. In C++, two overloads are available. The overload taking a pointer to `const` returns a pointer to `const`; the version that takes a pointer to non-`const` returns a pointer to non-`const`. The macro _CONST_CORRECT_OVERLOADS is defined if both the `const` and non-`const` versions of these functions are available. If you require the non-`const` behavior for both C++ overloadsin C++, define the symbol _CONST_RETURN.  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`memchr`|<memory.h> or <string.h>|  
|`wmemchr`|<wchar.h>|  
  
 For more information about compatibility, see [Compatibility](../vs140/Compatibility.md).  
  
## Libraries  
 All versions of the [C run-time libraries](../vs140/CRT-Library-Features.md).  
  
## Example  
  
```  
// crt_memchr.c  
  
#include <memory.h>  
#include <stdio.h>  
  
int  ch = 'r';  
char str[] =    "lazy";  
char string[] = "The quick brown dog jumps over the lazy fox";  
char fmt1[] =   "         1         2         3         4         5";  
char fmt2[] =   "12345678901234567890123456789012345678901234567890";  
  
int main( void )  
{  
   char *pdest;  
   int result;  
   printf( "String to be searched:\n             %s\n", string );  
   printf( "             %s\n             %s\n\n", fmt1, fmt2 );  
  
   printf( "Search char: %c\n", ch );  
   pdest = memchr( string, ch, sizeof( string ) );  
   result = (int)(pdest - string + 1);  
   if ( pdest != NULL )  
      printf( "Result:      %c found at position %d\n", ch, result );  
   else  
      printf( "Result:      %c not found\n" );  
}  
```  
  
## Output  
  
```  
String to be searched:  
             The quick brown dog jumps over the lazy fox  
                      1         2         3         4         5  
             12345678901234567890123456789012345678901234567890  
  
Search char: r  
Result:      r found at position 12  
```  
  
## .NET Framework Equivalent  
 Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).  
  
## See Also  
 [Buffer Manipulation](../vs140/Buffer-Manipulation.md)   
 [_memccpy](../vs140/_memccpy.md)   
 [memcmp, wmemcmp](../vs140/memcmp--wmemcmp.md)   
 [memcpy, wmemcpy](../vs140/memcpy--wmemcpy.md)   
 [memset, wmemset](../vs140/memset--wmemset.md)   
 [strchr, wcschr, _mbschr, _mbschr_l](../vs140/strchr--wcschr--_mbschr--_mbschr_l.md)