---
title: "Compiler Warning (level 3) C4570"
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
ms.assetid: feec1225-e6ad-4995-8d96-c22e864a77bd
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 3) C4570
'type' : is not explicitly declared as abstract but has abstract functions  
  
 A type that contains [abstract (C++)](../vs140/abstract---C---Component-Extensions-.md) functions should itself be marked as abstract.  
  
## Example  
 The following sample generates C4570.  
  
```  
// C4570.cpp  
// compile with: /clr /W3 /c  
ref struct X {   // C4570  
// try the following line instead  
// ref class X abstract {  
   virtual void f() abstract;  
};  
```