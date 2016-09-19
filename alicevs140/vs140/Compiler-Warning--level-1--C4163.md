---
title: "Compiler Warning (level 1) C4163"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b08413fd-03fc-4f41-9167-a98976ac12f2
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 1) C4163
'identifier' : not available as an intrinsic function  
  
 The specified function cannot be used as an [intrinsic](../vs140/intrinsic.md) function. The compiler ignores the invalid function name.  
  
 The following sample generates C4163:  
  
```  
// C4163.cpp  
// compile with: /W1 /LD  
#include <math.h>  
#pragma intrinsic(mysin)   // C4163  
// try the following line instead  
// #pragma intrinsic(sin)  
```