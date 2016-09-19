---
title: "Linker Tools Warning LNK4217"
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
ms.assetid: 280dc03e-5933-4e8d-bb8c-891fbe788738
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Linker Tools Warning LNK4217
locally defined symbol 'symbol' imported in function 'function'  
  
 [__declspec(dllimport)](../vs140/dllexport--dllimport.md) was specified for a symbol even though the symbol is defined locally. Remove the `__declspec` modifier to resolve this warning.  
  
 `symbol` is the symbol name that's defined within the image. `function` is the function that is importing the symbol.  
  
 This warning will not appear when you compile by using the option [/clr](../Topic/-clr%20\(Common%20Language%20Runtime%20Compilation\).md).  
  
 LNK4217 can also occur if you attempt to link two modules together, when instead you should compile the second module with the import library of the first module.  
  
```  
// LNK4217.cpp  
// compile with: /LD  
#include "windows.h"  
__declspec(dllexport) void func(unsigned short*) {}  
```  
  
 And then,  
  
```  
// LNK4217b.cpp  
// compile with: /c  
#include "windows.h"  
__declspec(dllexport) void func(unsigned short*) {}  
```  
  
 Attempting to link these two modules will result in LNK4217, compile the second sample with the import library of the first sample to resolve.