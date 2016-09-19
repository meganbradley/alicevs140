---
title: "Compiler Warning (level 1) C4377"
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
ms.assetid: a1c797b8-cd5e-4a56-b430-d07932e811cf
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 1) C4377
native types are private by default; -d1PrivateNativeTypes is deprecated  
  
 In previous releases, native types in assemblies were public by default, and an internal, undocumented compiler option (**/d1PrivateNativeTypes**) was used to make them private.  
  
 All types, native and CLR, are now private by default in an assembly, so **/d1PrivateNativeTypes** is no longer needed.  
  
## Example  
 The following sample generates C4377.  
  
```  
// C4377.cpp  
// compile with: /clr /d1PrivateNativeTypes /W1  
// C4377 warning expected  
int main() {}  
```