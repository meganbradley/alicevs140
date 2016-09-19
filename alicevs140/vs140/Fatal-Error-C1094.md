---
title: "Fatal Error C1094"
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
ms.assetid: 9e1193b2-cb95-44f9-bf6f-019e0d41dd97
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Fatal Error C1094
'-Zmval1' : command line option is inconsistent with value used to build precompiled header ('-Zmval2')  
  
 The value that is passed to [/Yc](../vs140/-Yc--Create-Precompiled-Header-File-.md) must be the same value that is passed to [/Yu](../vs140/-Yu--Use-Precompiled-Header-File-.md) (**/Zm** values must be the same in all compilations that use or create the same precompiled header file).  
  
 The following sample generates C1094:  
  
```  
// C1094.h  
int func1();  
```  
  
 And then,  
  
```  
// C1094.cpp  
// compile with: /Yc"C1094.h" /Zm200  
int u;  
int main() {  
   int sd = 32;  
}  
#include "C1094.h"  
```  
  
 And then,  
  
```  
// C1094b.cpp  
// compile with: /Yu"C1094.h" /Zm300 /c  
#include "C1094.h"   // C1094 compile with /Zm200  
void Test() {}  
```