---
title: "Method cannot contain both an &#39;On Error GoTo&#39; statement and a lambda or query expression"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 4e7cc11e-f53d-4481-afb4-653a81d54483
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Method cannot contain both an &#39;On Error GoTo&#39; statement and a lambda or query expression
A method contains both an `On Error Goto` statement and either a lambda expression or a LINQ query. You cannot include an `On Error Goto` statement with a lambda expression or LINQ query in a method.  
  
 **Error ID:** BC36595  
  
### To correct this error  
  
1.  Replace the exception handling code that uses the `On Error Goto` statement with a `Try...Catch` statement.  
  
## See Also  
 [Introduction to Exception Handling (Visual Basic)](assetId:///9792f16a-0cd2-40bd-ace2-f7a4344c0e52)   
 [Try...Catch...Finally Statement (Visual Basic)](../vs140/Try...Catch...Finally-Statement--Visual-Basic-.md)   
 [Introduction to LINQ in Visual Basic](../Topic/Introduction%20to%20LINQ%20in%20Visual%20Basic.md)   
 [Lambda Expressions](../vs140/Lambda-Expressions--Visual-Basic-.md)   
 [On Error Statement (Visual Basic)](../Topic/On%20Error%20Statement%20\(Visual%20Basic\).md)