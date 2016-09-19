---
title: "false (C++)"
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
ms.topic: language-reference
ms.assetid: cc13aec5-1f02-4d38-8dbf-5473ea2b354f
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# false (C++)
The keyword is one of the two values for a variable of type [bool](../vs140/bool--C---.md) or a conditional expression (a conditional expression is now a **true** Boolean expression). For example, if `i` is a variable of type `bool`, the `i = false;` statement assigns **false** to `i`.  
  
## Example  
  
```  
// bool_false.cpp  
#include <stdio.h>  
  
int main()  
{  
    bool bb = true;  
    printf_s("%d\n", bb);  
    bb = false;  
    printf_s("%d\n", bb);  
}  
```  
  
 **1**  
**0**   
## See Also  
 [Keywords](../vs140/Keywords--C---.md)