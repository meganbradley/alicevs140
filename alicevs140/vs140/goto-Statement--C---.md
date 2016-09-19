---
title: "goto Statement (C++)"
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
ms.assetid: 724c5deb-2de1-42d8-8ef1-23589d9bf5ed
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# goto Statement (C++)
The `goto` statement unconditionally transfers control to the statement labeled by the specified identifier.  
  
## Syntax  
  
```  
goto identifier;  
```  
  
## Remarks  
 The labeled statement designated by `identifier` must be in the current function. All `identifier` names are members of an internal namespace and therefore do not interfere with other identifiers.  
  
 A statement label is meaningful only to a `goto` statement; otherwise, statement labels are ignored. Labels cannot be redeclared.  
  
 It is good programming style to use the `break`, `continue`, and `return` statements instead of the `goto` statement whenever possible. However, because the `break` statement exits from only one level of a loop, you might have to use a `goto` statement to exit a deeply nested loop.  
  
 For more information about labels and the `goto` statement, see [Labeled Statements](../vs140/Labeled-Statements.md) and [Using Labels with the goto Statement](assetId:///6cd7c31a-9822-4241-8566-f79f51be48fe).  
  
## Example  
 In this example, a `goto` statement transfers control to the point labeled `stop` when `i` equals 3.  
  
```  
// goto_statement.cpp  
#include <stdio.h>  
int main()  
{  
    int i, j;  
  
    for ( i = 0; i < 10; i++ )  
    {  
        printf_s( "Outer loop executing. i = %d\n", i );  
        for ( j = 0; j < 2; j++ )  
        {  
            printf_s( " Inner loop executing. j = %d\n", j );  
            if ( i == 3 )  
                goto stop;  
        }  
    }  
  
    // This message does not print:   
    printf_s( "Loop exited. i = %d\n", i );  
  
    stop:   
    printf_s( "Jumped to stop. i = %d\n", i );  
}  
```  
  
 **Outer loop executing. i = 0**  
 **Inner loop executing. j = 0**  
 **Inner loop executing. j = 1**  
**Outer loop executing. i = 1**  
 **Inner loop executing. j = 0**  
 **Inner loop executing. j = 1**  
**Outer loop executing. i = 2**  
 **Inner loop executing. j = 0**  
 **Inner loop executing. j = 1**  
**Outer loop executing. i = 3**  
 **Inner loop executing. j = 0**  
**Jumped to stop. i = 3**   
## See Also  
 [Jump Statements](../vs140/Jump-Statements--C---.md)   
 [Keywords](../vs140/Keywords--C---.md)