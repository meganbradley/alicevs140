---
title: "Compiler Error C3149"
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
ms.assetid: cf6e2616-2f06-46da-8a8a-d449cb481c51
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3149
'type' : cannot use this type here without a top-level 'char'  
  
 A declaration was not specified correctly.  
  
 For example, you may have defined a CLR type at global scope and tried to create a variable of the type as part of the definition. Because global variables of CLR types are not allowed, the compiler will generate C3149.  
  
 To resolve this error, declare variables of CLR types inside a function or type definition.  
  
 The following sample generates C3149:  
  
```  
// C3149.cpp  
// compile with: /clr  
using namespace System;  
int main() {  
   // declare an array of value types   
   array< Int32 ^> IntArray;   // C3149  
   array< Int32>^ IntArray2;   // OK  
}  
```  
  
 The following sample generates C3149:  
  
```  
// C3149b.cpp  
// compile with: /clr /c  
delegate int MyDelegate(const int, int);  
void Test1(MyDelegate m) {}   // C3149  
void Test2(MyDelegate ^ m) {}   // OK  
```  
  
 **Managed Extensions for C++**  
  
 A managed object was not used correctly.  
  
 The following sample generates C3149:  
  
```  
// C3149c.cpp  
// compile with: /clr:oldSyntax  
__gc class A {};  
  
int main() {  
   A a = new A;   // C3149  
   A *a = new A;   // OK  
}  
```