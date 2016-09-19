---
title: "Compiler Error C3033"
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
ms.assetid: 8628b6bb-a650-4ed2-af13-57acd2f7ddbb
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3033
'var' : variable in 'clause' clause cannot have const-qualified type  
  
 Values passed to certain clauses cannot be `const` variables.  
  
 The following sample generates C3033:  
  
```  
// C3033.cpp  
// compile with: /openmp /link vcomps.lib  
int main() {  
   const int val = 1;  
   int val2 = 1;  
  
   #pragma omp parallel reduction(+ : val)   // C3033  
   ;  
  
   #pragma omp parallel reduction(+ : val2)   // OK  
   ;  
}  
```