---
title: "_countof Macro"
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
apilocation: 
  - msvcr80.dll
  - msvcr100.dll
  - msvcr120.dll
  - msvcr90.dll
  - msvcr110.dll
  - msvcr110_clr0400.dll
apitype: DLLExport
ms.assetid: 86198767-f7e5-4beb-898d-3cbbf60350a3
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _countof Macro
Compute the number of elements in a statically-allocated array.  
  
## Syntax  
  
```  
size_t _countof(   
   array  
);  
```  
  
#### Parameters  
 `array`  
 The name of an array.  
  
## Return Value  
 The number of elements in the array, expressed as a `size_t`.  
  
## Remarks  
 Ensure that `array` is actually an array, not a pointer. In C, `_countof` will produce erroneous results if `array` is a pointer. In C++, `_countof` will fail to compile if `array` is a pointer.  
  
## Requirements  
  
|Macro|Required header|  
|-----------|---------------------|  
|`_countof`|<stdlib.h>|  
  
## Example  
  
```  
// crt_countof.cpp  
#define _UNICODE  
#include <stdio.h>  
#include <stdlib.h>  
#include <tchar.h>  
  
int main( void )  
{  
   _TCHAR arr[20], *p;  
   printf( "sizeof(arr) = %zu bytes\n", sizeof(arr) );  
   printf( "_countof(arr) = %zu elements\n", _countof(arr) );  
   // In C++, the following line would generate a compile-time error:  
   // printf( "%zu\n", _countof(p) ); // error C2784 (because p is a pointer)  
  
   _tcscpy_s( arr, _countof(arr), _T("a string") );  
   // unlike sizeof, _countof works here for both narrow- and wide-character strings  
}  
```  
  
 **sizeof(arr) = 40 bytes**  
**_countof(arr) = 20 elements**   
## See Also  
 [sizeof Operator](../vs140/sizeof-Operator.md)