---
title: "Compiler Error C2270"
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
ms.assetid: b52c068e-0b61-42e7-b775-4d57b3ddcba0
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2270
'function' : modifiers not allowed on nonmember functions  
  
 A nonmember function is declared with [const](../vs140/const--C---.md), [volatile](../vs140/volatile--C---.md), or another memory-model modifier.  
  
 The following sample generates C2270:  
  
```  
// C2270.cpp  
// compile with: /c  
void func1(void) const;   // C2270, nonmember function  
  
void func2(void);  
  
class CMyClass {  
public:  
   void func2(void) const;  
};  
```