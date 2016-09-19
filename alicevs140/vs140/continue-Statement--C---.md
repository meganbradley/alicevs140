---
title: "continue Statement (C++)"
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
ms.assetid: 3c94ee57-f732-4c1d-8537-d0ce5382bfd4
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# continue Statement (C++)
Forces transfer of control to the controlling expression of the smallest enclosing [do](../vs140/do-while-Statement--C---.md), [for](../vs140/for-Statement--C---.md), or [while](../vs140/while-Statement--C---.md) loop.  
  
## Syntax  
  
```  
continue;  
```  
  
## Remarks  
 Any remaining statements in the current iteration are not executed. The next iteration of the loop is determined as follows:  
  
-   In a `do` or `while` loop, the next iteration starts by reevaluating the controlling expression of the `do` or `while` statement.  
  
-   In a `for` loop (using the syntax `for`(`init-expr`; `cond-expr`; `loop-expr`)), the `loop-expr` clause is executed. Then the `cond-expr` clause is reevaluated and, depending on the result, the loop either ends or another iteration occurs.  
  
 The following example shows how the `continue` statement can be used to bypass sections of code and begin the next iteration of a loop.  
  
## Example  
  
```  
// continue_statement.cpp  
#include <stdio.h>  
int main()  
{  
    int i = 0;  
    do  
    {  
        i++;  
        printf_s("before the continue\n");  
        continue;  
        printf("after the continue, should never print\n");  
     } while (i < 3);  
  
     printf_s("after the do loop\n");  
}  
```  
  
 **before the continue**  
**before the continue**  
**before the continue**  
**after the do loop**   
## See Also  
 [Jump Statements](../vs140/Jump-Statements--C---.md)   
 [Keywords](../vs140/Keywords--C---.md)