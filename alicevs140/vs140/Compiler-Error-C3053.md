---
title: "Compiler Error C3053"
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
ms.assetid: ab9a25f3-e341-4f6e-8e69-069b4a963a64
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3053
'symbol' : 'threadprivate' is only valid for global or static data items  
  
 Symbols passed to [threadprivate](../vs140/threadprivate.md) must either be global or static.  
  
 The following sample generates C3053:  
  
```  
// C3053.cpp  
// compile with: /openmp  
void Test() {  
   int x, y;  
   #pragma omp threadprivate(x, y)   // C3053  
   #pragma omp parallel copyin(x, y)  
   {  
      x = y;  
   }  
}  
```  
  
 Possible resolution:  
  
```  
// C3053b.cpp  
// compile with: /openmp /LD  
int x, y;  
#pragma omp threadprivate(x, y)  
  
void Test() {  
   #pragma omp parallel copyin(x, y)  
   {  
      x = y;  
   }  
}  
```