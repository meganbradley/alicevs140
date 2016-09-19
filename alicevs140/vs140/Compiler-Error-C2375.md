---
title: "Compiler Error C2375"
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
ms.assetid: 193c5e8b-1b20-4928-8a02-8c1cddaf2a26
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2375
'function' : redefinition; different linkage  
  
 The function is already declared with a different linkage specifier.  
  
 The following sample generates C2375:  
  
```  
// C2375.cpp  
// compile with: /Za /c  
extern void func( void );  
static void func( void );   // C2375  
static void func2( void );   // OK  
```