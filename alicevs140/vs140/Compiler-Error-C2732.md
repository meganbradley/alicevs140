---
title: "Compiler Error C2732"
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
ms.assetid: 01b7ad2c-93cf-456f-a4c0-c5f2fdc7c07c
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2732
linkage specification contradicts earlier specification for 'function'  
  
 The function is already declared with a different linkage specifier.  
  
 This error can be caused by include files with different linkage specifiers.  
  
 To fix this error, change the `extern` statements so that the linkages agree. In particular, do not wrap `#include` directives in `extern "C"` blocks.  
  
## Example  
 The following sample generates C2732:  
  
```  
// C2732.cpp  
extern void func( void );   // implicit C++ linkage  
extern "C" void func( void );   // C2732  
```