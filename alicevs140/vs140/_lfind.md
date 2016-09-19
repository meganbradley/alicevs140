---
title: "_lfind"
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
  - _lfind
apilocation: 
  - msvcr110.dll
  - msvcr100.dll
  - msvcrt.dll
  - msvcr90.dll
  - msvcr110_clr0400.dll
  - msvcr120.dll
  - msvcr80.dll
apitype: DLLExport
ms.assetid: a40ece70-1674-4b75-94bd-9f57cfff18f2
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _lfind
Performs a linear search for the specified key. A more secure version of this function is available; see [_lfind_s](../Topic/_lfind_s.md).  
  
## Syntax  
  
```  
void *_lfind(  
   const void *key,  
   const void *base,  
   unsigned int *num,  
   unsigned int width,  
   int (__cdecl *compare)(const void *, const void *)  
);  
```  
  
#### Parameters  
 `key`  
 Object to search for.  
  
 `base`  
 Pointer to the base of search data.  
  
 `num`  
 Number of array elements.  
  
 `width`  
 Width of array elements.  
  
 `compare`  
 Pointer to comparison routine. The first parameter is a pointer to key for search. The second parameter is a pointer to array element to be compared with key.  
  
## Return Value  
 If the key is found, `_lfind` returns a pointer to the element of the array at `base` that matches `key`. If the key is not found, `_lfind` returns `NULL`.  
  
## Remarks  
 The `_lfind` function performs a linear search for the value `key` in an array of `num` elements, each of `width` bytes. Unlike `bsearch`, `_lfind` does not require the array to be sorted. The `base` argument is a pointer to the base of the array to be searched. The `compare` argument is a pointer to a user-supplied routine that compares two array elements and then returns a value specifying their relationship. `_lfind` calls the `compare` routine one or more times during the search, passing pointers to two array elements on each call. The `compare` routine must compare the elements and then return nonzero (meaning the elements are different) or 0 (meaning the elements are identical).  
  
 This function validates its parameters. If `compare`, `key` or `num` is `NULL`, or if `base` is NULL and *`num` is nonzero, or if `width` is less than zero, the invalid parameter handler is invoked, as described in [Parameter Validation](../vs140/Parameter-Validation.md). If execution is allowed to continue, `errno` is set to `EINVAL` and the function returns `NULL`.  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`_lfind`|<search.h>|  
  
 For more compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## Example  
  
```  
// crt_lfind.c  
// This program uses _lfind to search a string array  
// for an occurrence of "hello".  
  
#include <search.h>  
#include <string.h>  
#include <stdio.h>  
  
int compare(const void *arg1, const void *arg2 )  
{  
   return( _stricmp( * (char**)arg1, * (char**)arg2 ) );  
}  
  
int main( )  
{  
   char *arr[] = {"Hi", "Hello", "Bye"};  
   int n = sizeof(arr) / sizeof(char*);  
   char **result;  
   char *key = "hello";  
  
   result = (char **)_lfind( &key, arr,   
                      &n, sizeof(char *), compare );  
  
   if( result )  
      printf( "%s found\n", *result );  
   else  
      printf( "hello not found!\n" );  
}  
```  
  
 **Hello found**   
## .NET Framework Equivalent  
 [System::Collections::ArrayList::Contains](https://msdn.microsoft.com/en-us/library/system.collections.arraylist.contains.aspx)  
  
## See Also  
 [Searching and Sorting](../vs140/Searching-and-Sorting.md)   
 [_lfind_s](../Topic/_lfind_s.md)   
 [bsearch](../vs140/bsearch.md)   
 [_lsearch](../vs140/_lsearch.md)   
 [qsort](../vs140/qsort.md)