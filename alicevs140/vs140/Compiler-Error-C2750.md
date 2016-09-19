---
title: "Compiler Error C2750"
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
ms.assetid: 30450034-feb5-448c-9655-b8c5f3639695
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2750
'type' : cannot use 'new' on the reference type; use 'gcnew' instead  
  
 To create an instance of a CLR type, which causes the instance to be placed on the garbage-collected heap, you must use [gcnew](../vs140/ref-new--gcnew---C---Component-Extensions-.md).  
  
 The following sample generates C2750:  
  
```  
// C2750.cpp  
// compile with: /clr  
ref struct Y1 {};  
  
int main() {  
   Y1 ^ x = new Y1;   // C2750  
  
   // try the following line instead  
   Y1 ^ x2 = gcnew Y1;  
}  
```