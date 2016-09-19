---
title: "operator new(CRT)"
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
  - msvcr110_clr0400.dll
  - msvcr100.dll
  - msvcr120.dll
  - msvcr110.dll
  - msvcr80.dll
  - msvcr90.dll
apitype: DLLExport
ms.assetid: 79682f85-6889-40f6-b8f7-9eed5176ea35
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# operator new(CRT)
Allocate block of memory from heap  
  
## Syntax  
  
```  
  
      void *__cdecl operator new[](size_t count);  
void *__cdecl operator new[] (  
   size_t count,   
   void * object  
) throw();  
void *__cdecl operator new[] (  
   size_t count,   
   const std::nothrow_t&  
) throw();  
```  
  
#### Parameters  
 *count*  
 The size of the allocation.  
  
 *object*  
 A pointer to a block of memory in which the object will be created.  
  
## Return Value  
 A pointer to the lowest byte address of the newly allocated storage.  
  
## Remarks  
 This form of `operator new` is known as vector new, in contrast to the scalar new form ([operator new](../vs140/operator-new--CRT-.md)).  
  
 The first form of this operator is known as the nonplacement form. The second form of this operator is known as the placement form and the third form of this operator is the nonthrowing placement form.  
  
 The first form of the operator is defined by the compiler and does not require new.h to be included in your program.  
  
 [operator delete&#91;&#93;](../vs140/operator-delete--new--.md) frees memory allocated with operator new.  
  
 You can configure whether `operator new[]` returns null or throws an exception on failure. See [The new and delete Operators](../vs140/new-and-delete-Operators.md) for more information.  
  
 With the exception of throwing or no-throwing behavior, the CRT `operator new` behaves like [operator new&#91;&#93;](../vs140/operator-new--new--.md) in the Standard C++ Library.  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`new[]`|<new.h>|  
  
 For additional compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## Libraries  
 All versions of the [C run-time libraries](../vs140/CRT-Library-Features.md).  
  
## Example  
 The following shows how to use the vector, nonplacement form of `operator new`.  
  
```  
// crt_new4.cpp  
#include <stdio.h>  
int main() {  
   int * k = new int[10];  
   k[0] = 21;  
   printf("%d\n", k[0]);  
   delete [] k;  
}  
```  
  
 The following shows how to use the vector, placement form of `operator new`.  
  
```  
// crt_new5.cpp  
#include <stdio.h>  
#include <new.h>  
int main() {  
   int * i = new int[10];  
   i[0] = 21;  
   printf("%d\n", i[0]);  
   // initialize existing memory (i) with, in this case, int[[10]  
   int * j = new(i) int[10];   // placement vector new  
   printf("%d\n", j[0]);  
   j[0] = 22;  
   printf("%d\n", i[0]);  
   delete [] i;   // or, could have deleted [] j   
}  
```  
  
 The following shows how to use the vector, placement, no-throw form of `operator new`.  
  
```  
// crt_new6.cpp  
#include <stdio.h>  
#include <new.h>  
int main() {  
   int * k = new(std::nothrow) int[10];  
   k[0] = 21;  
   printf("%d\n", k[0]);  
   delete [] k;  
}  
```  
  
## See Also  
 [Memory Allocation](../vs140/Memory-Allocation.md)