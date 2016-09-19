---
title: "Compiler Error C2228"
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
ms.assetid: 901cadb1-ce90-4ae0-a360-547a9ba2ca18
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2228
left of '.identifier' must have class/struct/union  
  
 The operand to the left of the period (.) is not a class, structure, or union.  
  
 The following sample generates C2228:  
  
```  
// C2228.cpp  
int i;  
struct S {  
public:  
    int member;  
} s, *ps = &s;  
  
int main() {  
   i.member = 0;   // C2228 i is not a class type  
   ps.member = 0;  // C2228 ps is a pointer to a structure  
  
   s.member = 0;   // s is a structure type  
   ps->member = 0; // ps points to a structure S  
}  
```  
  
 You will also see this error if you use incorrect syntax when using Managed Extensions. Whereas in other Visual Studio languages, you can use the dot operator to access a member of a managed class, a pointer to the object in C++ means you have to use the -> operator to access the member:  
  
 Wrong: `String * myString = checkedListBox1->CheckedItems->Item[0].ToString();`  
  
 Right: `String * myString = checkedListBox1->CheckedItems->Item[0]->ToString();`