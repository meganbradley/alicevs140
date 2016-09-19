---
title: "Compiler Error C3191"
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
ms.assetid: 348851b6-7061-4219-8763-ab6936d8f35c
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3191
'syntax' : incompatible with /clr:oldSyntax  
  
 The syntax for Managed Extensions for C++ was requested (`/clr:oldSyntax`). However, the compiler found newer syntax in a source code file.  
  
 The following sample generates C3191:  
  
```  
// C3191.cpp  
// compile with: /clr:oldSyntax  
#using <mscorlib.dll>  
using namespace System;  
int main() {  
   Object ^ o;   // C3191  
   Object * o2;   // OK  
}  
```