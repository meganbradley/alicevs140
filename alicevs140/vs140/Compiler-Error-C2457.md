---
title: "Compiler Error C2457"
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
ms.assetid: 347e169d-23ad-434f-8836-5b09b53980ff
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2457
'macro': predefined macro cannot appear outside of a function body  
  
 You attempted to use a predefined macro, such as [__FUNCTION\_\_](../vs140/Predefined-Macros.md), in a global space.  
  
## Example  
 The following sample generates C2457:  
  
```  
// C2457.cpp  
#include <stdio.h>  
  
__FUNCTION__;   // C2457, cannot be global  
  
int main()   
{  
    printf_s("\n%s",__FUNCTION__);   // OK  
}  
```