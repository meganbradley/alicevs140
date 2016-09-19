---
title: "Compiler Error C3068"
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
ms.assetid: 613e3447-b4a8-4268-a661-297bed63ccdf
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3068
'function' : a 'naked' function cannot contain objects that would require unwinding if a C++ exception occurred  
  
 The compiler was unable to perform stack unwinding on a [naked](../vs140/naked--C---.md) function that threw an exception because a temporary object was created in the function and C++ exception handling ([/EHsc](../vs140/-EH--Exception-Handling-Model-.md)) was specified.  
  
 To resolve this error, do at least one of the following:  
  
-   Do not compile with /EHsc.  
  
-   Do not mark the function as `naked`.  
  
-   Do not create a temporary object in the function.  
  
 If a function creates a temporary object on the stack, if the function throws an exception, and if C++ exception handling is enabled, the compiler will clean up the stack if an exception is thrown.  
  
 When an exception is thrown, compiler generated code, called the prolog and epilog and which are not present in a naked function, is executed for a function.  
  
## Example  
 The following sample generates C3068:  
  
```  
// C3068.cpp  
// compile with: /EHsc  
// processor: x86  
class A {  
public:  
   A(){}  
   ~A(){}  
};  
  
void b(A){}  
  
__declspec(naked) void c() {  
   b(A());   // C3068   
};  
```