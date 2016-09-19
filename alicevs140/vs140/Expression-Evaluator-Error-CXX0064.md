---
title: "Expression Evaluator Error CXX0064"
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
ms.assetid: aa509e71-0616-41ca-a94e-6c376b041e57
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Expression Evaluator Error CXX0064
can't set breakpoint on bound virtual member function  
  
 A breakpoint was set on a virtual member function through a pointer to an object, such as:  
  
```  
pClass->vfunc( int );  
```  
  
 A breakpoint can be set on a virtual function by entering the class, such as:  
  
```  
Class::vfunc( int );  
```  
  
 This error is identical to CAN0064.