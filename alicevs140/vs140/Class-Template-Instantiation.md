---
title: "Class Template Instantiation"
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
ms.assetid: 750cb629-24bd-449f-a7f1-9dcb27ecf940
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Class Template Instantiation
Unlike function templates, when instantiating a class template, you must explicitly instantiate the class by giving the arguments for the class templates. To create an instance of `TempClass`:  
  
```  
TempClass< float, 6 > test1;       // OK  
TempClass< char, items++ > test2;  // Error, second parameter   
                                   // must be constant.  
```  
  
 The compiler generates code for a template class or function when the class or function is instantiated. A member function is instantiated when it is called, and a virtual member function is instantiated when its class is constructed. This can cause problems if you are building a library with templates for other users. For more information, see [Explicit Instantiation](../vs140/Explicit-Instantiation.md).  
  
 A class template is first specialized and then instantiated by the compiler. The compiler does not instantiate the class template until a reference to a member of this template class is made, sizeof is used on the class, or an instance is created.  
  
 An explicit specialization of a template is a customized version of the template for a particular type.  
  
```  
// template_instantiation2.cpp  
template<class T> class X  
{  
};  
  
// Explicit specialization of X with 'int'  
template<> class X<int>  
{  
};  
int main()  
{  
}  
```  
  
 Explicit specialization without `template<>` will produce an error. Versions of Visual C++  before Visual C++ .NET 2003 accepted this syntax:  
  
```  
// Explicit specialization of X with 'char'  
class X<char> // C2906  
{  
};  
```  
  
 If a template is explicitly instantiated or specialized once, it cannot be explicitly instantiated or specialized a second time in the same program for the same set of template arguments. Further specializations with different template arguments are allowed.  
  
 If there is not an explicit instantiation or specialization for a particular template argument, the template will be implicitly instantiated at the point where it is first used.  
  
 Because different instantiations of the same template are different types, static members for one specialization or instantiation of a template are separate from static members for a different specialization or instantiation of the same template.  
  
## See Also  
 [Class Templates](../vs140/Class-Templates.md)