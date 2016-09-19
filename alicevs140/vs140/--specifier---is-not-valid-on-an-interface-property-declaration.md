---
title: "&#39;&lt;specifier&gt;&#39; is not valid on an interface property declaration"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: f10c4f5f-6176-4dba-99a9-b58f3b390fba
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;&lt;specifier&gt;&#39; is not valid on an interface property declaration
A `Property` statement inside an interface contains an invalid keyword, such as `Implements`. An interface can only define members, not implement them.  
  
 **Error ID:** BC30273  
  
### To correct this error  
  
-   Remove the invalid keyword from the declaration statement.  
  
-   Move the implementation of interface members to a class that implements the interface.  
  
## See Also  
 [Interface Statement](../vs140/Interface-Statement--Visual-Basic-.md)   
 [Implements Statement](../vs140/Implements-Statement.md)