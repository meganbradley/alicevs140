---
title: "Compiler Error C2500"
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
ms.assetid: 6bff8161-dc9a-48ca-91f1-fd2eefdbbc93
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2500
'identifier1' : 'identifier2' is already a direct base class  
  
 A class or structure appears more than once in a list of base classes.  
  
 A direct base is one mentioned in the base list. An indirect base is a base class of one of the classes in the base list.  
  
 A class cannot be specified as a direct base class more than once. A class can be used as an indirect base class more than once.  
  
 The following sample generates C2500:  
  
```  
// C2500.cpp  
// compile with: /c  
class A {};  
class B : public A, public A {};    // C2500  
  
// OK  
class C : public A {};  
class D : public A {};  
class E : public C, public D {};  
```