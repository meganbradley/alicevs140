---
title: "Compiler Error C2357"
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
ms.assetid: d1083945-0ea2-4385-9e66-8c665978806c
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2357
'identifier' : must be a function of type 'type'  
  
 Your code declares a version of the `atexit` function that does not match the version declared internally by the compiler. Declare `atexit` as follows:  
  
```  
int __cdecl atexit(void (__cdecl *)());  
```  
  
 For more information, see [init_seg](../vs140/init_seg.md).  
  
 The following sample generates C2357:  
  
```  
// C2357.cpp  
// compile with: /c  
// C2357 expected  
#pragma warning(disable : 4075)  
// Uncomment the following line to resolve.  
// int __cdecl myexit(void (__cdecl *)());  
#pragma init_seg(".mine$m",myexit)  
```