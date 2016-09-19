---
title: "Compound Statement (C)"
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
ms.assetid: 32d1bf86-cbbc-42a9-ba3a-1be1c6c7754c
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compound Statement (C)
A compound statement (also called a "block") typically appears as the body of another statement, such as the **if** statement. [Declarations and Types](../vs140/Declarations-and-Types.md) describes the form and meaning of the declarations that can appear at the head of a compound statement.  
  
## Syntax  
 *compound-statement*:  
 **{**  *declaration-list* opt*statement-list*opt**}**  
  
 *declaration-list*:  
 *declaration*  
  
 *declaration-list declaration*  
  
 *statement-list*:  
 s*tatement*  
  
 *statement-list statement*  
  
 If there are declarations, they must come before any statements. The scope of each identifier declared at the beginning of a compound statement extends from its declaration point to the end of the block. It is visible throughout the block unless a declaration of the same identifier exists in an inner block.  
  
 Identifiers in a compound statement are presumed **auto** unless explicitly declared otherwise with **register**, **static**, or `extern`, except functions, which can only be `extern`. You can leave off the `extern` specifier in function declarations and the function will still be `extern`.  
  
 Storage is not allocated and initialization is not permitted if a variable or function is declared in a compound statement with storage class `extern`. The declaration refers to an external variable or function defined elsewhere.  
  
 Variables declared in a block with the **auto** or **register** keyword are reallocated and, if necessary, initialized each time the compound statement is entered. These variables are not defined after the compound statement is exited. If a variable declared inside a block has the **static** attribute, the variable is initialized when program execution begins and keeps its value throughout the program. See [Storage Classes](../vs140/C-Storage-Classes.md) for information about **static**.  
  
 This example illustrates a compound statement:  
  
```  
if ( i > 0 )   
{  
    line[i] = x;  
    x++;  
    i--;  
}  
```  
  
 In this example, if `i` is greater than 0, all statements inside the compound statement are executed in order.  
  
## See Also  
 [Statements (C)](../vs140/Statements--C-.md)