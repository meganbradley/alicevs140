---
title: "Compiler Error C2086"
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
ms.assetid: 4329bf72-90c8-444c-8524-4ef75e6b2139
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2086
'identifier' : redefinition  
  
 The identifier is defined more than once, or a subsequent declaration differs from a previous one.  
  
 C2086 can also be the result of incremental building for a referenced C# assembly. Rebuild the C# assembly to resolve this error.  
  
 The following sample generates C2086:  
  
```  
// C2086.cpp  
main() {  
  int a;  
  int a;   // C2086 not an error in ANSI C  
}  
```