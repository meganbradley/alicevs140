---
title: "Compiler Error C2886"
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
ms.assetid: c01588a1-484c-4dc9-a3f1-f900c6e44543
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2886
'class::identifier' : symbol cannot be used in a member using-declaration  
  
 A `using` declaration uses a symbol, such as a namespace name. A `using` declaration is for declaring base class members.  
  
 The following sample generates C2886:  
  
```  
// C2886.cpp  
// compile with: /c  
namespace Z {  
    int i;  
}  
  
class B {  
protected:  
    int i;  
};  
  
class D : public B {  
    // Error: Z is a namespace  
    using Z::i;   // C2886  
  
    // OK: B is a base class  
    using B::i;  
};  
```