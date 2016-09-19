---
title: "memcmp, wmemcmp"
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
  - memcmp
  - wmemcmp
apilocation: 
  - msvcr110.dll
  - msvcr80.dll
  - msvcr120.dll
  - msvcrt.dll
  - msvcr110_clr0400.dll
  - msvcr90.dll
  - msvcr100.dll
  - msvcr120_clr0400.dll
apitype: DLLExport
ms.assetid: 0c21c3e3-8ee4-40e5-add1-eb26d225fd8d
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# memcmp, wmemcmp
Compares characters in two buffers.  
  
## Syntax  
  
```  
  
      int memcmp(  
   const void *buf1,  
   const void *buf2,  
   size_t count  
);  
int wmemcmp(  
   const wchar_t * buf1,  
   const wchar_t * buf2,  
   size_t count  
);  
```  
  
#### Parameters  
 `buf1`  
 First buffer.  
  
 `buf2`  
 Second buffer.  
  
 `count`  
 Number of characters to compare. (Compares bytes for `memcmp`, wide characters for `wmemcmp`).  
  
## Return Value  
 The return value indicates the relationship between the buffers.  
  
|Return value|Relationship of first `count` characters of buf1 and buf2|  
|------------------|---------------------------------------------------------------|  
|< 0|`buf1` less than `buf2`|  
|0|`buf1` identical to `buf2`|  
|> 0|`buf1` greater than `buf2`|  
  
## Remarks  
 Compares the first `count` characters of `buf1` and `buf2` and returns a value that indicates their relationship. The sign of a non-zero return value is the sign of the difference between the first differing pair of values in the buffers. The values are interpreted as `unsigned char` for `memcmp`, and as `wchar_t` for `wmemcmp`.  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`memcmp`|<memory.h> or <string.h>|  
|`wmemcmp`|<wchar.h>|  
  
 For additional compatibility information, see [Compatibility](../vs140/Compatibility.md).  
  
## Libraries  
 All versions of the [C run-time library](../vs140/CRT-Library-Features.md).  
  
## Example  
  
```  
  
      // crt_memcmp.c  
/* This program uses memcmp to compare  
 * the strings named first and second. If the first  
 * 19 bytes of the strings are equal, the program  
 * considers the strings to be equal.  
 */  
  
#include <string.h>  
#include <stdio.h>  
  
int main( void )  
{  
   char first[]  = "12345678901234567890";  
   char second[] = "12345678901234567891";  
   int int_arr1[] = {1,2,3,4};  
   int int_arr2[] = {1,2,3,4};  
   int result;  
  
   printf( "Compare '%.19s' to '%.19s':\n", first, second );  
   result = memcmp( first, second, 19 );  
   if( result < 0 )  
      printf( "First is less than second.\n" );  
   else if( result == 0 )  
      printf( "First is equal to second.\n" );  
   else  
      printf( "First is greater than second.\n" );  
  
   printf( "Compare '%d,%d' to '%d,%d':\n", int_arr1[0], int_arr1[1], int_arr2[0], int_arr2[1]);  
   result = memcmp( int_arr1, int_arr2, sizeof(int) * 2 );  
   if( result < 0 )  
      printf( "int_arr1 is less than int_arr2.\n" );  
   else if( result == 0 )  
      printf( "int_arr1 is equal to int_arr2.\n" );  
   else   
      printf( "int_arr1 is greater than int_arr2.\n" );  
}  
```  
  
## Output  
  
```  
Compare '1234567890123456789' to '1234567890123456789':  
First is equal to second.  
Compare '1,2' to '1,2':  
int_arr1 is equal to int_arr2.  
```  
  
## .NET Framework Equivalent  
 Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).  
  
## See Also  
 [Buffer Manipulation](../vs140/Buffer-Manipulation.md)   
 [_memccpy](../vs140/_memccpy.md)   
 [memchr, wmemchr](../vs140/memchr--wmemchr.md)   
 [memcpy, wmemcpy](../vs140/memcpy--wmemcpy.md)   
 [memset, wmemset](../vs140/memset--wmemset.md)   
 [strcmp, wcscmp, _mbscmp](../vs140/strcmp--wcscmp--_mbscmp.md)   
 [strncmp, wcsncmp, _mbsncmp, _mbsncmp_l](../vs140/strncmp--wcsncmp--_mbsncmp--_mbsncmp_l.md)