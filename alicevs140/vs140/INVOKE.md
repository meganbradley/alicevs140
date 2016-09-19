---
title: "INVOKE"
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
ms.topic: article
ms.assetid: 12d9bb40-33b9-411e-b801-45a1d675967e
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# INVOKE
Calls the procedure at the address given by *expression*, passing the arguments on the stack or in registers according to the standard calling conventions of the language type.  
  
## Syntax  
  
```  
  
INVOKE   
expression [[, arguments]]  
```  
  
## Remarks  
 Each argument passed to the procedure may be an expression, a register pair, or an address expression (an expression preceded by `ADDR`).  
  
## See Also  
 [Directives Reference](../vs140/Directives-Reference.md)