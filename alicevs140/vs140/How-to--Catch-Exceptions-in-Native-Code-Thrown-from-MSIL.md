---
title: "How to: Catch Exceptions in Native Code Thrown from MSIL"
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
ms.topic: article
ms.assetid: c15afd2b-8505-43bf-8a4a-f1d41532a124
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Catch Exceptions in Native Code Thrown from MSIL
In native code, you can catch native C++ exception from MSIL.  You can catch CLR exceptions with `__try` and `__except`.  
  
 For more information, see [Structured Exception Handling (C++)](../vs140/Structured-Exception-Handling--C-C---.md) and [C++ Exception Handling](../vs140/C---Exception-Handling.md).  
  
## Example  
 The following sample defines a module with two functions, one that throws a native exception, and another that throws an MSIL exception.  
  
```  
// catch_MSIL_in_native.cpp  
// compile with: /clr /c  
void Test() {  
   throw ("error");  
}  
  
void Test2() {  
   throw (gcnew System::Exception("error2"));  
}  
```  
  
## Example  
 The following sample defines a module that catches a native and MSIL exception.  
  
```  
// catch_MSIL_in_native_2.cpp  
// compile with: /clr catch_MSIL_in_native.obj  
#include <iostream>  
using namespace std;  
void Test();  
void Test2();  
  
void Func() {  
   // catch any exception from MSIL  
   // should not catch Visual C++ exceptions like this  
   // runtime may not destroy the object thrown  
   __try {  
      Test2();  
   }  
   __except(1) {  
      cout << "caught an exception" << endl;  
   }  
  
}  
  
int main() {  
   // catch native C++ exception from MSIL  
   try {  
      Test();  
   }  
   catch(char * S) {  
      cout << S << endl;  
   }  
   Func();  
}  
```  
  
 **error**  
**caught an exception**   
## See Also  
 [Exception Handling under /clr](../vs140/Exception-Handling---C---Component-Extensions-.md)