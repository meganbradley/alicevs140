---
title: "Compiler Error C2765"
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
ms.assetid: 47ad86f3-a7e0-47ad-85ff-0f5534458cb9
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2765
'function' : an explicit specialization of a function template cannot have any default arguments  
  
 Default arguments are not allowed on an explicit specialization of a function template. For more information, see [Explicit Specialization of Function Templates](../vs140/Explicit-Specialization-of-Function-Templates.md).  
  
 The following sample generates C2765:  
  
```  
// C2765.cpp  
template<class T> void f(T t) {};  
  
template<> void f<char>(char c = 'a') {}   // C2765  
// try the following line instead  
// template<> void f<char>(char c) {}  
```