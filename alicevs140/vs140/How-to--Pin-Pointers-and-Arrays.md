---
title: "How to: Pin Pointers and Arrays"
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
ms.topic: language-reference
ms.assetid: ee783260-e676-46b8-a38e-11a06f1d57b0
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Pin Pointers and Arrays
Pinning a sub-object defined in a managed object has the effect of pinning the entire object.  For example, if any element of an array is pinned, then the whole array is also pinned. There are no extensions to the language for declaring a pinned array. To pin an array, declare a pinning pointer to its element type, and pin one of its elements.  
  
## Example  
  
### Code  
  
```  
// pin_ptr_array.cpp  
// compile with: /clr  
#include <stdio.h>  
using namespace System;  
  
int main() {  
   array<Byte>^ arr = gcnew array<Byte>(4);  
   arr[0] = 'C';  
   arr[1] = '+';  
   arr[2] = '+';  
   arr[3] = '\0';  
   pin_ptr<Byte> p = &arr[1];   // entire array is now pinned  
   unsigned char * cp = p;  
  
   printf_s("%s\n", cp); // bytes pointed at by cp  
                         // will not move during call  
}  
```  
  
### Output  
  
```  
++  
```  
  
## See Also  
 [pin_ptr (C++/CLI)](../vs140/pin_ptr--C---CLI-.md)