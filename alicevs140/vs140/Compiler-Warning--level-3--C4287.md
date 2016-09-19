---
title: "Compiler Warning (level 3) C4287"
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
ms.assetid: 1bf3bff8-6402-4d06-95ba-431678a790a7
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 3) C4287
'operator' : unsigned/negative constant mismatch  
  
 An unsigned variable was used in an operation with a negative number.  
  
 This warning is off by default. See [Compiler Warnings That Are Off by Default](../vs140/Compiler-Warnings-That-Are-Off-by-Default.md) for more information.  
  
## Example  
 The following sample generates C4287:  
  
```  
// C4287.cpp  
// compile with: /W3  
#pragma warning(default : 4287)  
#include <stdio.h>  
  
int main()  
{  
    unsigned int u = 1;  
    if (u < -1)   // C4287  
        printf_s("u LT -1");  
    else  
        printf_s("u !LT -1");  
    return 0;  
}  
```