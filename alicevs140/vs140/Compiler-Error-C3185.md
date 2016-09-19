---
title: "Compiler Error C3185"
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
ms.assetid: 5bf96279-043c-4981-9d02-b4550071b192
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3185
'typeid' used on managed or WinRT type 'type', use 'operator' instead  
  
 You cannot apply the [typeid](../Topic/typeid%20Operator.md) operator to a managed or WinRT type; use [typeid](../Topic/typeid%20%20\(C++%20Component%20Extensions\).md) instead.  
  
 The following sample generates C3185 and shows how to fix it:  
  
```  
// C3185a.cpp  
// compile with: /clr  
ref class Base {};  
ref class Derived : public Base {};  
  
int main() {  
   Derived ^ pd = gcnew Derived;  
   Base ^pb = pd;  
   const type_info & t1 = typeid(pb);   // C3185  
   System::Type ^ MyType = Base::typeid;   // OK  
};  
```  
  
 **Managed Extensions for C++**  
  
 You cannot apply [typeid](../Topic/typeid%20Operator.md) to a managed type; use [__typeof](../vs140/__typeof.md) instead.  
  
 The following sample generates C3185:  
  
```  
// C3185b.cpp  
// compile with: /clr:oldSyntax  
#using <mscorlib.dll>  
__gc class Base {};  
__gc class Derived : public Base {};  
  
int main() {  
   Derived *pd = new Derived;  
   Base *pb = pd;  
   const type_info & t1 = typeid(*pb);   // C3185  
  
   // OK  
   Type * t = __typeof(Base);  
   Type * t1 = __typeof(Derived);  
};  
```