---
title: "Compiler Error C3010"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e959d038-bba6-432a-9c0a-0470474de7d9
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3010
'label' : jump out of OpenMP structured block not allowed  
  
 Code cannot jump into or out of an OpenMP block.  
  
 The following sample generates C3010:  
  
```  
// C3010.c  
// compile with: /openmp  
int main() {  
   #pragma omp parallel   
   {  
      #pragma omp parallel  
      {  
         goto lbl3;  
      }  
   }  
   lbl3:;   // C3010  
}  
```