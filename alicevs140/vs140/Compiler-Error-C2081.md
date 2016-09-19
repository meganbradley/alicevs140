---
title: "Compiler Error C2081"
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
ms.assetid: 7db9892d-364d-4178-a49d-f8398ece09a0
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2081
'identifier' : name in formal parameter list illegal  
  
 The identifier caused a syntax error.  
  
 This error can be caused by using the old style for the formal parameter list. You must specify the type of formal parameters in the formal parameter list.  
  
 The following sample generates C2081:  
  
```  
// C2081.c  
void func( int i, j ) {}  // C2081, no type specified for j  
```  
  
 Possible resolution:  
  
```  
// C2081b.c  
// compile with: /c  
void func( int i, int j ) {}  
```