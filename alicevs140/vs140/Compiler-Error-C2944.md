---
title: "Compiler Error C2944"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: f209e668-e72f-442a-a438-8c4ff43a404a
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2944
'class' : type-class-id redefined as a value argument of a template  
  
 You cannot use a generic or template class, instead of a symbol, as a template value argument.  
  
 The following sample generates C2944:  
  
```  
// C2944.cpp  
// compile with: /c  
template<class T>  
class TC { };   
  
template <int TC<int> > struct X1 { };   // C2944  
  
template <class T > struct X2 {};  
```  
  
 C2944 can also occur when using generics:  
  
```  
// C2944b.cpp  
// compile with: /clr /c  
generic<class T>  
ref class GC {};  
  
template <int GC<int> > struct X2 { };   // C2944  
template <class T> struct X3 {};   // OK  
```