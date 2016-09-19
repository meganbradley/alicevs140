---
title: "Compiler Error C3899"
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
ms.assetid: 14e07e4a-f7a7-4309-baaa-649d69e12e23
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3899
'var' : l-value use of initonly data member is not allowed directly within a parallel region in class 'class'  
  
 An [initonly](../vs140/initonly--C---CLI-.md) data member cannot be initialized inside that part of a constructor that is in a [parallel](../vs140/parallel.md) region.  This is because the compiler does an internal relocation of that code, such that, it is effectively no longer part of the constructor.  
  
 To resolve, initialize the initonly data member in the constructor, but outside the parallel region.  
  
## Example  
 The following sample generates C3899.  
  
```  
// C3899.cpp  
// compile with: /clr /openmp  
#include <omp.h>   
  
public ref struct R {  
   initonly int x;  
   R() {  
      x = omp_get_thread_num() + 1000;   // OK  
      #pragma omp parallel num_threads(5)  
      {  
         // cannot assign to 'x' here  
         x = omp_get_thread_num() + 1000;   // C3899  
         System::Console::WriteLine("thread {0}", omp_get_thread_num());  
      }  
      x = omp_get_thread_num() + 1000;   // OK  
   }  
};  
  
int main() {  
   R^ r = gcnew R;  
   System::Console::WriteLine(r->x);  
}  
```