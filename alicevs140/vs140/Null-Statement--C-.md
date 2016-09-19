---
title: "Null Statement (C)"
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
ms.assetid: 72576ce6-26d0-4379-be65-fee522088790
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Null Statement (C)
A "null statement" is a statement containing only a semicolon; it can appear wherever a statement is expected. Nothing happens when a null statement is executed. The correct way to code a null statement is:  
  
## Syntax  
  
```  
  
;  
  
```  
  
## Remarks  
 Statements such as **do**, **for**, **if**, and `while` require that an executable statement appear as the statement body. The null statement satisfies the syntax requirement in cases that do not need a substantive statement body.  
  
 As with any other C statement, you can include a label before a null statement. To label an item that is not a statement, such as the closing brace of a compound statement, you can label a null statement and insert it immediately before the item to get the same effect.  
  
 This example illustrates the null statement:  
  
```  
for ( i = 0; i < 10; line[i++] = 0 )  
     ;  
```  
  
 In this example, the loop expression of the **for** statement `line[i++] = 0` initializes the first 10 elements of `line` to 0. The statement body is a null statement, since no further statements are necessary.  
  
## See Also  
 [Statements (C)](../vs140/Statements--C-.md)