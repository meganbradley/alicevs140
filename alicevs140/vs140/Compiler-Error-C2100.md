---
title: "Compiler Error C2100"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: error-reference
ms.assetid: 9ed5ea11-9d55-4ddf-8b1a-162c74f3c390
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2100
illegal indirection  
  
 Indirection operator ( `*` ) is applied to a nonpointer value.  
  
 The following sample generates C2100:  
  
```  
// C2100.cpp  
int main() {  
   int r = 0, *s = 0;  
   s = &r;  
   *r = 200;   // C2100  
   *s = 200;   // OK  
}  
```