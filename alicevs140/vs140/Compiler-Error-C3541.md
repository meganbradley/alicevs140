---
title: "Compiler Error C3541"
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
ms.assetid: 252cfd4c-5fd2-415e-a17d-6b0c254350db
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3541
'type': typeid cannot be applied to a type that contains 'auto'  
  
 The [typeid](../Topic/typeid%20%20\(C++%20Component%20Extensions\).md) operator cannot be applied to the indicated type because it contains the `auto` specifier.  
  
## Example  
 The following example yields C3541.  
  
```  
// C3541.cpp  
// Compile with /Zc:auto  
#include <typeinfo>  
int main() {  
    auto x = 123;  
    typeid(x);    // OK  
    typeid(auto); // C3541  
    return 0;  
}  
```  
  
## See Also  
 [auto Keyword](../vs140/auto-Keyword.md)   
 [/Zc:auto (Deduce Variable Type)](../vs140/-Zc-auto--Deduce-Variable-Type-.md)   
 [typeid](../Topic/typeid%20%20\(C++%20Component%20Extensions\).md)