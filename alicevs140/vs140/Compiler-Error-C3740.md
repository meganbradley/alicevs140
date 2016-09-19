---
title: "Compiler Error C3740"
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
ms.assetid: edb17a90-2307-4df6-943d-580460d26d2b
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3740
templates cannot source or receive events  
  
 A templated class or struct cannot contain [events](../vs140/Event-Handling.md).  
  
 The following sample generates C3740:  
  
```  
// C3740.cpp  
template <typename T>   // Delete the template specification  
struct E {  
   __event void f();   // C3740  
};  
  
int main() {  
}  
```