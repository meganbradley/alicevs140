---
title: "Compiler Warning (level 4) C4510"
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
ms.assetid: fd28d1d4-ad27-4dad-94c0-9dba46c93180
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 4) C4510
'class' : default constructor could not be generated  
  
 The compiler cannot generate a default constructor for the specified class and no user-defined constructor was created. You will not be able to create objects of this type.  
  
 There are several situations that prevent the compiler from generating a default constructor, including:  
  
-   A const data member.  
  
-   A data member that is a reference.  
  
 You need to create a user-defined default constructor for the class that initializes these members.  
  
 The following sample generates C4510:  
  
```  
// C4510.cpp  
// compile with: /W4  
struct A {  
   const int i;  
   int &j;  
   A& operator=( const A& ); // C4510 expected  
   // uncomment the following line to resolve this C4510  
   // A(int ii, int &jj) : i(ii), j(jj) {}  
};   // C4510  
  
int main() {  
}  
```