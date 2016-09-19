---
title: "Compiler Error C3533"
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
ms.assetid: a68b1ba5-466e-4190-a1a4-505ccfe548b7
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3533
'type': a parameter cannot have a type that contains 'auto'  
  
 A method or template parameter cannot be declared with the `auto` keyword if the default [/Zc:auto](../vs140/-Zc-auto--Deduce-Variable-Type-.md) compiler option is in effect.  
  
### To correct this error  
  
1.  Remove the `auto` keyword from the parameter declaration.  
  
## Example  
 The following example yields C3535 because it declares a function parameter with the `auto` keyword and it is compiled with **/Zc:auto**.  
  
```  
// C3533a.cpp  
// Compile with /Zc:auto  
void f(auto j){} // C3533  
```  
  
## Example  
 The following example yields C3535 because it declares a template parameter with the `auto` keyword and it is compiled with **/Zc:auto**.  
  
```  
// C3533b.cpp  
// Compile with /Zc:auto  
template<auto T> class C{}; // C3533  
```  
  
## See Also  
 [auto Keyword](../vs140/auto-Keyword.md)   
 [/Zc:auto (Deduce Variable Type)](../vs140/-Zc-auto--Deduce-Variable-Type-.md)