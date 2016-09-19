---
title: "&#39;Using&#39; resource variable must have an explicit initialization"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 5db996a6-0802-4b67-91f1-4aa9c3dd6b09
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;Using&#39; resource variable must have an explicit initialization
A `Using` statement specifies at least one resource that it does not initialize with a `New` clause.  
  
 If you have not already acquired the resource before passing control to the `Using` block, the `Using` statement must acquire the resource. To do this, it must create an object from the specified class, which requires a `New` clause.  
  
 **Error ID:** BC36011  
  
### To correct this error  
  
-   If you have already acquired the resource, use a reference variable or expression in the `Using` statement that evaluates to the acquired resource.  
  
     `Dim newFont As New System.Drawing.Font`  
  
     `Using newFont`  
  
-   If you have not already acquired the resource, add a `New` clause to the `Using` statement.  
  
     `Using newFont as`   `New`   `System.Drawing.Font`  
  
## See Also  
 [Using Statement (Visual Basic)](../Topic/Using%20Statement%20\(Visual%20Basic\).md)   
 [New (Visual Basic)](../vs140/New-Operator--Visual-Basic-.md)   
 [How to: Dispose of a System Resource](../Topic/How%20to:%20Dispose%20of%20a%20System%20Resource%20\(Visual%20Basic\).md)