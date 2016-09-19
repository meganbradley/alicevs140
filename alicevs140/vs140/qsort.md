---
title: "qsort"
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
  - qsort
apilocation: 
  - msvcr110_clr0400.dll
  - msvcr110.dll
  - msvcr90.dll
  - msvcr100.dll
  - msvcr120.dll
  - msvcrt.dll
  - msvcr80.dll
apitype: DLLExport
ms.assetid: d6cb33eb-d209-485f-8d41-229eb743c027
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# qsort
Performs a quick sort. A more secure version of this function is available; see [qsort_s](../Topic/qsort_s.md).  
  
## Syntax  
  
```  
void qsort(  
   void *base,  
   size_t num,  
   size_t width,  
   int (__cdecl *compare )(const void *, const void *)   
);  
```  
  
#### Parameters  
 `base`  
 Start of target array.  
  
 `num`  
 Array size in elements.  
  
 `width`  
 Element size in bytes.  
  
 `compare`  
 Pointer to a user-supplied routine that compares two array elements and returns a value that specifies their relationship.  
  
## Remarks  
 The `qsort` function implements a quick-sort algorithm to sort an array of `num` elements, each of `width` bytes. The argument `base` is a pointer to the base of the array to be sorted. `qsort` overwrites this array by using the sorted elements.  
  
 `qsort` calls the `compare` routine one or more times during the sort, and passes pointers to two array elements on each call.  
  
```  
compare( (void *) & elem1, (void *) & elem2 );  
```  
  
 The routine compares the elements and returns one of the following values.  
  
|Compare function return value|Description|  
|-----------------------------------|-----------------|  
|< 0|`elem1` less than `elem2`|  
|0|`elem1` equivalent to `elem2`|  
|> 0|`elem1` greater than `elem2`|  
  
 The array is sorted in increasing order, as defined by the comparison function. To sort an array in decreasing order, reverse the sense of "greater than" and "less than" in the comparison function.  
  
 This function validates its parameters. If `compare` or `num` is `NULL`, or if `base` is `NULL` and *`num` is nonzero, or if `width` is less than zero, the invalid parameter handler is invoked, as described in [Parameter Validation](../vs140/Parameter-Validation.md). If execution is allowed to continue, the function returns and `errno` is set to `EINVAL`.  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`qsort`|<stdlib.h> and <search.h>|  
  
 For additional compatibility information, see [Compatibility](../vs140/Compatibility.md).  
  
## Example  
  
```  
// crt_qsort.c  
// arguments: every good boy deserves favor  
  
/* This program reads the command-line  
 * parameters and uses qsort to sort them. It  
 * then displays the sorted arguments.  
 */  
  
#include <stdlib.h>  
#include <string.h>  
#include <stdio.h>  
  
int compare( const void *arg1, const void *arg2 );  
  
int main( int argc, char **argv )  
{  
   int i;  
   /* Eliminate argv[0] from sort: */  
   argv++;  
   argc--;  
  
   /* Sort remaining args using Quicksort algorithm: */  
   qsort( (void *)argv, (size_t)argc, sizeof( char * ), compare );  
  
   /* Output sorted list: */  
   for( i = 0; i < argc; ++i )  
      printf( " %s", argv[i] );  
   printf( "\n" );  
}  
  
int compare( const void *arg1, const void *arg2 )  
{  
   /* Compare all of both strings: */  
   return _stricmp( * ( char** ) arg1, * ( char** ) arg2 );  
}  
```  
  
  **boy deserves every favor good**   
## .NET Framework Equivalent  
 [System::Collections::ArrayList::Sort](https://msdn.microsoft.com/en-us/library/system.collections.arraylist.sort.aspx)  
  
## See Also  
 [Searching and Sorting](../vs140/Searching-and-Sorting.md)   
 [bsearch](../vs140/bsearch.md)   
 [_lsearch](../vs140/_lsearch.md)