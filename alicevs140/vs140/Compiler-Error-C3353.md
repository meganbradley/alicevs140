---
title: "Compiler Error C3353"
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
ms.assetid: 5699c04b-d504-46ce-bf71-c200318fed71
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3353
'delegate' : a delegate can only be created from a global function or a member function of a managed or WinRT type  
  
 Delegates, declared with the [__delegate](../vs140/__delegate.md) or [delegate](../vs140/delegate---C---Component-Extensions-.md) keyword, can only be declared at global scope.  
  
 The following sample generates C3353:  
  
```  
// C3353.cpp  
// compile with: /clr  
delegate int f;   // C3353  
```