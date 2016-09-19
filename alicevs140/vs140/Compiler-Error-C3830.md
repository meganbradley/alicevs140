---
title: "Compiler Error C3830"
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
ms.assetid: c9798f88-5001-4067-9fb1-09957ddc6fa8
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3830
'type1': cannot inherit from 'type2', value types can only inherit from interface classes  
  
 A value type cannot inherit a base class.  For more information, see [Classes and Structs (Managed)](../vs140/Classes-and-Structs---C---Component-Extensions-.md).  
  
 The following sample generates C3830:  
  
```  
// C3830a.cpp  
// compile with: /clr /c  
public value struct MyStruct4 {  
   int i;  
};  
  
public value class MyClass : public MyStruct4 {};   // C3830  
  
// OK  
public interface struct MyInterface4 {  
   void i();  
};  
  
public value class MyClass2 : public MyInterface4 {  
public:  
   virtual void i(){}  
};  
```  
  
 **Managed Extensions for C++**  
  
 A `__value` type cannot inherit a base class.  
  
 The following sample generates C3830:  
  
```  
// C3830b.cpp  
// compile with: /clr:oldSyntax /c  
#using <mscorlib.dll>  
__value struct v : public System::Object {};   // C3830  
__value struct w {};   // OK  
```