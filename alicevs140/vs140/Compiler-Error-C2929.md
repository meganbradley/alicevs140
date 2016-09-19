---
title: "Compiler Error C2929"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 11134027-6adc-4733-b6bd-b94486bd1933
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2929
'identifier' : explicit instantiation; cannot explicitly force and suppress instantiation of template-class member  
  
 You cannot explicitly instantiate an identifier while preventing it from being instantiated.  
  
 The following sample generates C2929:  
  
```  
// C2929.cpp  
// compile with: /c  
template<typename T>  
class A {  
public:  
   A() {}  
};  
  
template A<int>::A();  
  
extern template A<int>::A();   // C2929  
```