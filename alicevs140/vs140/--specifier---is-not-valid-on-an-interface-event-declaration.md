---
title: "&#39;&lt;specifier&gt;&#39; is not valid on an interface event declaration"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: bd12c952-c619-4753-8d6d-90ef4086fdc2
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;&lt;specifier&gt;&#39; is not valid on an interface event declaration
An `Event` statement inside an interface contains a keyword that is not allowed, such as `Implements`. An interface can only define members, not implement them.  
  
 **Error ID:** BC30275  
  
### To correct this error  
  
1.  Remove the keyword from the declaration statement.  
  
2.  Move the implementation of interface members to a class that implements the interface.  
  
## See Also  
 [Interface Statement](../vs140/Interface-Statement--Visual-Basic-.md)   
 [Implements Statement](../vs140/Implements-Statement.md)