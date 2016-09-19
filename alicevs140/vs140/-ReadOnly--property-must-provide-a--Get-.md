---
title: "&#39;ReadOnly&#39; property must provide a &#39;Get&#39;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a522c39e-1f11-45c8-a00b-3546c842909a
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;ReadOnly&#39; property must provide a &#39;Get&#39;
If a property is declared as `ReadOnly`, it must supply a procedure for reading its value.  
  
 **Error ID:** BC30126  
  
### To correct this error  
  
1.  Make sure you include a `Get` procedure between the `Property` statement and the `End Property` statement.  
  
2.  Verify that other procedures within the `Property` declaration are correctly terminated.  
  
## See Also  
 [Property Statement](../vs140/Property-Statement.md)   
 [Get Statement](../vs140/Get-Statement.md)