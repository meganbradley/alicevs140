---
title: "return Statement in Program Termination (C++)"
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
ms.assetid: 66d002ab-5625-4b68-8446-71e1b8fcdbd8
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# return Statement in Program Termination (C++)
Issuing a `return` statement from **main** is functionally equivalent to calling the **exit** function. Consider the following example:  
  
```  
// return_statement.cpp  
#include <stdlib.h>  
int main()  
{  
    exit( 3 );  
    return 3;  
}  
```  
  
 The **exit** and `return` statements in the preceding example are functionally identical. However, C++ requires that functions that have return types other than `void` return a value. The `return` statement allows you to return a value from **main**.  
  
## See Also  
 [Program Termination](../vs140/Program-Termination.md)