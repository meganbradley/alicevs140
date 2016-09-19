---
title: "public (C++)"
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
ms.assetid: f3e10a59-39f6-4bcd-827e-3e99f8f89497
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# public (C++)
## Syntax  
  
```  
public:  
   [member-list]  
public base-class  
```  
  
## Remarks  
 When preceding a list of class members, the **public** keyword specifies that those members are accessible from any function. This applies to all members declared up to the next access specifier or the end of the class.  
  
 When preceding the name of a base class, the **public** keyword specifies that the public and protected members of the base class are public and protected members, respectively, of the derived class.  
  
 Default access of members in a class is private. Default access of members in a structure or union is public.  
  
 Default access of a base class is private for classes and public for structures. Unions cannot have base classes.  
  
 For more information, see [private](../vs140/private--C---.md), [protected](../vs140/protected--C---.md), [friend](../vs140/friend--C---.md), and the member-access table in [Controlling Access to Class Members](../vs140/Controlling-Access-to-Class-Members.md).  
  
## /clr Specific  
 In CLR types, the C++ access specifier keywords (**public**, `private`, and `protected`) can affect the visibility of types and methods with regard to assemblies. For more information, see [Type and Member Visibility](../vs140/Type-and-Member-Visibility.md).  
  
> [!NOTE]
>  Files compiled with [/LN](../vs140/-LN--Create-MSIL-Module-.md) are not affected by this behavior. In this case, all managed classes (either public or private) will be visible.  
  
## END /clr Specific  
  
## Example  
  
```  
// keyword_public.cpp  
class BaseClass {  
public:  
   int pubFunc() { return 0; }  
};  
  
class DerivedClass : public BaseClass {};  
  
int main() {  
   BaseClass aBase;  
   DerivedClass aDerived;  
   aBase.pubFunc();       // pubFunc() is accessible   
                          //    from any function  
   aDerived.pubFunc();    // pubFunc() is still public in   
                          //    derived class  
}  
```  
  
## See Also  
 [Controlling Access to Class Members](../vs140/Controlling-Access-to-Class-Members.md)   
 [Keywords](../vs140/Keywords--C---.md)