---
title: "interface class  (C++ Component Extensions)"
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
ms.assetid: 3ccea701-f50b-4da7-ad6b-f0ee1203e2b9
caps.latest.revision: 30
translation.priority.ht: 
  - de-de
  - ja-jp
---
# interface class  (C++ Component Extensions)
Declares an interface.  For information on native interfaces, see [__interface](../vs140/__interface.md).  
  
## All Runtimes  
 **Syntax**  
  
```  
  
interface_access  
interface class  
 name :  inherit_accessbase_interface{};interface_accessinterface structname :  inherit_accessbase_interface{};  
```  
  
 **Parameters**  
  
 *interface_access*  
 The accessibility of an interface outside the assembly.  Possible values are **public** and `private`.  `private` is the default.  Nested interfaces cannot have an *interface_access* specifier.  
  
 *name*  
 The name of the interface.  
  
 *inherit_access*  
 The accessibility of *base_interface*.  The only permitted accessibility for a base interface is `public` (the default).  
  
 *base_interface* (optional)  
 A base interface for interface *name*.  
  
 **Remarks**  
  
 **interface struct** is equivalent to **interface class**.  
  
 An interface can contain declarations for functions, events, and properties.  All interface members have public accessibility. An interface can also contain static data members, functions, events, and properties, and these static members must be defined in the interface.  
  
 An interface defines how a class may be implemented. An interface is not a class and classes can only implement interfaces. When a class defines a function declared in an interface, the function is implemented, not overridden. Therefore, name lookup does not include interface members.  
  
 A class or struct that derives from an interface must implement all members of the interface. When implementing interface *name* you must also implement the interfaces in the `base_interface` list.  
  
 For more information, see:  
  
-   [Interface Static Constructor](../vs140/How-to--Define-an-Interface-Static-Constructor--C---CLI-.md)  
  
-   [Generic Interfaces (C++)](../vs140/Generic-Interfaces--Visual-C---.md)  
  
 For information on other CLR types, see [Classes and Structs](../vs140/Classes-and-Structs---C---Component-Extensions-.md).  
  
 You can detect at compile time if a type is an interface with `__is_interface_class(``type``)`. For more information, see [Intrinsic Support for Type Traits](../vs140/Compiler-Support-for-Type-Traits--C---Component-Extensions-.md).  
  
 In the development environment, you can get F1 help on these keywords by highlighting the keyword, (`interface class`, for example) and pressing F1.  
  
## [!INCLUDE[wrt](../vs140/includes/wrt_md.md)]  
 **Remarks**  
  
 (There are no remarks for this language feature that apply to only the Windows Runtime.)  
  
### Requirements  
 Compiler option: **/ZW**  
  
## [!INCLUDE[clr_for_headings](../vs140/includes/clr_for_headings_md.md)]  
 **Remarks**  
  
 (There are no remarks for this language feature that apply to only the common language runtime.)  
  
### Requirements  
 Compiler option: **/clr**  
  
### Examples  
 **Example**  
  
 The following code example demonstrates how an interface can define the behavior of a clock function.  
  
```  
// mcppv2_interface_class.cpp  
// compile with: /clr  
using namespace System;  
  
public delegate void ClickEventHandler(int, double);  
  
// define interface with nested interface  
public interface class Interface_A {  
   void Function_1();  
  
   interface class Interface_Nested_A {  
      void Function_2();  
   };  
};  
  
// interface with a base interface  
public interface class Interface_B : Interface_A {  
   property int Property_Block;  
   event ClickEventHandler^ OnClick;     
   static void Function_3() { Console::WriteLine("in Function_3"); }  
};  
  
// implement nested interface  
public ref class MyClass : public Interface_A::Interface_Nested_A {  
public:  
   virtual void Function_2() { Console::WriteLine("in Function_2"); }  
};  
  
// implement interface and base interface  
public ref class MyClass2 : public Interface_B {  
private:  
   int MyInt;  
  
public:  
   // implement non-static function  
   virtual void Function_1() { Console::WriteLine("in Function_1"); }  
  
   // implement property  
   property int Property_Block {  
      virtual int get() { return MyInt; }  
      virtual void set(int value) { MyInt = value; }  
   }  
   // implement event  
   virtual event ClickEventHandler^ OnClick;  
  
   void FireEvents() {  
      OnClick(7, 3.14159);  
   }  
};  
  
// class that defines method called when event occurs  
ref class EventReceiver {  
public:  
   void OnMyClick(int i, double d) {  
      Console::WriteLine("OnClick: {0}, {1}", i, d);  
   }  
};  
  
int main() {  
   // call static function in an interface  
   Interface_B::Function_3();  
  
   // instantiate class that implements nested interface  
   MyClass ^ x = gcnew MyClass;  
   x->Function_2();  
  
   // instantiate class that implements interface with base interface  
   MyClass2 ^ y = gcnew MyClass2;  
   y->Function_1();  
   y->Property_Block = 8;  
   Console::WriteLine(y->Property_Block);  
  
   EventReceiver^ MyEventReceiver = gcnew EventReceiver();  
  
   // hook handler to event  
   y->OnClick += gcnew ClickEventHandler(MyEventReceiver, &EventReceiver::OnMyClick);  
  
   // invoke events  
   y->FireEvents();  
  
   // unhook handler to event  
   y->OnClick -= gcnew ClickEventHandler(MyEventReceiver, &EventReceiver::OnMyClick);  
  
   // call implemented function via interface handle  
   Interface_A^ hi = gcnew MyClass2();  
   hi->Function_1();  
}  
```  
  
 **Output**  
  
 **in Function_3**   
 **in Function_2**   
 **in Function_1**   
 **8**   
 **OnClick: 7, 3.14159**   
 **in Function_1** **Example**  
  
 The following code sample shows two ways to implement functions with the same signature declared in multiple interfaces and where those interfaces are used by a class.  
  
```  
// mcppv2_interface_class_2.cpp  
// compile with: /clr /c  
interface class I {  
   void Test();  
   void Test2();  
};  
  
interface class J : I {  
   void Test();  
   void Test2();  
};  
  
ref struct R : I, J {  
   // satisfies the requirement to implement Test in both interfaces  
   virtual void Test() {}  
  
   // implement both interface functions with explicit overrides  
   virtual void A() = I::Test2 {}  
   virtual void B() = J::Test2 {}  
};  
```  
  
## See Also  
 [Language Extensions for Runtime Platforms](../Topic/Component%20Extensions%20for%20Runtime%20Platforms.md)