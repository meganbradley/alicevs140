---
title: "Compiler Error C3834"
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
ms.assetid: 059e0dc4-300b-4e74-b6c2-41a57831fe2a
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3834
illegal explicit cast to a pinning pointer; use a pinned local variable instead  
  
 Explicit casts to a pinned pointer are not allowed.  
  
## Example  
 The following sample generates C3834.  
  
```  
// C3834.cpp  
// compile with: /clr  
int main() {  
   int x = 33;  
  
   pin_ptr<int> p = safe_cast<pin_ptr<int> >(&x);   // C3834  
   pin_ptr<int> p2 = &x;   // OK  
}  
```  
  
## Example  
 The following sample generates C3834.  
  
```  
// C3834_b.cpp  
// compile with: /clr:oldSyntax  
using namespace System;  
  
int main() {  
   const __wchar_t * pS = reinterpret_cast<const __wchar_t __pin*>(S"hello");   // C3834  
  
   // OK   
   // declare a pinning variable  
   String __pin* ppin = S"Hello";  
  
   // cast pinning variable to unmanaged type  
   const __wchar_t * pS2 = reinterpret_cast<__wchar_t*>(ppin);     
  
   pS2 += 6;  
}  
```