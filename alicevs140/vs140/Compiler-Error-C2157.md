---
title: "Compiler Error C2157"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: babbca24-16dc-4b69-be14-a675029249c1
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2157
'function' : must be declared before use in pragma list  
  
 The function name is not declared before being referenced in the list of functions for an [alloc_text](../vs140/alloc_text.md) pragma.  
  
 The following sample generates C2157:  
  
```  
// C2157.cpp  
// compile with: /c  
#pragma alloc_text( "func", func)   // C2157  
  
// OK  
extern "C" void func();  
#pragma alloc_text( "func", func)  
```