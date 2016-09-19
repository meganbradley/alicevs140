---
title: "Attribute cannot be used because it does not have a Public constructor"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b72d1ff2-f6b2-4a89-9ac2-8765f77bcc97
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Attribute cannot be used because it does not have a Public constructor
The constructor for the attribute being used is `Private`, and cannot be used.  
  
 **Error ID:** BC30758  
  
### To correct this error  
  
1.  If you see this error with a custom attribute that you developed, change its `Sub``New` constructor's access modifier to `Public`.  
  
## See Also  
 [NOT IN BUILD: Attributes in Visual Basic](assetId:///620bfc0e-4582-4c8b-8432-ebc5c3dccc22)   
 [Object Lifetime: How Objects Are Created and Destroyed](../Topic/Object%20Lifetime:%20How%20Objects%20Are%20Created%20and%20Destroyed%20\(Visual%20Basic\).md)