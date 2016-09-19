---
title: "Compiler Error C3895"
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
ms.assetid: 771b9fe5-d6d4-4297-bf57-e2f857722155
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3895
'var' : type data members cannot be 'volatile'  
  
 Certain kinds of data members, for example [literal](../vs140/literal--C---Component-Extensions-.md) or [initonly](../vs140/initonly--C---CLI-.md), cannot be [volatile (C++)](../vs140/volatile--C---.md).  
  
 The following sample generates C3895:  
  
```  
// C3895.cpp  
// compile with: /clr  
ref struct Y1 {  
   initonly  
   volatile int data_var2;   // C3895  
};  
```