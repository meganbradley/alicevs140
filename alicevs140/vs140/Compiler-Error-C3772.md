---
title: "Compiler Error C3772"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 63e938d4-088d-41cc-a562-5881a05b5710
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3772
"name" : invalid friend template declaration  
  
 It is invalid to declare a friend of a class template specialization. You cannot declare an explicit or partial specialization of a class template and in the same statement declare a friend of that specialization. The *name* placeholder identifies the invalid declaration.  
  
### To correct this error  
  
-   Do not declare a friend of a class template specialization.  
  
-   If appropriate for your application, declare a friend of the class template, or declare a friend of a particular partial or explicit specialization.  
  
## Example  
 The following code example fails because it declares a friend of a partial specialization of a class template.  
  
```  
// c3772.cpp  
// compile with: /c  
  
// A class template.  
    template<class T> class A {};  
  
// A partial specialization of the class template.  
    template<class T> class A<T*> {};  
  
// An explicit specialization.  
    template<> class A<char>;  
  
class X {  
// Invalid declaration of a friend of a partial specialization.  
    template<class T> friend class A<T*>; // C3772  
  
// Instead, if it is appropriate for your application, declare a   
// friend of the class template. Consequently, all specializations   
// of the class template are friends:  
//    template<class T> friend class A;  
// Or declare a friend of a particular partial specialization:  
//    friend class A<int*>;  
// Or declare a friend of a particular explicit specialization:  
//    friend class A<char>;  
};  
```  
  
## See Also  
 [Template Specifications](../vs140/Template-Specifications.md)   
 [Partial Specialization of Class Templates (C++)](../vs140/Template-Specialization--C---.md)   
 [Explicit Specialization of Class Templates](../vs140/Explicit-Specialization-of-Class-Templates.md)