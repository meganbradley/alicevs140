---
title: "Compiler Error C3865"
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
ms.assetid: 9bc62bb0-4fb8-4856-a5cf-c7cb4029a596
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3865
'calling_convention' : can only be used on native member functions  
  
 A calling convention was used on a function that was either a global function or on a managed member function. The calling convention can only be used on a native (not managed) member function.  
  
 For more information, see [Calling Conventions](../vs140/Calling-Conventions.md).  
  
 The following sample generates C3865:  
  
```  
// C3865.cpp  
// compile with: /clr  
// processor: x86  
void __thiscall Func(){}   // C3865  
  
// OK  
struct MyType {  
   void __thiscall Func(){}  
};  
```