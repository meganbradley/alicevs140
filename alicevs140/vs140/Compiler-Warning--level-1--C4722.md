---
title: "Compiler Warning (level 1) C4722"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d8660710-f67b-4f59-a5fd-59259475529e
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 1) C4722
'function' : destructor never returns, potential memory leak  
  
 The flow of control terminates in a destructor. The thread or the entire program will terminate and allocated resources may not be released.  Furthermore, if a destructor will be called for stack unwinding during exception processing, the behavior of executable is undefined.  
  
 To resolve, remove the function call that causes the destructor to not return.  
  
## Example  
 The following sample generates C4722:  
  
```  
// C4722.cpp  
// compile with: /O1 /W1 /c  
#include <stdlib.h>  
class C {  
public:  
   C();  
   ~C() { exit(1); };   // C4722  
};  
  
extern void func (C*);  
  
void Test(){  
   C x;  
   func(&x);  
   // control will not leave Test because destructor will exit  
}  
```