---
title: "Compiler Warning (Level 1) C4789"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: error-reference
ms.assetid: 5800c301-5afb-4af0-85c1-ceb54d775234
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (Level 1) C4789
buffer 'identifier' of size N bytes will be overrun; M bytes will be written starting at offset L  
  
 Warns about buffer overrun when specific C run-time (CRT) functions are used, parameters are passed, and assignments are performed, such that the data sizes are known at compile time. This warning is for situations that might elude typical data-size mismatch detection.  
  
 The warning appears when data, whose length is known at compile time, is copied and put into a data block whose size is known at compile time to be too small for the data. The copy must be done by using the intrinsic form of one of the following CRT functions:  
  
-   [strcpy](../vs140/strcpy--wcscpy--_mbscpy.md)  
  
-   [memset](../vs140/memset--wmemset.md)  
  
-   [memcpy](../vs140/memcpy--wmemcpy.md), [wmemcpy](../vs140/memcpy--wmemcpy.md)  
  
 The warning also appears when a parameter datatype is mismatched by using a cast, and then a copy assignment from an lvalue reference is attempted.  
  
 Visual C++ might generate this warning for a code path that does not ever execute. You can temporarily disable the warning by using `#pragma`, as shown in this example:  
  
 `#pragma(push)`  
  
 `#pragma warning ( disable : 4789 )`  
  
 `// unused code that generates compiler warning C4789`  
  
 `#pragma(pop)`  
  
 This keeps Visual C++ from generating the warning for that specific block of code. The `#pragma(push)` preserves the existing state before `#pragma warning(disable: 4789)` changes it. The `#pragma(pop)` restores the pushed state, and removes the effects of the `#pragma warning(disable:4789)`. For more information about the C++ preprocessor directive `#pragma`, see [warning](../vs140/warning.md) and [Pragma Directives and the __Pragma Keyword](../vs140/Pragma-Directives-and-the-__Pragma-Keyword.md).  
  
## Example  
 The following sample generates C4789.  
  
```  
// C4789.cpp  
// compile with: /Oi /W1 /c  
#include <string.h>  
#include <stdio.h>  
  
int main()   
{  
    char a[20];  
    strcpy(a, "0000000000000000000000000\n");   // C4789  
  
    char buf2[20];  
    memset(buf2, 'a', 21);   // C4789  
  
    char c;  
    wchar_t w = 0;  
    memcpy(&c, &w, sizeof(wchar_t));  
}  
```  
  
## Example  
 The following sample also generates C4789.  
  
```  
// C4789b.cpp  
// compile with: /W1 /O2 /c  
// processor: x86  
short G;  
  
void main()  
{  
   int * p = (int *)&G;   
   *p = 3;   // C4789 - writes an int through a pointer to short  
}   
```