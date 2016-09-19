---
title: "Compiler Error C2897"
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
ms.assetid: a88349e2-823f-42a0-8660-0653b677afa4
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2897
a destructor/finalizer cannot be a function template  
  
 Destructors or finalizers cannot be overloaded, so declaring a destructor as a template (which would define a set of destructors) is not allowed.  
  
 The following sample generates C2897:  
  
## Example  
 The following sample generates C2897.  
  
```  
// C2897.cpp  
// compile with: /c  
class X {  
public:  
   template<typename T> ~X() {}   // C2897  
};  
```  
  
## Example  
 The following sample generates C2897.  
  
```  
// C2897_b.cpp  
// compile with: /c /clr  
ref struct R2 {  
protected:  
   template<typename T> !R2(){}   // C2897 error  
};  
```