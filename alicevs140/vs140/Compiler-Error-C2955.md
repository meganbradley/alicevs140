---
title: "Compiler Error C2955"
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
ms.assetid: 77709fb6-d69b-46fd-a62f-e8564563d01b
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2955
'identifier' : use of class template or alias generic requires template or generic argument list  
  
 You cannot use a class template or class generic as an identifier without a template or generic argument list.  
  
 For more information, see [Class Templates](../vs140/Class-Templates.md).  
  
 The following sample generates C2955 and shows how to fix it:  
  
```  
// C2955.cpp  
// compile with: /c  
template<class T>   
class X {};  
  
X x1;   // C2955  
X<int> x2;   // OK - this is how to fix it.  
```  
  
 C2955 can also occur when attempting an out-of-line definition for a function declared in a class template:  
  
```  
// C2955_b.cpp  
// compile with: /c  
template <class T>  
class CT {  
public:  
   void CTFunc();  
   void CTFunc2();  
};  
  
void CT::CTFunc() {}   // C2955  
  
// OK - this is how to fix it  
template <class T>  
void CT<T>::CTFunc2() {}  
  
```  
  
 C2955 can also occur when using generics:  
  
```  
// C2955_c.cpp  
// compile with: /clr  
generic <class T>   
ref struct GC {   
   T t;  
};  
  
int main() {  
   GC^ g;   // C2955  
   GC <int>^ g;  
}  
```