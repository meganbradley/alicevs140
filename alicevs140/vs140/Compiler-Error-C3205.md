---
title: "Compiler Error C3205"
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
ms.assetid: 802d306e-5ff3-4491-8a22-c5f1c072d005
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3205
argument list for template parameter 'parameter' is missing  
  
 A [template](../vs140/Template-Specifications.md) parameter is missing.  
  
 The following sample generates C3205:  
  
```  
// C3205.cpp  
template<template<class> class T> struct A {  
   typedef T unparameterized_type;   // C3205  
   // try the following line instead  
   // typedef T<int> unparameterized_type;  
};  
  
template <class T>  
struct B {  
   typedef int value_type;  
};  
  
int main() {  
   A<B> x;  
}  
```