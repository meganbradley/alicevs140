---
title: "Type parameter name &#39;&lt;typeparametername1&gt;&#39; does not match the name &#39;&lt;typeparametername2&gt;&#39; of the corresponding type parameter defined on one of the other partial types of &#39;&lt;partialtypename&gt;&#39;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 01b053c3-d1b5-4e69-b908-3d5cfc73913b
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Type parameter name &#39;&lt;typeparametername1&gt;&#39; does not match the name &#39;&lt;typeparametername2&gt;&#39; of the corresponding type parameter defined on one of the other partial types of &#39;&lt;partialtypename&gt;&#39;
A generic class or structure is defined in multiple partial declarations with conflicting type parameter specifications.  
  
 When you divide the definition of a class or structure among several partial declarations, the compiler treats the type as the union of all its partial declarations. This applies not only to the members but also to the implementation, inheritance, and access level.  
  
 You cannot specify multiple names for any type parameter in the definition of a generic class or structure.  
  
 **Error ID:** BC30931  
  
### To correct this error  
  
-   Decide what name the type parameter should have, and use the same name in every partial declaration.  
  
## See Also  
 [Partial (Visual Basic)](../Topic/Partial%20\(Visual%20Basic\).md)   
 [Class Statement (Visual Basic)](../Topic/Class%20Statement%20\(Visual%20Basic\).md)   
 [Structure Statement](../Topic/Structure%20Statement.md)   
 [NOT IN BUILD: Classes: Blueprints for Objects](assetId:///2c86373d-0333-4616-a7d8-4790c4e89f7b)   
 [Structures: Your Own Data Types](../vs140/Structures--Visual-Basic-.md)   
 [Generic Types in Visual Basic](../Topic/Generic%20Types%20in%20Visual%20Basic%20\(Visual%20Basic\).md)   
 [Type List](../vs140/Type-List--Visual-Basic-.md)