---
title: "Compiler Error C3535"
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
ms.assetid: 24449c98-f681-484d-a00b-32533dca3a88
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3535
cannot deduce type for 'type1' from 'type2'  
  
 The type of the variable declared by the `auto` keyword cannot be deduced from the type of the initialization expression. For example, this error occurs if the initialization expression evaluates to `void`, which is not a type.  
  
### To correct this error  
  
1.  Ensure that the type of the initialization expression is not `void`.  
  
2.  Ensure that the declaration is not a pointer to a fundamental type. For more information, see [Fundamental Types](../vs140/Fundamental-Types---C---.md).  
  
3.  Ensure that if the declaration is a pointer to a type, the initialization expression is a pointer type.  
  
## Example  
 The following example yields C3535 because the initialization expression evaluates to `void`.  
  
```  
// C3535a.cpp  
// Compile with /Zc:auto  
void f(){}  
int main()  
{  
   auto x = f();   //C3535  
   return 0;  
}  
```  
  
## Example  
 The following example yields C3535 because the statement declares variable `x` as a pointer to a deduced type, but the type of the initializer expression is double. Consequently, the compiler cannot deduce the type of the variable.  
  
```  
// C3535b.cpp  
// Compile with /Zc:auto  
int main()  
{  
   auto* x = 123.0;   // C3535  
   return 0;  
}  
```  
  
## Example  
 The following example yields C3535 because variable `p` declares a pointer to a deduced type, but the initialization expression is not a pointer type.  
  
```  
// C3535c.cpp  
// Compile with /Zc:auto  
class A { };  
A x;  
auto *p = x;  // C3535  
```  
  
## See Also  
 [auto Keyword](../vs140/auto-Keyword.md)   
 [Fundamental Types](../vs140/Fundamental-Types---C---.md)