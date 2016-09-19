---
title: "break Statement (C)"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
  - C
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 015627c7-0924-49b2-a4d1-c77edf5eae6a
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# break Statement (C)
The `break` statement terminates the execution of the nearest enclosing `do`, `for`, `switch`, or `while` statement in which it appears. Control passes to the statement that follows the terminated statement.  
  
## Syntax  
 *jump-statement*:  
 `break;`  
  
 The `break` statement is frequently used to terminate the processing of a particular case within a `switch` statement. Lack of an enclosing iterative or `switch` statement generates an error.  
  
 Within nested statements, the `break` statement terminates only the `do`, `for`, `switch`, or `while` statement that immediately encloses it. You can use a `return` or `goto` statement to transfer control elsewhere out of the nested structure.  
  
 This example illustrates the `break` statement:  
  
```  
#include <stdio.h>  
int main() {  
   char c;  
   for(;;) {  
      printf_s( "\nPress any key, Q to quit: " );  
  
      // Convert to character value  
      scanf_s("%c", &c);  
      if (c == 'Q')  
          break;  
   }  
} // Loop exits only when 'Q' is pressed  
```  
  
## See Also  
 [break Statement](../vs140/break-Statement--C---.md)