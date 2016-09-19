---
title: "Compiler Error C2821"
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
ms.assetid: e8d71988-a968-4484-94db-e8c3bad74a4a
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2821
first formal parameter to 'operator new' must be 'unsigned int'  
  
 The first formal parameter of the [operator new](../vs140/operator-new---new--.md) must be an unsigned `int`.  
  
 The following sample generates C2821:  
  
```  
// C2821.cpp  
// compile with: /c  
void * operator new( /* unsigned int,*/ void * );   // C2821  
void * operator new( unsigned int, void * );  
```