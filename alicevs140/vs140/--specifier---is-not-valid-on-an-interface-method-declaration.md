---
title: "&#39;&lt;specifier&gt;&#39; is not valid on an interface method declaration"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 598f2944-3e5d-4686-b6f7-2b4bcaf5c211
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;&lt;specifier&gt;&#39; is not valid on an interface method declaration
A `Function` or `Sub` statement inside an interface contains an invalid keyword, such as `Implements`. An interface can only define members, not implement them.  
  
 **Error ID:** BC30270  
  
### To correct this error  
  
1.  Remove the invalid keyword from the declaration statement.  
  
2.  Move the implementation of interface members to a class that implements the interface.  
  
## See Also  
 [Interface Statement](../vs140/Interface-Statement--Visual-Basic-.md)   
 [Implements Statement](../vs140/Implements-Statement.md)