---
title: "Compiler Error C3638"
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
ms.assetid: 8d8bc5ca-75aa-480e-b6b6-3178fab51b1d
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3638
'operator' : the standard boxing and unboxing conversion operators cannot be redefined  
  
 The compiler defines a conversion operator for each managed class to support implicit boxing. This operator cannot be redefined.  
  
 For more information, see [Implicit Boxing](../vs140/Boxing---C---Component-Extensions-.md).  
  
 The following sample generates C3638:  
  
```  
// C3638.cpp  
// compile with: /clr  
value struct V {  
   V(){}  
   static operator V^(V);   // C3638  
};  
  
int main() {  
   V myV;  
   V ^ pmyV = myV;   // operator supports implicit boxing  
}  
```