---
title: "Compiler Error C2959"
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
ms.assetid: d66bb2a8-70c3-4209-a358-b0c47f111a50
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2959
a generic class or function may not be a member of a template  
  
 For more information, see [Managed Templates](../vs140/Windows-Runtime-and-Managed-Templates--C---Component-Extensions-.md) and [Generics (C++)](../vs140/Generics---C---Component-Extensions-.md).  
  
## Example  
 The following sample generates C2959.  
  
```  
// C2959.cpp  
// compile with: /clr /c  
template <class T> ref struct S {  
   generic <class U> ref struct GR1;   // C2959  
};  
```