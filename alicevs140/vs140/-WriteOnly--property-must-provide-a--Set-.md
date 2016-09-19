---
title: "&#39;WriteOnly&#39; property must provide a &#39;Set&#39;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: c2b18086-9cd9-4094-b9a9-491c8d617096
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;WriteOnly&#39; property must provide a &#39;Set&#39;
If a property is declared as `WriteOnly`, it must supply a procedure for writing its value.  
  
 **Error ID:** BC30125  
  
### To correct this error  
  
1.  Make sure you include a `Set` procedure between the `Property` statement and the `End Property` statement.  
  
2.  Verify that other procedures within the `Property` declaration are correctly terminated.  
  
## See Also  
 [Property Statement](../vs140/Property-Statement.md)   
 [Set Statement](../vs140/Set-Statement--Visual-Basic-.md)