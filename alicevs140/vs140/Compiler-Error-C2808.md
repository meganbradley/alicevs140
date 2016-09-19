---
title: "Compiler Error C2808"
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
ms.assetid: 3d745102-d3b3-4735-a7d2-ad42d5bf3cfa
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2808
unary 'operator operator' has too many formal parameters  
  
 The unary operator has a nonvoid parameter list.  
  
 The following sample generates C2808:  
  
```  
// C2808.cpp  
// compile with: /c  
class X {  
public:  
   X operator! ( X );   // C2808 nonvoid parameter list  
   X operator! ( void );   // OK  
};  
  
```