---
title: "Compiler Error C2879"
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
ms.assetid: ac92b645-2394-49de-8632-43d44e0553ed
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2879
'symbol' : only an existing namespace can be given an alternative name by a namespace alias definition  
  
 You cannot create a [namespace alias](../vs140/namespace-Alias.md) to a symbol other than a namespace.  
  
 The following sample generates C2879:  
  
```  
// C2879.cpp  
int main() {  
   int i;  
   namespace A = i;   // C2879 i is not a namespace  
}  
```