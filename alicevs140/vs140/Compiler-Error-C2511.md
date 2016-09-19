---
title: "Compiler Error C2511"
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
ms.assetid: df999efe-fe2b-418b-bb55-4af6a0592631
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2511
'identifier' : overloaded member function not found in 'class'  
  
 No version of the function is declared with the specified parameters.  Possible causes:  
  
1.  Wrong parameters passed to function.  
  
2.  Parameters passed in wrong order.  
  
3.  Incorrect spelling of parameter names.  
  
 The following sample generates C2511:  
  
```  
// C2511.cpp  
// compile with: /c  
class C {  
   int c_2;  
   int Func(char *, char *);  
};  
  
int C::Func(char *, char *, int i) {   // C2511  
// try the following line instead  
// int C::Func(char *, char *) {  
   return 0;  
}  
```