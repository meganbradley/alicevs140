---
title: "protected (C++)"
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
ms.assetid: 863d299f-fc0d-45d5-a1a7-bd24b7778a93
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# protected (C++)
## Syntax  
  
```  
protected:  
   [member-list]  
protected base-class  
```  
  
## Remarks  
 The `protected` keyword specifies access to class members in the *member-list* up to the next access specifier (**public** or `private`) or the end of the class definition. Class members declared as `protected` can be used only by the following:  
  
-   Member functions of the class that originally declared these members.  
  
-   Friends of the class that originally declared these members.  
  
-   Classes derived with public or protected access from the class that originally declared these members.  
  
-   Direct privately derived classes that also have private access to protected members.  
  
 When preceding the name of a base class, the `protected` keyword specifies that the public and protected members of the base class are protected members of its derived classes.  
  
 Protected members are not as private as `private` members, which are accessible only to members of the class in which they are declared, but they are not as public as **public** members, which are accessible in any function.  
  
 Protected members that are also declared as **static** are accessible to any friend or member function of a derived class. Protected members that are not declared as **static** are accessible to friends and member functions in a derived class only through a pointer to, reference to, or object of the derived class.  
  
 For related information, see [friend](../vs140/friend--C---.md), [public](../vs140/public--C---.md), [private](../vs140/private--C---.md), and the member-access table in [Controlling Access to Class Members](../vs140/Controlling-Access-to-Class-Members.md).  
  
## /clr Specific  
 In CLR types, the C++ access specifier keywords (**public**, `private`, and `protected`) can affect the visibility of types and methods with regard to assemblies. For more information, see [Type and Member Visibility](../vs140/Type-and-Member-Visibility.md).  
  
> [!NOTE]
>  Files compiled with [/LN](../vs140/-LN--Create-MSIL-Module-.md) are not affected by this behavior. In this case, all managed classes (either public or private) will be visible.  
  
## END /clr Specific  
  
## Example  
  
```  
// keyword_protected.cpp  
// compile with: /EHsc  
#include <iostream>  
  
using namespace std;  
class X {  
public:  
   void setProtMemb( int i ) { m_protMemb = i; }  
   void Display() { cout << m_protMemb << endl; }  
protected:  
   int  m_protMemb;  
   void Protfunc() { cout << "\nAccess allowed\n"; }  
} x;  
  
class Y : public X {  
public:  
   void useProtfunc() { Protfunc(); }  
} y;  
  
int main() {  
   // x.m_protMemb;         error, m_protMemb is protected  
   x.setProtMemb( 0 );   // OK, uses public access function  
   x.Display();  
   y.setProtMemb( 5 );   // OK, uses public access function  
   y.Display();  
   // x.Protfunc();         error, Protfunc() is protected  
   y.useProtfunc();      // OK, uses public access function  
                        // in derived class  
}  
```  
  
## See Also  
 [Controlling Access to Class Members](../vs140/Controlling-Access-to-Class-Members.md)   
 [Keywords](../vs140/Keywords--C---.md)