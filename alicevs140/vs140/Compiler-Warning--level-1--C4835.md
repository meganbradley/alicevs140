---
title: "Compiler Warning (level 1) C4835"
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
ms.assetid: d2e44c62-7b0e-4a45-943d-97903e27ed9d
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 1) C4835
'variable' : the initializer for exported data will not be run until managed code is first executed in the host assembly  
  
 When accessing data between managed components, it is recommended that you not use native C++ import and export mechanisms. Instead, declare your data members inside a managed type and reference the metadata with `#using` in the client. For more information, see [The #using Directive](../vs140/#using-Directive--C---.md).  
  
## Example  
 The following sample generates C4835.  
  
```  
// C4835.cpp  
// compile with: /W1 /clr /LD  
int f() { return 1; }  
int n = 9;  
  
__declspec(dllexport) int m = f();   // C4835  
__declspec(dllexport) int *p = &n;   // C4835  
```  
  
## Example  
 The following sample consumes the component built in the previous sample, showing that the value of the variables is not as expected.  
  
```  
// C4835_b.cpp  
// compile with: /clr C4835.lib  
#include <stdio.h>  
__declspec(dllimport) int m;  
__declspec(dllimport) int *p;  
  
int main() {  
   printf("%d\n", m);  
   printf("%d\n", p);  
}  
```  
  
 **0**  
**268456008**