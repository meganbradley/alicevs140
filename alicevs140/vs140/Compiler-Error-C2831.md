---
title: "Compiler Error C2831"
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
ms.assetid: c8c04288-0889-4265-a077-17f94cbcdcc9
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2831
'operator operator' cannot have default parameters  
  
 Only three operators can have default parameters:  
  
-   [new](../vs140/new-Operator--C---.md)  
  
-   Assignment =  
  
-   Left parenthesis (  
  
 The following sample generates C2831:  
  
```  
// C2831.cpp  
// compile with: /c  
#define BINOP <=  
class A {  
public:  
   int i;  
   int operator BINOP(int x = 1) {   // C2831  
   // try the following line instead  
   // int operator BINOP(int x) {  
      return i+x;  
   }  
};  
```