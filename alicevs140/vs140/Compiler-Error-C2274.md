---
title: "Compiler Error C2274"
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
ms.assetid: 8e874903-f499-45ef-8291-f821eee4cc1c
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2274
'type' : illegal as right side of '.' operator  
  
 A type appears as the right operand of a member-access (.) operator.  
  
 This error can be caused by trying to access a user-defined type conversion. Use the keyword `operator` between the period and `type`.  
  
 The following sample generates C2286:  
  
```  
// C2274.cpp  
struct MyClass {  
   operator int() {  
      return 0;  
   }  
};  
  
int main() {  
   MyClass ClassName;  
   int i = ClassName.int();   // C2274  
   int j = ClassName.operator int();   // OK  
}  
```