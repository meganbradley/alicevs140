---
title: "Compiler Error C3056"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 9500173d-870b-49b3-8e88-0ee93586d19a
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3056
'symbol' : symbol is not in the same scope with 'threadprivate' directive  
  
 A symbol used in a [threadprivate](../vs140/threadprivate.md) clause must be in the same scope as the `threadprivate` clause.  
  
 The following sample generates C3056:  
  
```  
// C3056.cpp  
// compile with: /openmp  
int x, y;  
void test() {  
   #pragma omp threadprivate(x, y)   // C3056  
   #pragma omp parallel copyin(x, y)  
   {  
      x = y;  
   }  
}  
```  
  
 Possible resolution:  
  
```  
// C3056b.cpp  
// compile with: /openmp /LD  
int x, y;  
#pragma omp threadprivate(x, y)  
void test() {  
   #pragma omp parallel copyin(x, y)  
   {  
      x = y;  
   }  
}  
```