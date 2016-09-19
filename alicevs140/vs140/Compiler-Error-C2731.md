---
title: "Compiler Error C2731"
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
ms.assetid: 9b563999-febd-4582-9147-f355083c091e
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2731
'identifier' : function cannot be overloaded  
  
 The functions `main`, `WinMain`, `DllMain`, and `LibMain` cannot be overloaded.  
  
 The following sample generates C2731:  
  
```  
// C2731.cpp  
extern "C" void WinMain(int, char *, char *);  
void WinMain(int, short, char *, char*);   // C2731  
```