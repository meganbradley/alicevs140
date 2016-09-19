---
title: "Compiler Error C2142"
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
ms.assetid: d0dbe10e-0952-49a4-8b33-e82fb7558b19
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2142
function declarations differ, variable parameters specified only in one of them  
  
 One declaration of the function contains a variable parameter list. Another declaration does not. ANSI C ([/Za](../Topic/-Za,%20-Ze%20\(Disable%20Language%20Extensions\).md)) only.  
  
 The following sample generates C2142:  
  
```  
// C2142.c  
// compile with: /Za /c  
void func();  
void func( int, ... );   // C2142  
void func2( int, ... );   // OK  
```