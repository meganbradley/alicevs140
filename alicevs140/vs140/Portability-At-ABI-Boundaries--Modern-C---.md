---
title: "Portability At ABI Boundaries (Modern C++)"
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
ms.topic: article
ms.assetid: abbd405e-3038-427c-8c24-e00598f0936a
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Portability At ABI Boundaries (Modern C++)
Use sufficiently portable types and conventions at binary interface boundaries. A “portable type” is a C built-in type or a struct that contains only C built-in types. Class types can only be used when caller and callee agree on layout, calling convention, etc. This is only possible when both are compiled with the same compiler and compiler settings.  
  
## How to flatten a class for C portability  
 When callers may be compiled with another compiler/language, then “flatten” to an “extern C” API with a specific calling convention:  
  
```cpp  
// class widget {  
//   widget();  
//   ~widget();  
//   double method( int, gadget& );  
// };  
extern “C” {    // functions using explicit “this”  
  struct widget;   // + opaque type (fwd decl only)  
  widget* STDCALL widget_create();    // ctor → create new  “this”  
  void STDCALL widget_destroy( widget* );    // dtor → consume “this”  
  double STDCALL widget_method( widget*, int, gadget* );    // method → use “this”  
}  
  
```  
  
## See Also  
 [Welcome Back to C++](../vs140/Welcome-Back-to-C----Modern-C---.md)   
 [C++ Language Reference](../vs140/C---Language-Reference.md)   
 [Standard C++ Library](../vs140/C---Standard-Library-Reference.md)