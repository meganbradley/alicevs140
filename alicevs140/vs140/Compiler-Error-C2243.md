---
title: "Compiler Error C2243"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: error-reference
ms.assetid: b90065bb-d251-4ba9-8b4c-280ee13fa9c0
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2243
'conversion type' conversion from 'type1' to 'type2' exists, but is inaccessible  
  
 Access protection (`protected` or `private`) prevented conversion from a pointer to a derived class to a pointer to the base class.  
  
 The following sample generates C2243:  
  
```  
// C2243.cpp  
// compile with: /c  
class B {};  
class D : private B {};  
class E : public B {};  
  
D d;  
B *p = &d;   // C2243  
  
E e;  
B *p2 = &e;  
```  
  
 Base classes with `protected` or `private` access are not accessible to clients of the derived class. These levels of access control are used to indicate that the base class is an implementation detail that should be invisible to clients. Use public derivation if you want clients of the derived class to have access to implicit conversion of a derived class pointer to a pointer to the base class.