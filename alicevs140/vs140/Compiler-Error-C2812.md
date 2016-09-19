---
title: "Compiler Error C2812"
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
ms.assetid: 22aadb8c-7232-489d-a3ad-60662dda30a8
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2812
\#import is not supported with /clr:pure and /clr:safe  
  
 [The #import Directive](../vs140/#import-Directive--C---.md) is not supported with **/clr:pure** and **/clr:safe** because `#import` requires the use of native compiler support libraries.  
  
## Example  
 The following sample generates C2812.  
  
```  
// C2812.cpp  
// compile with: /clr:pure /c  
#import "importlib.tlb"   // C2812  
```