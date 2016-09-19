---
title: "&#39;Group&#39; not allowed in this context; identifier expected"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ef6b453e-68e7-47c2-997c-9fd1ca074217
caps.latest.revision: 5
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;Group&#39; not allowed in this context; identifier expected
The `Group` keyword is included in the `Into` section of an `Aggregate` clause. The `Group` keyword is only valid in the `Group By` or `Group Join` clauses.  
  
 **Error ID:** BC36618  
  
### To correct this error  
  
-   Remove the `Group` keyword from the `Aggregate` clause. You can add a `Group By` clause to the query to group results.  
  
## See Also  
 [Aggregate Clause (Visual Basic)](../vs140/Aggregate-Clause--Visual-Basic-.md)   
 [Group By Clause (Visual Basic)](../vs140/Group-By-Clause--Visual-Basic-.md)   
 [Group Join Clause (Visual Basic)](../vs140/Group-Join-Clause--Visual-Basic-.md)   
 [Introduction to LINQ in Visual Basic](../Topic/Introduction%20to%20LINQ%20in%20Visual%20Basic.md)   
 [LINQ in Visual Basic](../vs140/LINQ-in-Visual-Basic.md)