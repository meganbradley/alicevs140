---
title: "new (new slot in vtable)  (C++ Component Extensions)"
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
ms.topic: language-reference
ms.assetid: 1a9a5704-f02f-46ae-ad65-f0f2b6dbabc3
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# new (new slot in vtable)  (C++ Component Extensions)
The `new` keyword indicates that a virtual member will get a new slot in the vtable.  
  
> [!NOTE]
>  The `new` keyword has many uses and meanings. For more information, see the disambiguation topic [new](../vs140/new.md).  
  
## All Runtimes  
 (There are no remarks for this language feature that apply to all runtimes.)  
  
## Windows Runtime  
 Not supported in [!INCLUDE[wrt](../vs140/includes/wrt_md.md)].  
  
## [!INCLUDE[clr_for_headings](../vs140/includes/clr_for_headings_md.md)]  
 **Remarks**  
  
 In a **/clr** compilation, `new` indicates that a virtual member will get a new slot in the vtable; that the function does not override a base class method.  
  
 `new` causes the newslot modifier to be added to the IL for the function.  For more information about newslot, see:  
  
-   [MethodInfo.GetBaseDefinition Method](https://msdn.microsoft.com/en-us/library/system.reflection.methodinfo.getbasedefinition.aspx)  
  
-   [MethodAttributes Enumeration](https://msdn.microsoft.com/en-us/library/system.reflection.methodattributes.aspx)  
  
### Requirements  
 Compiler option: **/clr**  
  
### Examples  
 **Example**  
  
 The following sample shows the effect of `new`.  
  
```  
// newslot.cpp  
// compile with: /clr  
ref class C {  
public:  
   virtual void f() {  
      System::Console::WriteLine("C::f() called");  
   }  
  
   virtual void g() {  
      System::Console::WriteLine("C::g() called");  
   }  
};  
  
ref class D : public C {  
public:  
   virtual void f() new {  
      System::Console::WriteLine("D::f() called");  
   }  
  
   virtual void g() override {  
      System::Console::WriteLine("D::g() called");  
   }  
};  
  
ref class E : public D {  
public:  
   virtual void f() override {  
      System::Console::WriteLine("E::f() called");  
   }  
};  
  
int main() {  
   D^ d = gcnew D;  
   C^ c = gcnew D;  
  
   c->f();   // calls C::f  
   d->f();   // calls D::f  
  
   c->g();   // calls D::g  
   d->g();   // calls D::g  
  
   D ^ e = gcnew E;  
   e->f();   // calls E::f  
}  
```  
  
 **Output**  
  
 **C::f() called**   
 **D::f() called**   
 **D::g() called**   
 **D::g() called**   
 **E::f() called**   
## See Also  
 [Language Extensions for Runtime Platforms](../Topic/Component%20Extensions%20for%20Runtime%20Platforms.md)   
 [Override Specifiers](../vs140/Override-Specifiers---C---Component-Extensions-.md)