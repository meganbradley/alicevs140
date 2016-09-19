---
title: "Compiler Error C3754"
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
ms.assetid: 14b877bc-9277-40ec-af1c-196a58b45f10
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3754
delegate constructor: member function 'function' cannot be called on an instance of type 'type'  
  
 A call was made to a function through a pointer to a type that does not contain the function.  
  
 The following sample generates C3754:  
  
```  
// C3754a.cpp  
// compile with: /clr  
using namespace System;  
  
delegate void MyDel();  
  
interface class MyInterface {};  
  
ref struct MyClass : MyInterface {  
   void f() {}  
};  
  
int main() {  
   MyInterface^ p = gcnew MyClass;  
   MyDel^ q = gcnew MyDel(p, &MyClass::f);   // C3754  
   // try the following line instead  
//   MyDel^ q = gcnew MyDel(safe_cast<MyClass^>(p), &MyClass::f);  
}  
```  
  
 The following sample generates C3754:  
  
```  
// C3754b.cpp  
// compile with: /clr:oldSyntax  
#using <mscorlib.dll>  
using namespace System;  
  
__delegate void MyDel();  
  
__gc __interface MyInterface {};  
  
__gc struct MyClass : MyInterface {  
   void f() {}  
};  
  
int main() {  
   MyInterface* p = new MyClass;  
   MyDel* q = new MyDel(p, &MyClass::f);   // C3754  
   // try the following line instead  
   // MyDel* q = new MyDel(__try_cast<MyClass*>(p), &MyClass::f);  
}  
```