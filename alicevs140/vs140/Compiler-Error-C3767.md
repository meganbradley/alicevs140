---
title: "Compiler Error C3767"
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
ms.assetid: 5247cdcd-639c-4527-bd37-37e74c4e8fab
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3767
'function' candidate function(s) not accessible  
  
 A friend function defined in a class is not supposed to be treated as if it were defined and declared in the global namespace scope. It can, however, be found by argument-dependent lookup.  
  
 C3767 may also be caused by a breaking change: native types are now private by default in a **/clr** compilation; see [Type Visibility](../Topic/How%20to:%20Define%20and%20Consume%20Classes%20and%20Structs%20\(C++-CLI\).md#BKMK_Type_visibility) for more information.  
  
 The following sample generates C3767:  
  
```  
// C3767a.cpp  
// compile with: /clr  
using namespace System;  
public delegate void TestDel();  
  
public ref class MyClass {  
public:  
   static event TestDel^ MyClass_Event;  
};  
  
public ref class MyClass2 : public MyClass {  
public:  
   void Test() {  
      MyClass^ patient = gcnew MyClass;  
      patient->MyClass_Event();  
    }  
};  
  
int main() {  
   MyClass^ x = gcnew MyClass;  
   x->MyClass_Event();   // C3767  
  
   // OK  
   MyClass2^ y = gcnew MyClass2();  
   y->Test();  
};  
```  
  
 The following sample generates C3767:  
  
```  
// C3767b.cpp  
// compile with: /clr:oldSyntax  
using namespace System;  
__delegate void TestDel();  
  
public __gc class MyClass {  
public:  
   static __event TestDel * MyClass_Event;  
};  
  
public __gc class MyClass2 : public MyClass {  
public:  
   void Test() {  
      MyClass* patient = new MyClass;  
      patient->MyClass_Event();  
    }  
};  
  
int main() {  
   MyClass* x = new MyClass;  
   x->MyClass_Event();   // C3767  
  
   // OK  
   MyClass2 * y = new MyClass2();  
   y->Test();  
};  
```  
  
 The following sample generates C3767:  
  
```  
// C3767c.cpp  
// compile with: /clr /c  
  
ref class Base  {  
protected:  
   void Method() {  
      System::Console::WriteLine("protected");  
   }  
};  
  
ref class Der : public Base {  
   void Method() {  
      ((Base^)this)->Method();   // C3767  
      // try the following line instead  
      // Base::Method();  
   }  
};  
```  
  
 The following sample generates C3767:  
  
```  
// C3767d.cpp  
// compile with: /clr:oldSyntax /c  
  
__gc class Base {  
protected:  
   void Method() {  
      System::Console::WriteLine("protected");  
   }  
};  
  
__gc class Der : public Base {  
   void Method() {  
      ((Base*)this)->Method();   // C3767  
      // try the following line instead  
      // Base::Method();  
   }  
};  
```  
  
 In Visual C++ .NET 2002, the compiler changed the way it looked up symbols. In some cases, it would have automatically looked for symbols in a specified namespace. Now, it will use argument-dependent lookup.  
  
 The following sample generates C3767:  
  
```  
// C3767e.cpp  
namespace N {  
   class C {  
      friend void FriendFunc() {}  
      friend void AnotherFriendFunc(C* c) {}  
   };  
}  
  
int main() {  
   using namespace N;  
   FriendFunc();   // C3767 error  
   C* pC = new C();  
   AnotherFriendFunc(pC);   // found via argument-dependent lookup  
}  
```  
  
 For code that is valid in Visual C++ .NET 2003 and Visual C++ .NET 2002, declare the friend in class scope and define it in namespace scope:  
  
```  
// C3767f.cpp  
class MyClass {  
   int m_private;  
   friend void func();  
};  
  
void func() {  
   MyClass s;  
   s.m_private = 0;  
}  
  
int main() {  
   func();  
}  
```