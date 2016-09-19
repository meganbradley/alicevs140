---
title: "Private Virtual Functions"
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
ms.assetid: 04448086-bf72-44be-9c1f-dfda1744949e
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Private Virtual Functions
The way private virtual functions are handled in derived classes has changed from Managed Extensions for C++ to [!INCLUDE[cpp_current_long](../vs140/includes/cpp_current_long_md.md)].  
  
 In Managed Extensions, the access level of a virtual function does not constrain its ability to be overridden within a derived class. In the new syntax, a virtual function cannot override a base class virtual function that it cannot access. For example:  
  
```  
__gc class MyBaseClass {  
   // inaccessible to a derived class   
   virtual void g();  
};  
  
__gc class MyDerivedClass : public MyBaseClass {  
public:  
   // okay in Managed Extensions; g() overrides MyBaseClass::g()  
   // error in new syntax; cannot override: MyBaseClass::g() is inaccessible …  
   void g();  
};  
```  
  
 There is no real mapping of this sort of design onto the new syntax. One simply has to make the base class members accessible – that is, non-private. The inherited methods do not have to bear the same access. In this example, the least invasive change is to make the MyBaseClass member `protected`. This way the general program's access to the method through MyBaseClass is still prohibited.  
  
```  
ref class MyBaseClass {  
protected:  
   virtual void g();  
};  
  
ref class MyDerivedClass : MyBaseClass {  
public:  
   virtual void g() override;  
};  
```  
  
 Note that the absence of the explicit `virtual` keyword in the base class, under the new syntax, generates a warning message.  
  
## See Also  
 [Member Declarations within a Class or Interface](../vs140/Member-Declarations-within-a-Class-or-Interface--C---CLI-.md)   
 [Member Visibility](../vs140/Member-Visibility.md)