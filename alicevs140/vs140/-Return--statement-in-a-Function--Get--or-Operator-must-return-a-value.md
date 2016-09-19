---
title: "&#39;Return&#39; statement in a Function, Get, or Operator must return a value"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: af0fb1fc-1b2e-4cae-9768-10965cda5506
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;Return&#39; statement in a Function, Get, or Operator must return a value
`Return` statements must be used to return a value to a calling procedure. You cannot use `Return` statements by themselves to control program flow.  
  
 **Error ID:** BC30654  
  
### To correct this error  
  
1.  Specify a value that the function or procedure can return.  
  
2.  Use the `End` statement to cause the program to exit the current procedure.  
  
## See Also  
 [Return Statement](../vs140/Return-Statement--Visual-Basic-.md)   
 [End <keyword\> Statement](../vs140/End--keyword--Statement--Visual-Basic-.md)