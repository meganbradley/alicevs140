---
title: "Compiler Warning (level 1 and level 4) C4700"
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
ms.assetid: 2da0deb4-77dd-4b05-98d3-b78d74ac4ca7
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 1 and level 4) C4700
uninitialized local variable 'name' used  
  
 You used the local variable *name* without first assigning it a value, which could lead to unpredictable results.  
  
 The following sample generates C4700:  
  
```  
// C4700.cpp  
// compile with: /W1  
int main() {  
   int i;  
   return i;   // C4700  
}  
```  
  
 Under [/clr:safe](../Topic/-clr%20\(Common%20Language%20Runtime%20Compilation\).md) this is a level 4 warning.  The following sample generates C4700:  
  
```  
// C4700b.cpp  
// compile with: /W4 /clr:safe /c  
using namespace System;  
int main() {  
   Int32^ bi;  
   return *bi;   // C4700  
}  
```