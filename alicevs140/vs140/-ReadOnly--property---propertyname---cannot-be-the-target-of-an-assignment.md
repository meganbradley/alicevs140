---
title: "&#39;ReadOnly&#39; property &#39;&lt;propertyname&gt;&#39; cannot be the target of an assignment"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d0c6cdac-a49d-49d2-ba92-ddf01eed0620
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;ReadOnly&#39; property &#39;&lt;propertyname&gt;&#39; cannot be the target of an assignment
A `ReadOnly` property occurs in a context that assigns a value to it. Only writable variables, properties, and array elements can have values assigned to them during execution.  
  
 **Error ID:** BC30098  
  
### To correct this error  
  
-   Remove the `ReadOnly` keyword from the `Property` statement declaring the variable, or remove the statement that assigns a value to it.  
  
## See Also  
 [ReadOnly](../vs140/ReadOnly--Visual-Basic-.md)   
 [Property Statement](../vs140/Property-Statement.md)