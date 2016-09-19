---
title: "Compiler Error C2739"
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
ms.assetid: 5b63e435-7631-43d7-805e-f2adefb7e517
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2739
'number' : explicit managed or WinRT array dimensions must be between 1 and 32  
  
 An array dimension was not between 1 and 32.  
  
 The following sample generates C2739 and shows how to fix it:  
  
```  
// C2739.cpp  
// compile with: /clr  
int main() {  
   array<int, -1>^a;   // C2739  
   // try the following line instead  
   // array<int, 2>^a;  
}  
```