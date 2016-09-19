---
title: "Compiler Error C2434"
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
ms.assetid: 01329e26-7c74-4219-b74f-69e3a40c9738
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2434
'symbol' : a symbol declared with __declspec(process) cannot be dynamically initialized in /clr:pure mode  
  
 It is not possible to dynamically initialize a per-process variable under **/clr:pure**. For more information, see [/clr (Common Language Runtime Compilation)](../Topic/-clr%20\(Common%20Language%20Runtime%20Compilation\).md) and [process](../vs140/process.md).  
  
## Example  
 The following sample generates C2434.  
  
```  
// C2434.cpp  
// compile with: /clr:pure /c  
int f() { return 0; }  
__declspec(process) int i = f();   // C2434  
__declspec(process) int i2 = 0;   // OK  
```