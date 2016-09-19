---
title: "_lsearch_s"
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
  - _lsearch_s
apilocation: 
  - msvcr80.dll
  - msvcr120.dll
  - msvcr100.dll
  - msvcr110_clr0400.dll
  - msvcrt.dll
  - msvcr90.dll
  - msvcr110.dll
apitype: DLLExport
ms.assetid: d2db0635-be7a-4799-8660-255f14450882
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _lsearch_s
Performs a linear search for a value. A version of [_lsearch](../vs140/_lsearch.md) with security enhancements as described in [Security Enhancements in the CRT](../vs140/Security-Features-in-the-CRT.md).  
  
## Syntax  
  
```  
void *_lsearch_s(  
   const void *key,  
   void *base,  
   unsigned int *num,  
   size_t size,  
   int (__cdecl *compare)(void *, const void *, const void *),  
   void * context  
);  
```  
  
#### Parameters  
 `key`  
 Object to search for.  
  
 `base`  
 Pointer to the base of array to be searched.  
  
 `num`  
 Number of elements.  
  
 `size`  
 Size of each array element in bytes.  
  
 `compare`  
 Pointer to the comparison routine. The second parameter is a pointer to the key for search. The third parameter is a pointer to an array element to be compared with the key.  
  
 `context`  
 A pointer to an object that might be accessed in the comparison function.  
  
## Return Value  
 If `key` is found, `_lsearch_s` returns a pointer to the element of the array at `base` that matches `key`. If `key` is not found, `_lsearch_s` returns a pointer to the newly added item at the end of the array.  
  
 If invalid parameters are passed to the function, the invalid parameter handler is invoked, as described in [Parameter Validation](../vs140/Parameter-Validation.md). If execution is allowed to continue, then `errno` is set to `EINVAL` and the function returns `NULL`. For more information, see [errno, _doserrno, _sys_errlist, and _sys_nerr](../vs140/errno--_doserrno--_sys_errlist--and-_sys_nerr.md).  
  
### Error Conditions  
  
|`key`|`base`|`compare`|`num`|`size`|`errno`|  
|-----------|------------|---------------|-----------|------------|-------------|  
|`NULL`|any|any|any|any|`EINVAL`|  
|any|`NULL`|any|!= 0|any|`EINVAL`|  
|any|any|any|any|zero|`EINVAL`|  
|any|any|`NULL`|an|any|`EINVAL`|  
  
## Remarks  
 The `_lsearch_s` function performs a linear search for the value `key` in an array of `num` elements, each of `width` bytes. Unlike `bsearch_s`, `_lsearch_s` does not require the array to be sorted. If `key` is not found, then `_lsearch_s` adds it to the end of the array and increments `num`.  
  
 The `compare` function is a pointer to a user-supplied routine that compares two array elements and returns a value specifying their relationship. The `compare` function also takes the pointer to the context as the first argument. `_lsearch_s` calls `compare` one or more times during the search, passing pointers to two array elements on each call. `compare` must compare the elements and then return either nonzero (meaning the elements are different) or 0 (meaning the elements are identical).  
  
 The `context` pointer can be useful if the searched data structure is part of an object and the `compare` function needs to access members of the object. For example, code in the `compare` function can cast the void pointer into the appropriate object type and access members of that object. The addition of the `context` pointer makes `_lsearch_s` more secure because additional context can be used to avoid reentrancy bugs associated with using static variables to make data available to the `compare` function.  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`_lsearch_s`|<search.h>|  
  
 For more compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## .NET Framework Equivalent  
 Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).  
  
## See Also  
 [Searching and Sorting](../vs140/Searching-and-Sorting.md)   
 [bsearch_s](../Topic/bsearch_s.md)   
 [_lfind_s](../Topic/_lfind_s.md)   
 [_lsearch](../vs140/_lsearch.md)