---
title: "Compiler Error C2943"
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
ms.assetid: ede6565e-d892-44c0-8eee-c69545f3be2e
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2943
'class' : type-class-id redefined as a type argument of a template  
  
 You cannot use a generic or template class, instead of a symbol, as a generic or template type argument.  
  
 The following sample generates C2943:  
  
```  
// C2943.cpp  
// compile with: /c  
template<class T>  
class List {};  
  
template<class List<int> > class MyList;   // C2943  
template<class T >  class MyList;  
```