---
title: "Type arguments cannot be applied to the expression &#39;&lt;expression&gt;&#39;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: c6b9b49c-6fb2-47b8-a8bb-464562d3adfd
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Type arguments cannot be applied to the expression &#39;&lt;expression&gt;&#39;
An import alias is defined with an [Of](../Topic/Of%20Clause%20\(Visual%20Basic\).md) clause that passes type arguments to the import alias.  
  
 Type arguments are used for generic types, and only classes, structures, interfaces, procedures, and delegates can be generic. Neither namespaces nor import aliases can be generic.  
  
 **Error ID:** BC32058  
  
### To correct this error  
  
-   Remove the `Of` clause and its type arguments from the import alias.  
  
## See Also  
 [Imports Statement](../Topic/Imports%20Statement%20\(.NET%20Namespace%20and%20Type\).md)   
 [References and the Imports Statement](../vs140/References-and-the-Imports-Statement--Visual-Basic-.md)   
 [NOTINBUILD: Resolving a Reference When Multiple Variables Have the Same Name](assetId:///9601e39f-1911-44e1-ace5-3f6e090408b9)   
 [Generic Types in Visual Basic](../Topic/Generic%20Types%20in%20Visual%20Basic%20\(Visual%20Basic\).md)   
 [Type List](../vs140/Type-List--Visual-Basic-.md)