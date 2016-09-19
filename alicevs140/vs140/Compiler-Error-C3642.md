---
title: "Compiler Error C3642"
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
ms.assetid: 429790c2-9614-4d85-b31c-687c8d8f83ff
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3642
'return_type/args' : cannot call a function with __clrcall calling convention from native code  
  
 A function that is marked with the [__clrcall](../Topic/__clrcall.md) calling convention cannot be called from native (unmanaged) code.  
  
 *return_type/args* is either the name of the function or the type of the `__clrcall` function you are trying to call.  A type is used when you're calling through a function-pointer.  
  
 To call a managed function from a native context, you can add a "wrapper" function that will call the `__clrcall` function. Or, you can use the CLR marshalling mechanism; see [How to: Marshal Function Pointers using PInvoke](../Topic/How%20to:%20Marshal%20Function%20Pointers%20Using%20PInvoke.md) for more information.  
  
 The following sample generates C3642:  
  
```  
// C3642.cpp  
// compile with: /clr  
using namespace System;  
struct S {  
   void Test(String ^ s) {   // CLR type in signature, implicitly __clrcall  
      Console::WriteLine(s);  
   }  
   void Test2(char * s) {  
      Test(gcnew String(s));  
   }  
};  
  
#pragma unmanaged  
int main() {  
   S s;  
   s.Test("abc");   // C3642  
   s.Test2("abc");   // OK  
}  
```