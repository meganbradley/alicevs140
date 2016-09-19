---
title: "Explicit Override of an Interface Member"
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
ms.assetid: 46f1f536-bf43-4311-9a17-ff2282e528a9
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Explicit Override of an Interface Member
The syntax for declaring an explicit override of an interface member within a class has changed from Managed Extensions for C++ to [!INCLUDE[cpp_current_long](../vs140/includes/cpp_current_long_md.md)].  
  
 You often want to provide two instances of an interface member within a class that implements the interface – one that is used when class objects are manipulated through an interface handle, and one that is used when class objects are used through the class interface. For example:  
  
```  
public __gc class R : public ICloneable {  
   // to be used through ICloneable  
   Object* ICloneable::Clone();  
  
   // to be used through an R  
   R* Clone();  
};  
```  
  
 In Managed Extensions we do this by providing an explicit declaration of the interface method with the method's name qualified with the name of the interface. The class-specific instance is unqualified. This eliminates the need to downcast the return value of `Clone`, in this example, when explicit called through an instance of `R`.  
  
 In the new syntax, a general overriding mechanism has been introduced that replaces the Managed Extensions syntax. Our example would be rewritten as follows:  
  
```  
public ref class R : public ICloneable {  
public:  
   // to be used through ICloneable  
   virtual Object^ InterfaceClone() = ICloneable::Clone;  
  
   // to be used through an R  
   virtual R^ Clone();  
};  
```  
  
 This revision requires that the interface member being explicitly overridden be given a unique name within the class. Here, I've provided the awkward name of `InterfaceClone`. The behavior is still the same – an invocation through the `ICloneable` interface invokes the renamed `InterfaceClone,` while a call through an object of type `R` invokes the second `Clone` instance.  
  
## See Also  
 [Member Declarations within a Class or Interface](../vs140/Member-Declarations-within-a-Class-or-Interface--C---CLI-.md)   
 [Explicit Overrides](../vs140/Explicit-Overrides---C---Component-Extensions-.md)