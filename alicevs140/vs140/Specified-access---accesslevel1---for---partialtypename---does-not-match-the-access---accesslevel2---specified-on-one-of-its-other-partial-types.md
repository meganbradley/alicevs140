---
title: "Specified access &#39;&lt;accesslevel1&gt;&#39; for &#39;&lt;partialtypename&gt;&#39; does not match the access &#39;&lt;accesslevel2&gt;&#39; specified on one of its other partial types"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: aabe0f4a-dc02-4828-a837-20cd47a7bd43
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Specified access &#39;&lt;accesslevel1&gt;&#39; for &#39;&lt;partialtypename&gt;&#39; does not match the access &#39;&lt;accesslevel2&gt;&#39; specified on one of its other partial types
A class or structure is defined in multiple partial declarations with conflicting access level specifications.  
  
 When you divide the definition of a class or structure among several partial declarations, the compiler treats the type as the union of all its partial declarations. This applies not only to the members but also to the implementation, inheritance, and access level.  
  
 You cannot mix access levels in the definition of a class or structure. Even the combination `Protected Friend` is allowed only when the keywords are contiguous in the same declaration statement.  
  
 **Error ID:** BC30925  
  
### To correct this error  
  
-   Decide what the access level of the class should be, and remove any conflicting access level specifications.  
  
## See Also  
 [Partial (Visual Basic)](../Topic/Partial%20\(Visual%20Basic\).md)   
 [Access Levels in Visual Basic](../vs140/Access-Levels-in-Visual-Basic.md)   
 [Class Statement (Visual Basic)](../Topic/Class%20Statement%20\(Visual%20Basic\).md)   
 [Structure Statement](../Topic/Structure%20Statement.md)   
 [NOT IN BUILD: Classes: Blueprints for Objects](assetId:///2c86373d-0333-4616-a7d8-4790c4e89f7b)   
 [Structures: Your Own Data Types](../vs140/Structures--Visual-Basic-.md)