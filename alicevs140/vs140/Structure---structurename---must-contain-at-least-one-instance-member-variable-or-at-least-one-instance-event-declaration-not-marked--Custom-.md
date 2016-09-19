---
title: "Structure &#39;&lt;structurename&gt;&#39; must contain at least one instance member variable or at least one instance event declaration not marked &#39;Custom&#39;"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - VB
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-visual-basic
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 7054cc1e-bac3-4c3d-82f3-35772bd8dd3b
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Structure &#39;&lt;structurename&gt;&#39; must contain at least one instance member variable or at least one instance event declaration not marked &#39;Custom&#39;
A structure definition does not include any nonshared variables or nonshared noncustom events.  
  
 Every structure must have either a variable or an event that applies to each specific instance (nonshared) instead of to all instances collectively ([Shared (Visual Basic)](../Topic/Shared%20\(Visual%20Basic\).md)). Nonshared constants, properties, and procedures do not satisfy this requirement. In addition, if there are no nonshared variables and only one nonshared event, that event cannot be a `Custom` event.  
  
 **Error ID:** BC30941  
  
### To correct this error  
  
-   Define at least one variable or event that is not `Shared`. If you define only one event, it must be noncustom as well as nonshared.  
  
## See Also  
 [Structures: Your Own Data Types](../vs140/Structures--Visual-Basic-.md)   
 [Structure Declaration](../vs140/How-to--Declare-a-Structure--Visual-Basic-.md)   
 [Structure Statement](../Topic/Structure%20Statement.md)