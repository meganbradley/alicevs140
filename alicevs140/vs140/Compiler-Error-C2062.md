---
title: "Compiler Error C2062"
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
ms.assetid: 6cc98353-2ddf-43ab-88a2-9cc91cdd6033
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2062
type 'type' unexpected  
  
 The compiler did not expect a type name.  
  
 The following sample generates C2062:  
  
```  
// C2062.cpp  
// compile with: /c  
struct A {  : int l; };   // C2062  
struct B { private: int l; };   // OK  
```  
  
 C2062 can also occur due to the way the compiler handles undefined types in a constructor's parameter list. If the compiler encounters an undefined (misspelled?) type, it assumes the constructor is an expression, and issues C2062. To resolve, only use defined types in a constructor parameter list.