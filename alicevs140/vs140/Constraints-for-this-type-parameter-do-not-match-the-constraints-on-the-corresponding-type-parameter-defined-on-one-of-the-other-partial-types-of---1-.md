---
title: "Constraints for this type parameter do not match the constraints on the corresponding type parameter defined on one of the other partial types of &#39;|1&#39;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a38ca4ad-6bbf-421e-a0d7-c5e0a9029160
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Constraints for this type parameter do not match the constraints on the corresponding type parameter defined on one of the other partial types of &#39;|1&#39;
When you divide the definition of a class or structure among several declarations, the compiler treats the class or structure as the union of all its partial declarations. Because of this, you cannot define any conflicting modifiers or type parameter lists in the various partial declarations.  
  
 **Error ID:** BC30932  
  
### To correct this error  
  
1.  Determine which type parameter list is the desired one for your class or structure. This includes the parameters, their order, and their constraint lists.  
  
2.  Make sure every partial definition uses the identical type parameter list.  
  
## See Also  
 [Partial (Visual Basic)](../Topic/Partial%20\(Visual%20Basic\).md)   
 [Generic Types in Visual Basic](../Topic/Generic%20Types%20in%20Visual%20Basic%20\(Visual%20Basic\).md)