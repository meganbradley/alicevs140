---
title: "Compiler Error C3891"
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
ms.assetid: 6e1a9458-97f5-4580-bc0f-aa97a1bfd20d
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3891
'var' : a literal data member cannot be used as a l-value  
  
 A [literal](../vs140/literal--C---Component-Extensions-.md) variable is const, and its value cannot be changed after it is initialized in the declaration.  
  
 The following sample generates C3891:  
  
```  
// C3891.cpp  
// compile with: /clr  
ref struct Y1 {  
   literal int staticConst = 9;  
};  
  
int main() {  
   Y1::staticConst = 0;   // C3891  
}  
```