---
title: "Compiler Error C2989"
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
ms.assetid: 936303d8-eb3b-4746-82ec-2f18020a6f64
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2989
'class' : class type has already been declared as a non-class type  
  
 The class generic or template redefines a non-template or non-generic class. Check header files for conflicts.  
  
 If you are using class template partial specializations, see Knowledge Base article Q240866.  
  
 The following sample generates C2989:  
  
```  
// C2989.cpp  
// compile with: /c  
class C{};  
  
template <class T>  
class C{};  // C2989  
class C2{};  
```  
  
 C2989 can also occur when using generics:  
  
```  
// C2989b.cpp  
// compile with: /clr /c  
ref class GC1;  
  
generic <typename T> ref class GC1;   // C2989  
template <typename T> ref class GC2;  
  
generic <typename T> ref class GC2;   // C2989  
generic <typename T> ref class GCb;  
template <typename T> ref class GC2;  
generic <typename T> ref class GCc;  
```