---
title: "Compiler Error C2756"
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
ms.assetid: 42eb988d-4043-4dee-8fd4-596949f69a55
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2756
'template type' : default template arguments not allowed on a partial specialization  
  
 The template for a partial specialization may not contain a default argument.  
  
 The following sample generates C2756 and shows how to fix it:  
  
```  
// C2756.cpp  
template <class T>  
struct S {};  
  
template <class T=int>  
// try the following line instead  
// template <class T>  
struct S<T*> {};   // C2756  
```